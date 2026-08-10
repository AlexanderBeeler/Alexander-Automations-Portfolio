# E-Commerce Order & Inventory Automation

## Overview

An automated order processing workflow that validates payments, checks product inventory, and automatically updates stock levels.

The workflow receives order information including the order ID, customer details, product, SKU, quantity, price, and payment status.

Orders with an invalid payment status are stopped and reported through Discord. Valid orders are matched to their corresponding product inventory, where available stock is checked before the order is processed.

## Workflow

![E-Commerce Order Processing Workflow](images/E%20Commerce)

```text id="tq8i1a"
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
* Rejects unpaid/invalid orders
* Sends Discord alerts for invalid payments
* Identifies the ordered product
* Checks available inventory
* Rejects orders when stock is unavailable
* Updates inventory after a successful order
* Subtracts the ordered quantity from the current stock

## Tools Used

* Google Sheets
* Discord
* Automation workflows
* Conditional logic
* Data mapping
* Inventory management

## Inventory Logic

Product inventory is stored in Google Sheets.

When a valid order is received, the workflow checks the appropriate product path and compares the requested quantity against the available stock.

If sufficient stock exists:

`Current Stock - Ordered Quantity = Updated Stock`

The updated inventory is then saved back to Google Sheets.

If sufficient stock is not available, the order is stopped and a Discord alert is sent.

**[!]**

## Payment Validation

Orders are only allowed to continue when the payment status is valid.

Invalid payment statuses trigger a Discord notification instead of continuing to the inventory process.

**[!]**

## Product Routing

The workflow currently uses three product-specific paths to handle inventory checks.

For example:

**Mechanical Keyboard → Mechanical Keyboard inventory → Stock check → Update inventory**

The same process is applied to the other supported products.

**[!]**

## Screenshots

### Workflow

**[!]**

### Inventory

**[!]**

### Discord Alerts

**[!]**

### Successful Order

**[!]**

## Workflow

**[!]**
