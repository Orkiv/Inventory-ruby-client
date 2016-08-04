# InventoryClient::Order

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**order_id** | **String** | Order ID | [optional] 
**info_email** | **String** | Customer email | [optional] 
**info_first** | **String** | Customer first name | [optional] 
**info_last** | **String** | Customer last name | [optional] 
**phone** | **String** | Customer phone number | [optional] 
**shipset** | **BOOLEAN** | Customer billing address matches shipping address | [optional] 
**info_adr1** | **String** | Customer billing address line &#39;1&#39; | [optional] 
**info_adr2** | **String** | Customer billing address line &#39;2&#39; | [optional] 
**info_cty** | **String** | Customer billing city | [optional] 
**info_zip** | **String** | Customer billing zip code | [optional] 
**state** | **String** | Customer billing state | [optional] 
**info_sadr1** | **String** | Customer shipping address line &#39;1&#39; | [optional] 
**info_sadr2** | **String** | Customer shipping address line &#39;2&#39; | [optional] 
**info_scty** | **String** | Customer shipping city | [optional] 
**info_szip** | **String** | Customer shipping zip code | [optional] 
**sstate** | **String** | Customer shipping state | [optional] 
**tax_amount** | **Float** | Tax amount in hundreds. Must divide by &#39;100&#39; for USD value | [optional] 
**shipping_amount** | **Float** | Shipping total in USD | [optional] 
**amount_total** | **Float** | Checkout total in USD | [optional] 
**item_i_ds** | **Array&lt;String&gt;** | Array of items purchased at checkout | [optional] 


