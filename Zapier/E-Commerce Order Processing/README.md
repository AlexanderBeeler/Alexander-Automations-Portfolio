# E-Commerce Order & Inventory Automation

## Overview

An automated order processing workflow that validates payment status, checks product inventory, and updates stock levels.

The workflow receives order information including:

* Order ID
* Customer Name
* Email
* Product
* SKU
* Quantity
* Price
* Payment Status

Orders with an invalid payment status are stopped and reported through Discord. Valid orders are matched to their corresponding product inventory and checked against available stock before the inventory is updated.

## Workflow

![E-Commerce Workflow](images/Zapier%20E-Commerce.png)

```text
Order Information
       ↓
Payment Status Check
       ↓
   Payment Valid?
     ↙       ↘
   No         Yes
   ↓           ↓
Discord      Product
Alert         Match
               ↓
        ┌──────┼──────┐
        ↓      ↓      ↓
     Product Product Product
      Path 1  Path 2  Path 3
        ↓      ↓      ↓
      Check Inventory
            ↓
       Stock Available?
         ↙        ↘
       No          Yes
       ↓            ↓
 Discord Alert   Update Stock
                    ↓
             Current Stock
             - Order Quantity
```

## What It Does

* Receives and maps order information
* Validates payment status
* Rejects unpaid or invalid orders
* Sends Discord alerts for invalid payments
* Identifies the ordered product
* Checks available inventory
* Rejects orders when stock is unavailable
* Updates inventory after a successful order
* Subtracts the ordered quantity from current stock

## Payment Validation

Orders only continue when the payment status is valid.

If an invalid payment status is received, the order is stopped and a Discord alert is sent instead of continuing to the inventory process.

![Invalid Payment Discord Alert](images/payment-failed.png)

## Inventory Logic

Product inventory is stored in Google Sheets.

After payment is validated, the workflow routes the order to the appropriate product path and checks whether enough inventory is available.

If sufficient stock exists, the workflow updates the inventory by subtracting the ordered quantity from the current stock.

`Current Stock - Ordered Quantity = Updated Stock`

![Inventory Google Sheet](images/Zapier%20E-Commerce%20Stock%20Sheet.png)

If sufficient stock is not available, the order is stopped and a Discord alert is sent.

## Product Routing

The workflow currently uses three product-specific paths to handle inventory checks.

For example:

**Mechanical Keyboard → Mechanical Keyboard inventory → Stock check → Update inventory**

The same process is applied to the other supported products.

## Failed Order

If the requested quantity exceeds the available inventory, the order is stopped and does not update the stock.

The workflow sends an alert indicating that the order cannot be fulfilled due to insufficient inventory.

![Failed Order](images/Zapier%20E-Commerce%20Order%20Failed.png)

## Tools Used

* Google Sheets
* Discord
* Conditional logic
* Data mapping
* Inventory management
* Automation workflows
