# Create sales invoice using Rest API
    POST /api/method/systemaerp.accounts.utils.create_invoice
  ## Headers
  |Header                |Format                          |Example                         |
|----------------|-------------------------------|-----------------------------|
|Authorization|`token [Api Key]:[Api Secret]`            |`token 3feguids45:h56bncds24`           |
  ## Body
  |Field                |Description                          |Example                         |
|----------------|-------------------------------|-----------------------------|
|`name`| Required: Invoice No (string)            |04542           |
|`posting_date`| Required: Issue date of the invoice (string)            |2023-09-11           |
|`posting_time`| Required: Issue time of the invoice (string)            |23:55:0.58           |
|`customer`| Required: Customer Details (object)           |[Customer Details](#customer-details)           |
|`items`| Required: Invoice Items (array)            |[Item Details](#item-details)         |

  ## Customer Details
  |Field                |Description                          |Example                         |
|----------------|-------------------------------|-----------------------------|
|`name`| Required: Customer Name (string)           |Test Company           |
|`type`| Required: Customer Type : Can be `Company` or `Individual` (string)           |Company           |
|`tax_id`| Required if `type` is `Company`: Customer Tax ID (string)           |00893838223          |
|`mobile_no`| Optional: Customer Phone Number (string)            |+9665426233           |

  ## Item Details
  |Field                |Description                          |Example                         |
|----------------|-------------------------------|-----------------------------|
|`item_code`| Required: Item Code (string)           |Item - 0001           |
|`item_name`| Required: Item Name or Description (string)           |Transportation Service           |
|`uom`| Required: Item UOM (string)           |Unit          |
|`qty`| Required: Item Qty (float)           |2.00           |
|`rate`| Required: Item Rate (float)           |900.00           |
|`amount`| Required: Item Amount `qty * amount`  (float)           |1800.00           |
|`Tax`| Required: Item tax percent  (string)           |15%           |

