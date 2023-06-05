---
title: Order Object
type: endpoint
category: 639ba2628407100061f5faac
parentDoc: 639ba2658407100061f5fab8
slug: order-object
hidden: false
order: 1
---

| Attributes |  Description  | Example |
|:-----|:--------|------:|
| id | <p>Unique order ID, assigned by Voucherify.</p> | <p>ord_GFDbbv2I0wnO0sFUBOOOXPj2</p> |
| source_id | <p>The merchant’s order ID if it is different from the Voucherify order ID. It is really useful in case of integration between multiple systems. It can be an order ID from CRM, database or 3rd party service.</p> |  |
| created_at | <p>Timestamp representing the date and time when the order was created in ISO 8601 format.</p> | <p>2022-03-09T11:19:04.819Z</p> |
| updated_at | <p>Timestamp representing the date and time when the order was updated in ISO 8601 format.</p> | <p>2022-08-12T13:34:10.681Z</p> |
| status | <p>Order status.</p> Available values: `CREATED`, `PAID`, `CANCELED`, `FULFILLED` |  |
| amount | <p>Order amount before applying any discount.</p> |  |
| discount_amount | <p>Sum of all order-level discounts applied to the order.</p> |  |
| items_discount_amount | <p>Sum of all product-specific discounts applied to the order.<br><code>sum(items, i =&gt; i.discount_amount)</code></p> |  |
| total_discount_amount | <p>Sum of all order-level AND all product-specific discounts applied to the order.<br><code>total_discount_amount</code> = <code>discount_amount</code> + <code>items_discount_amount</code></p> |  |
| total_amount | <p>Order amount after applying all the discounts.<br><code>total_amount</code> = <code>amount</code> - <code>total_discount_amount</code></p> |  |
| items | <p>Array of order items that have been applied to the order. Each order item can show the effects of particular discounts on the item-level.</p> Array of: <table><thead><tr><th style="text-align:left">Attributes</th><th style="text-align:left">Description</th><th style="text-align:right">Example</th></tr></thead><tbody><tr><td style="text-align:left">object</td><td style="text-align:left"><p>The type of object represented by JSON. This object stores information about the <code>order_item</code>.</p></td><td style="text-align:right"></td></tr><tr><td style="text-align:left">product_id</td><td style="text-align:left"><p>A unique identifier that represents the product and is assigned by Voucherify.</p></td><td style="text-align:right"><p>prod_5h0wc453_1</p></td></tr><tr><td style="text-align:left">sku_id</td><td style="text-align:left"><p>A unique identifier that represents the SKU and is assigned by Voucherify.</p></td><td style="text-align:right"><p>sku_prod_5h0wc453_1_1</p></td></tr><tr><td style="text-align:left">quantity</td><td style="text-align:left"><p>Quantity of the item in the cart.</p></td><td style="text-align:right"></td></tr><tr><td style="text-align:left">amount</td><td style="text-align:left"><p>Represents a total pre-discount amount of order item (<code>price</code> * <code>quantity</code>).</p></td><td style="text-align:right"></td></tr><tr><td style="text-align:left">discount_amount</td><td style="text-align:left"><p>The item-level discount applied to the item.</p></td><td style="text-align:right"></td></tr><tr><td style="text-align:left">price</td><td style="text-align:left"><p>Unit price of an item. Value is multiplied by 100 to precisely represent 2 decimal places. For example, $100 is written as 10000.</p></td><td style="text-align:right"></td></tr><tr><td style="text-align:left">subtotal_amount</td><td style="text-align:left"><p>Final order item amount after the applied item-level discount.  If there are no item-level discounts applied, this item is equal to the <code>amount</code>.<br><code>subtotal_amount</code>=<code>amount</code>-<code>discount_amount</code></p></td><td style="text-align:right"></td></tr><tr><td style="text-align:left">product</td><td style="text-align:left"><p>This object stores more information about the related product.</p> <table><thead><tr><th style="text-align:left">Attributes</th><th style="text-align:left">Description</th><th style="text-align:right">Example</th></tr></thead><tbody><tr><td style="text-align:left">id</td><td style="text-align:left"><p>A unique identifier that represents the product and is assigned by Voucherify.</p></td><td style="text-align:right"><p>prod_5h0wc453_1</p></td></tr><tr><td style="text-align:left">source_id</td><td style="text-align:left"><p>A unique product identifier from your inventory system.</p></td><td style="text-align:right"><p>illy-arabica</p></td></tr><tr><td style="text-align:left">name</td><td style="text-align:left"><p>Product name.</p></td><td style="text-align:right"><p>Brewing System</p></td></tr><tr><td style="text-align:left">price</td><td style="text-align:left"><p>Unit price of a product. Value is multiplied by 100 to precisely represent 2 decimal places. For example, $100 is written as 10000.</p></td><td style="text-align:right"></td></tr></tbody></table></td><td style="text-align:right"></td></tr><tr><td style="text-align:left">sku</td><td style="text-align:left"><p>This object stores more information about the related SKU.</p> <table><thead><tr><th style="text-align:left">Attributes</th><th style="text-align:left">Description</th><th style="text-align:right">Example</th></tr></thead><tbody><tr><td style="text-align:left">id</td><td style="text-align:left"><p>A unique identifier that represents the SKU and is assigned by Voucherify.</p></td><td style="text-align:right"><p>sku_prod_5h0wc453_1_1</p></td></tr><tr><td style="text-align:left">source_id</td><td style="text-align:left"><p>A unique SKU identifier from your inventory system.</p></td><td style="text-align:right"><p>illy-arabica-250g</p></td></tr><tr><td style="text-align:left">sku</td><td style="text-align:left"><p>SKU name.</p></td><td style="text-align:right"></td></tr><tr><td style="text-align:left">price</td><td style="text-align:left"><p>Unit price of a SKU. Value is multiplied by 100 to precisely represent 2 decimal places. For example, $100 is written as 10000.</p></td><td style="text-align:right"></td></tr></tbody></table></td><td style="text-align:right"></td></tr></tbody></table> |  |
| metadata | <p>The metadata object stores all custom attributes assigned to the order. A set of key/value pairs that are attached to an order object. Stores additional information about the order in a structured format.</p>  |  |
| customer | <p>Object containing information about the customer that is making the purchase.</p> <table><thead><tr><th style="text-align:left">Attributes</th><th style="text-align:left">Description</th><th style="text-align:right">Example</th></tr></thead><tbody><tr><td style="text-align:left">id</td><td style="text-align:left"><p>Unique customer ID of the customer making the purchase.</p></td><td style="text-align:right"><p>cust_7iUa6ICKyU6gH40dBU25kQU1</p></td></tr><tr><td style="text-align:left">object</td><td style="text-align:left"><p>Type of object represented by the <code>customer</code> object.</p></td><td style="text-align:right"></td></tr></tbody></table> |  |
| referrer | <p>Object containing information about the referrer.</p> <table><thead><tr><th style="text-align:left">Attributes</th><th style="text-align:left">Description</th><th style="text-align:right">Example</th></tr></thead><tbody><tr><td style="text-align:left">id</td><td style="text-align:left"><p>Unique referrer ID, who referred the customer making the purchase.</p></td><td style="text-align:right"><p>cust_7iUa6ICKyU6gH40dBU25kQU1</p></td></tr><tr><td style="text-align:left">object</td><td style="text-align:left"><p>Type of object represented by the referrer object.</p></td><td style="text-align:right"></td></tr></tbody></table> |  |
| customer_id | <p>Unique customer ID of the customer making the purchase.</p> | <p>cust_7iUa6ICKyU6gH40dBU25kQU1</p> |
| referrer_id | <p>Unique referrer ID.</p> | <p>cust_nM4jqPiaXUvQdVSA6vTRUnix</p> |
| object | <p>The type of object represented by JSON. This object stores information about the <code>order</code>.</p> |  |
| redemptions | One of: <h2>Unstacked Redemption</h2><table><thead><tr><th style="text-align:left">Attributes</th><th style="text-align:left">Description</th><th style="text-align:right">Example</th></tr></thead><tbody><tr><td style="text-align:left">redemption_ID</td><td style="text-align:left"><p>The property name is the unique redemption ID; i.e. <code>r_0ba186c4824e4881e1</code>. This object contains information about the redemption of an incentive.</p> <table><thead><tr><th style="text-align:left">Attributes</th><th style="text-align:left">Description</th><th style="text-align:right">Example</th></tr></thead><tbody><tr><td style="text-align:left">date</td><td style="text-align:left"><p>Timestamp representing the date and time when the redemption was created in ISO 8601 format.</p></td><td style="text-align:right"><p>2022-09-02T17:06:56.649Z</p></td></tr><tr><td style="text-align:left">related_object_type</td><td style="text-align:left"><p>The source of the incentive.</p> Available values: <code>voucher</code>, <code>promotion_tier</code></td><td style="text-align:right"></td></tr><tr><td style="text-align:left">related_object_id</td><td style="text-align:left"><p>Unique ID of the related object that defines the incentive.</p></td><td style="text-align:right"></td></tr><tr><td style="text-align:left">related_object_parent_id</td><td style="text-align:left"><p>Represent's the campaign ID of the voucher if the redemption was based on a voucher that was part of bulk codes generated within a campaign. In case of a promotion tier, this represents the campaign ID of the promotion tier's parent campaign.</p></td><td style="text-align:right"></td></tr></tbody></table></td><td style="text-align:right"></td></tr></tbody></table> <h2>Stacked Redemption</h2><table><thead><tr><th style="text-align:left">Attributes</th><th style="text-align:left">Description</th><th style="text-align:right">Example</th></tr></thead><tbody><tr><td style="text-align:left">redemption_ID</td><td style="text-align:left"><p>The property name is the unique parent redemption ID; i.e. <code>r_0ba186c4824e4881e1</code>. This object contains information about the redemption of multiple incentives.</p> <table><thead><tr><th style="text-align:left">Attributes</th><th style="text-align:left">Description</th><th style="text-align:right">Example</th></tr></thead><tbody><tr><td style="text-align:left">date</td><td style="text-align:left"><p>Timestamp representing the date and time when the redemption was created in ISO 8601 format.</p></td><td style="text-align:right"><p>2022-09-02T17:06:56.649Z</p></td></tr><tr><td style="text-align:left">related_object_type</td><td style="text-align:left"><p>The source of the incentive.</p></td><td style="text-align:right"></td></tr><tr><td style="text-align:left">related_object_id</td><td style="text-align:left"><p>Unique ID of the parent redemption.</p></td><td style="text-align:right"><p>r_0ba186c4824e4881e1</p></td></tr><tr><td style="text-align:left">stacked</td><td style="text-align:left"><p>Contains a list of unique IDs of child redemptions, which belong to the stacked incentives.</p></td><td style="text-align:right"></td></tr></tbody></table></td><td style="text-align:right"></td></tr></tbody></table> |  |

[block:html]
{
  "html": "<style>\n[title=\"Toggle library\"] { \n  display: none; }\n.LanguagePicker-divider { \n  display: none; }\n.Playground-section3VTXuaYZivJK > .APISectionHeader3LN_-QIR0m7x {\n  display: none; }\n.LanguagePicker-languages1qVVo_v6AlP9 {\n  display: none; }\n.headline-container-article-info2GaOf2jMpV0r {\n  display: none; }\n.APISectionHeader3LN_-QIR0m7x {\n  display: none; }\n.APIResponseSchemaPicker-label3XMQ9E-slNcS {\n  display: none; }\n.PlaygroundC7DInM9NFvBg {\n  display: none; }\n.Modal-Header3VPrQs3MUWWd {\n  display: none; }\n.rm-ReferenceMain .rm-Article {\n  max-width: 2000px; }\n</style>"
}
[/block]