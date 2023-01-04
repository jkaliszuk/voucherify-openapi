# Changelog

## 20230101 - Transition to Interactive documentation

- Definitions of object schemas that were previously availalbe in a separate document are now viewable by navigating to the specified endpoints described in the API reference document titled Object schemas.

### Slugs updated for Reference Docs

| **API** | **Endpoint** | **Previous Slug** | **New Slug** |
|---|---|---|---|
| **Vouchers** | Get Voucher | vouchers-get | get-voucher |
|  | Import Vouchers | import-vouchers-1 | import-vouchers |
|  | Import Vouchers using CSV | import-vouchers-by-csv-1 | import-vouchers-using-csv |
|  | Examine Qualification | push-qualification-request | examine-vouchers-qualification |
|  | Update Vouchers in bulk | aa-update-vouchers-in-bulk | update-vouchers-in-bulk |
|  | Update Vouchers Metadata in bulk | aaupdate-vouchers-metadata-in-bulk | update-vouchers-metadata-in-bulk |
| **Campaigns** | Add Vouchers to Campaign | add-voucher-to-campaign | add-vouchers-to-campaign |
|  | Add Voucher with certain code to Campaign | add-voucher-with-certain-code-to-campaign | add-voucher-with-specific-code-to-campaign |
|  | Import Vouchers to Campaign | import-vouchers | import-vouchers-to-campaign |
|  | Import Vouchers to Campaign by CSV | import-vouchers-by-csv | import-vouchers-to-campaign-using-csv |
|  | Examine Qualification | create-qualification-request | examine-campaigns-qualification |
| **Promotions** | List Promotion Tiers from Campaign | get-promotions | list-promotion-tiers-from-campaign |
|  | Update Promotion Tier | update-promotion | update-promotion-tier |
|  | Delete Promotion Tier | delete-promotion | delete-promotion-tier |
|  | List Promotion Stacks | list-promotion-stacks | list-promotion-stacks-in-campaign |
| **Validations** | Validate Voucher (client-side) | vouchers-validate | validate-voucher-client-side |
|  | Validate Promotions | validate-promotions-1 | validate-promotions |
| **Redemptions** | Get Voucher's Redemptions | vouchers-redemptions | get-voucher-redemptions |
| **Stackable Discounts** | Validate Stackable Discounts | validate-stacked-discounts-1 | validate-stacked-discounts |
|  | Rollback Stackable Redemptions | rollback-stackable-redemptions | rollback-stacked-redemptions |
| **Loyalties** | Get Reward Assignment | get-reward-assignment | get-reward-assignment-1 |
|  | Get Reward Assignment | get-reward-assignment-1 | get-reward-assignment-2 |
|  | Redeem Reward | redeem-loyalty-card | redeem-reward-1 |
|  | Add Member | create-member | add-member |
|  | Add or Remove Loyalty Card Balance | add-loyalty-card-balance | add-remove-loyalty-card-balance-1 |
|  | Transfer Loyalty Points | transfer-points2 | transfer-points |
| **Customers** | Get Customer | read-customer | get-customer |
|  | Update Customers in Bulk | post-customers-in-bulk | update-customers-in-bulk |
|  | Update Customers Metadata in Bulk | post-customers-metadata-in-bulk | update-customers-metadata-in-bulk |
|  | Update Customer's consents (client) | update-customers-consents-client | update-customers-consents-client-side |
|  | List Customer Activities | get-customer-activities | list-customer-activities |
|  | List Customer's Segments | list-segments | list-customer-segments |
| **Orders** | Create Export | create-export-1 | create-order-export |
| **Products** | Update Products in bulk | post-products-in-bulk | update-products-in-bulk |
|  | Update Products Metadata in bulk | async-update-products-metadata-in-bulk | update-products-metadata-in-bulk |
|  | Get SKU | get-sku-v20210726 | get-sku |
|  | List SKUs | list-skus | list-skus-in-product |
|  | Import Products Using CSV | import-products-by-csv | import-products-using-csv |
|  | Import SKUS using CSV | import-skus-by-csv | import-skus-using-csv |
| **Product Collections** | List Products in Collection | get-products-in-collection | list-products-in-collection |
| **Validation Rules** | Get Validation Rules | get-validation-rules | get-validation-rule |
|  | Update Validation Rule | update-validation-rules | update-validation-rule |
|  | Create Validation Rules Assignment | create-validation-rules-assignment | create-validation-rule-assignment |
|  | Delete Validation Rules Assignment | delete-validation-rules-assignment | delete-validation-rule-assignment |
| **Events** | Track Custom Event | create-custom-event | track-custom-event |
| **Consents** | List Consents | get-consents | list-consents |
|  | List Consents (client-side) | get-consent-client-side | list-consents-client-side |
| **Async Actions** | Get Async Action | get-async-actions-1 | get-async-action |

### Slugs updated for Guides

| **Category** | **Guide** | **Previous Slug** | **New Slug** |
|:---|:---|:---|:---|
| More | Status | status-1 | status |
| Building Blocks | Orders | orders-1 | orders |
| Building Blocks | Vouchers | vouchers-1 | vouchers |
| Building Blocks | Campaigns | campaigns-1 | campaigns |

### Endpoints descriptions that were removed

| **API** | **Endpoint Name** | **Endpoint** | **Slug** | **Why** |
|---|---|---|---|---|
| **Vouchers** | [deprecated] Update Vouchers' metadata in bulk | **POST** `/vouchers/metdata` | update-vouchers-metadata-in-bulk | deprecated |
|  | [deprecated] Update Vouchers in bulk | **POST** `/vouchers/bulk` | update-vouchers-in-bulk | deprecated |
| **Promotions** | List Promotion Tiers (client-side) | **POST** `promotions/tiers` | list-promotion-tiers-client-side | same as server-side |
|  | Create Promotion Campaign | **POST** `/campaigns` | create-promotion-campaign | path exists under Campaigns API |
| **Stackable Discounts** | Validate Stackable Discounts (client-side) | **POST** `/validations` | validate-stackable-discounts-client-side | same as server-side |
|  | Redeem Stackable Discounts (client-side) | **POST** `/redemptions` | redeem-stackable-discounts-client-side | same as server-side |
| **Customers** | [deprecated] Update Customers' metadata in bulk | **POST** `customers/metadata` | update-customers-metadata-in-bulk | deprecated |
|  | [deprecated] Update Customers in bulk | **POST** `customers/bulk` | update-customers-in-bulk | deprecated |
| **Orders** | Download Export | **GET** `/exports/{id}` | download-export-1 | same in Exports API |
| **Products** | [deprecated] Update Products metadata in bulk | **POST** `/products/metadata` | update-products-metadata-in-bulk | deprecated |
|  | [deprecated] Update Products in bulk | **POST** `/products/bulk` | update-products-in-bulk | deprecated |
|  | Get SKU [deprecated] | **GET** `/products/{productId}/skus/{skuId}` | get-sku | deprecated |
| **Events** | Track Custom Event (client-side) | **POST** `/events` | track-custom-event-client-side | same as server-side |

### Endpoints that were added

| **API** | **Endpoint Name** | **Endpoint** | **Slug** |
|---|---|---|---|
| Rewards | Get Reward Assignment | **GET** `/rewards/{rewardId}/assignments/{assignmentId}` | get-reward-assignment |