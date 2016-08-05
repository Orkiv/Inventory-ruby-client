# InventoryClient::DefaultApi

All URIs are relative to *https://www.orkiv.com/i/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**all_get**](DefaultApi.md#all_get) | **GET** /all/ | 
[**categories_delete**](DefaultApi.md#categories_delete) | **DELETE** /categories/ | 
[**categories_post**](DefaultApi.md#categories_post) | **POST** /categories/ | 
[**categories_put**](DefaultApi.md#categories_put) | **PUT** /categories/ | 
[**item_add_post**](DefaultApi.md#item_add_post) | **POST** /item/add/ | 
[**item_addbulk_post**](DefaultApi.md#item_addbulk_post) | **POST** /item/addbulk/ | 
[**item_delete**](DefaultApi.md#item_delete) | **DELETE** /item/ | 
[**item_get**](DefaultApi.md#item_get) | **GET** /item/ | 
[**item_media_delete**](DefaultApi.md#item_media_delete) | **DELETE** /item-media/ | 
[**item_media_post**](DefaultApi.md#item_media_post) | **POST** /item-media/ | 
[**item_put**](DefaultApi.md#item_put) | **PUT** /item/ | 
[**items_count_post**](DefaultApi.md#items_count_post) | **POST** /items/count/ | 
[**items_post**](DefaultApi.md#items_post) | **POST** /items/ | 
[**orders_post**](DefaultApi.md#orders_post) | **POST** /orders/ | 
[**orders_services_post**](DefaultApi.md#orders_services_post) | **POST** /orders/services/ | 
[**query_post**](DefaultApi.md#query_post) | **POST** /query/ | 
[**services_delete**](DefaultApi.md#services_delete) | **DELETE** /services/ | 
[**services_get**](DefaultApi.md#services_get) | **GET** /services/ | 
[**services_open_get**](DefaultApi.md#services_open_get) | **GET** /services/open/ | 
[**services_post**](DefaultApi.md#services_post) | **POST** /services/ | 
[**services_put**](DefaultApi.md#services_put) | **PUT** /services/ | 
[**variation_delete**](DefaultApi.md#variation_delete) | **DELETE** /variation/ | 
[**variation_get**](DefaultApi.md#variation_get) | **GET** /variation/ | 
[**variation_post**](DefaultApi.md#variation_post) | **POST** /variation/ | 
[**variation_put**](DefaultApi.md#variation_put) | **PUT** /variation/ | 
[**write_delete**](DefaultApi.md#write_delete) | **DELETE** /write/ | 
[**write_post**](DefaultApi.md#write_post) | **POST** /write/ | 


# **all_get**
> Array&lt;InventoryGroup&gt; all_get



### Example
```ruby
# load the gem
require 'InventoryClient'
# setup authorization
InventoryClient.configure do |config|
  # Configure API key authorization: APIKey
  config.api_key['APIKey'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['APIKey'] = 'Bearer'

  # Configure API key authorization: AccountID
  config.api_key['accountid'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['accountid'] = 'Bearer'
end

api_instance = InventoryClient::DefaultApi.new

begin
  result = api_instance.all_get
  p result
rescue InventoryClient::ApiError => e
  puts "Exception when calling DefaultApi->all_get: #{e}"
end
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**Array&lt;InventoryGroup&gt;**](InventoryGroup.md)

### Authorization

[APIKey](../README.md#APIKey), [AccountID](../README.md#AccountID)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json



# **categories_delete**
> Response categories_delete(id)



### Example
```ruby
# load the gem
require 'InventoryClient'
# setup authorization
InventoryClient.configure do |config|
  # Configure API key authorization: APIKey
  config.api_key['APIKey'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['APIKey'] = 'Bearer'

  # Configure API key authorization: AccountID
  config.api_key['accountid'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['accountid'] = 'Bearer'
end

api_instance = InventoryClient::DefaultApi.new

id = "id_example" # String | Id of category to remove


begin
  result = api_instance.categories_delete(id)
  p result
rescue InventoryClient::ApiError => e
  puts "Exception when calling DefaultApi->categories_delete: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **String**| Id of category to remove | 

### Return type

[**Response**](Response.md)

### Authorization

[APIKey](../README.md#APIKey), [AccountID](../README.md#AccountID)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json



# **categories_post**
> Array&lt;Category&gt; categories_post(opts)



### Example
```ruby
# load the gem
require 'InventoryClient'
# setup authorization
InventoryClient.configure do |config|
  # Configure API key authorization: APIKey
  config.api_key['APIKey'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['APIKey'] = 'Bearer'

  # Configure API key authorization: AccountID
  config.api_key['accountid'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['accountid'] = 'Bearer'
end

api_instance = InventoryClient::DefaultApi.new

opts = { 
  query: InventoryClient::Category.new # Category | Category to query against system
}

begin
  result = api_instance.categories_post(opts)
  p result
rescue InventoryClient::ApiError => e
  puts "Exception when calling DefaultApi->categories_post: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **query** | [**Category**](Category.md)| Category to query against system | [optional] 

### Return type

[**Array&lt;Category&gt;**](Category.md)

### Authorization

[APIKey](../README.md#APIKey), [AccountID](../README.md#AccountID)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json



# **categories_put**
> Category categories_put(id, category)



If no ID is specified a new category will be created!

### Example
```ruby
# load the gem
require 'InventoryClient'
# setup authorization
InventoryClient.configure do |config|
  # Configure API key authorization: APIKey
  config.api_key['APIKey'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['APIKey'] = 'Bearer'

  # Configure API key authorization: AccountID
  config.api_key['accountid'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['accountid'] = 'Bearer'
end

api_instance = InventoryClient::DefaultApi.new

id = "id_example" # String | category id to update.

category = InventoryClient::Category.new # Category | New category information.


begin
  result = api_instance.categories_put(id, category)
  p result
rescue InventoryClient::ApiError => e
  puts "Exception when calling DefaultApi->categories_put: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **String**| category id to update. | 
 **category** | [**Category**](Category.md)| New category information. | 

### Return type

[**Category**](Category.md)

### Authorization

[APIKey](../README.md#APIKey), [AccountID](../README.md#AccountID)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json



# **item_add_post**
> Item item_add_post(item)



### Example
```ruby
# load the gem
require 'InventoryClient'
# setup authorization
InventoryClient.configure do |config|
  # Configure API key authorization: APIKey
  config.api_key['APIKey'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['APIKey'] = 'Bearer'

  # Configure API key authorization: AccountID
  config.api_key['accountid'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['accountid'] = 'Bearer'
end

api_instance = InventoryClient::DefaultApi.new

item = InventoryClient::ItemRequest.new # ItemRequest | Item to create.


begin
  result = api_instance.item_add_post(item)
  p result
rescue InventoryClient::ApiError => e
  puts "Exception when calling DefaultApi->item_add_post: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **item** | [**ItemRequest**](ItemRequest.md)| Item to create. | 

### Return type

[**Item**](Item.md)

### Authorization

[APIKey](../README.md#APIKey), [AccountID](../README.md#AccountID)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json



# **item_addbulk_post**
> Response item_addbulk_post(items)



### Example
```ruby
# load the gem
require 'InventoryClient'
# setup authorization
InventoryClient.configure do |config|
  # Configure API key authorization: APIKey
  config.api_key['APIKey'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['APIKey'] = 'Bearer'

  # Configure API key authorization: AccountID
  config.api_key['accountid'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['accountid'] = 'Bearer'
end

api_instance = InventoryClient::DefaultApi.new

items = [InventoryClient::ItemRequest.new] # Array<ItemRequest> | Items to create.


begin
  result = api_instance.item_addbulk_post(items)
  p result
rescue InventoryClient::ApiError => e
  puts "Exception when calling DefaultApi->item_addbulk_post: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **items** | [**Array&lt;ItemRequest&gt;**](ItemRequest.md)| Items to create. | 

### Return type

[**Response**](Response.md)

### Authorization

[APIKey](../README.md#APIKey), [AccountID](../README.md#AccountID)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json



# **item_delete**
> Response item_delete(id)



### Example
```ruby
# load the gem
require 'InventoryClient'
# setup authorization
InventoryClient.configure do |config|
  # Configure API key authorization: APIKey
  config.api_key['APIKey'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['APIKey'] = 'Bearer'

  # Configure API key authorization: AccountID
  config.api_key['accountid'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['accountid'] = 'Bearer'
end

api_instance = InventoryClient::DefaultApi.new

id = "id_example" # String | item id to remove


begin
  result = api_instance.item_delete(id)
  p result
rescue InventoryClient::ApiError => e
  puts "Exception when calling DefaultApi->item_delete: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **String**| item id to remove | 

### Return type

[**Response**](Response.md)

### Authorization

[APIKey](../README.md#APIKey), [AccountID](../README.md#AccountID)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json



# **item_get**
> Item item_get(id)



### Example
```ruby
# load the gem
require 'InventoryClient'
# setup authorization
InventoryClient.configure do |config|
  # Configure API key authorization: APIKey
  config.api_key['APIKey'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['APIKey'] = 'Bearer'

  # Configure API key authorization: AccountID
  config.api_key['accountid'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['accountid'] = 'Bearer'
end

api_instance = InventoryClient::DefaultApi.new

id = "id_example" # String | Item ID to open.


begin
  result = api_instance.item_get(id)
  p result
rescue InventoryClient::ApiError => e
  puts "Exception when calling DefaultApi->item_get: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **String**| Item ID to open. | 

### Return type

[**Item**](Item.md)

### Authorization

[APIKey](../README.md#APIKey), [AccountID](../README.md#AccountID)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json



# **item_media_delete**
> Response item_media_delete(imageurl)



### Example
```ruby
# load the gem
require 'InventoryClient'
# setup authorization
InventoryClient.configure do |config|
  # Configure API key authorization: APIKey
  config.api_key['APIKey'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['APIKey'] = 'Bearer'

  # Configure API key authorization: AccountID
  config.api_key['accountid'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['accountid'] = 'Bearer'
end

api_instance = InventoryClient::DefaultApi.new

imageurl = "imageurl_example" # String | URL of image to remove


begin
  result = api_instance.item_media_delete(imageurl)
  p result
rescue InventoryClient::ApiError => e
  puts "Exception when calling DefaultApi->item_media_delete: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **imageurl** | **String**| URL of image to remove | 

### Return type

[**Response**](Response.md)

### Authorization

[APIKey](../README.md#APIKey), [AccountID](../README.md#AccountID)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json



# **item_media_post**
> String item_media_post(id, image)



This endpoint is currently in testing.

### Example
```ruby
# load the gem
require 'InventoryClient'
# setup authorization
InventoryClient.configure do |config|
  # Configure API key authorization: APIKey
  config.api_key['APIKey'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['APIKey'] = 'Bearer'

  # Configure API key authorization: AccountID
  config.api_key['accountid'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['accountid'] = 'Bearer'
end

api_instance = InventoryClient::DefaultApi.new

id = "id_example" # String | Valid item id to bind image to.

image = File.new("/path/to/file.txt") # File | Image.


begin
  result = api_instance.item_media_post(id, image)
  p result
rescue InventoryClient::ApiError => e
  puts "Exception when calling DefaultApi->item_media_post: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **String**| Valid item id to bind image to. | 
 **image** | **File**| Image. | 

### Return type

**String**

### Authorization

[APIKey](../README.md#APIKey), [AccountID](../README.md#AccountID)

### HTTP request headers

 - **Content-Type**: multipart/form-data, application/x-www-form-urlencoded
 - **Accept**: application/json



# **item_put**
> Response item_put(id, item)



### Example
```ruby
# load the gem
require 'InventoryClient'
# setup authorization
InventoryClient.configure do |config|
  # Configure API key authorization: APIKey
  config.api_key['APIKey'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['APIKey'] = 'Bearer'

  # Configure API key authorization: AccountID
  config.api_key['accountid'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['accountid'] = 'Bearer'
end

api_instance = InventoryClient::DefaultApi.new

id = "id_example" # String | item id to update.

item = InventoryClient::ItemRequest.new # ItemRequest | New item information.


begin
  result = api_instance.item_put(id, item)
  p result
rescue InventoryClient::ApiError => e
  puts "Exception when calling DefaultApi->item_put: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **String**| item id to update. | 
 **item** | [**ItemRequest**](ItemRequest.md)| New item information. | 

### Return type

[**Response**](Response.md)

### Authorization

[APIKey](../README.md#APIKey), [AccountID](../README.md#AccountID)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json



# **items_count_post**
> Float items_count_post(opts)



### Example
```ruby
# load the gem
require 'InventoryClient'
# setup authorization
InventoryClient.configure do |config|
  # Configure API key authorization: APIKey
  config.api_key['APIKey'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['APIKey'] = 'Bearer'

  # Configure API key authorization: AccountID
  config.api_key['accountid'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['accountid'] = 'Bearer'
end

api_instance = InventoryClient::DefaultApi.new

opts = { 
  minprice: 3.4, # Float | Min price of items to find
  maxprice: 3.4, # Float | Max price of items to find
  query: InventoryClient::ItemRequest.new # ItemRequest | Item to query against system.
}

begin
  result = api_instance.items_count_post(opts)
  p result
rescue InventoryClient::ApiError => e
  puts "Exception when calling DefaultApi->items_count_post: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **minprice** | **Float**| Min price of items to find | [optional] 
 **maxprice** | **Float**| Max price of items to find | [optional] 
 **query** | [**ItemRequest**](ItemRequest.md)| Item to query against system. | [optional] 

### Return type

**Float**

### Authorization

[APIKey](../README.md#APIKey), [AccountID](../README.md#AccountID)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json



# **items_post**
> Array&lt;Item&gt; items_post(opts)



### Example
```ruby
# load the gem
require 'InventoryClient'
# setup authorization
InventoryClient.configure do |config|
  # Configure API key authorization: APIKey
  config.api_key['APIKey'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['APIKey'] = 'Bearer'

  # Configure API key authorization: AccountID
  config.api_key['accountid'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['accountid'] = 'Bearer'
end

api_instance = InventoryClient::DefaultApi.new

opts = { 
  minprice: 3.4, # Float | Min price of items to find
  maxprice: 3.4, # Float | Max price of items to find
  query: InventoryClient::ItemRequest.new # ItemRequest | Item to query against system.
}

begin
  result = api_instance.items_post(opts)
  p result
rescue InventoryClient::ApiError => e
  puts "Exception when calling DefaultApi->items_post: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **minprice** | **Float**| Min price of items to find | [optional] 
 **maxprice** | **Float**| Max price of items to find | [optional] 
 **query** | [**ItemRequest**](ItemRequest.md)| Item to query against system. | [optional] 

### Return type

[**Array&lt;Item&gt;**](Item.md)

### Authorization

[APIKey](../README.md#APIKey), [AccountID](../README.md#AccountID)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json



# **orders_post**
> Array&lt;Order&gt; orders_post(opts)



### Example
```ruby
# load the gem
require 'InventoryClient'
# setup authorization
InventoryClient.configure do |config|
  # Configure API key authorization: APIKey
  config.api_key['APIKey'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['APIKey'] = 'Bearer'

  # Configure API key authorization: AccountID
  config.api_key['accountid'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['accountid'] = 'Bearer'
end

api_instance = InventoryClient::DefaultApi.new

opts = { 
  query: InventoryClient::OrderRequest.new # OrderRequest | Order to query against item invoices.
}

begin
  result = api_instance.orders_post(opts)
  p result
rescue InventoryClient::ApiError => e
  puts "Exception when calling DefaultApi->orders_post: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **query** | [**OrderRequest**](OrderRequest.md)| Order to query against item invoices. | [optional] 

### Return type

[**Array&lt;Order&gt;**](Order.md)

### Authorization

[APIKey](../README.md#APIKey), [AccountID](../README.md#AccountID)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json



# **orders_services_post**
> Array&lt;Order&gt; orders_services_post(opts)



### Example
```ruby
# load the gem
require 'InventoryClient'
# setup authorization
InventoryClient.configure do |config|
  # Configure API key authorization: APIKey
  config.api_key['APIKey'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['APIKey'] = 'Bearer'

  # Configure API key authorization: AccountID
  config.api_key['accountid'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['accountid'] = 'Bearer'
end

api_instance = InventoryClient::DefaultApi.new

opts = { 
  query: InventoryClient::OrderRequest.new # OrderRequest | Order to query against service invoices.
}

begin
  result = api_instance.orders_services_post(opts)
  p result
rescue InventoryClient::ApiError => e
  puts "Exception when calling DefaultApi->orders_services_post: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **query** | [**OrderRequest**](OrderRequest.md)| Order to query against service invoices. | [optional] 

### Return type

[**Array&lt;Order&gt;**](Order.md)

### Authorization

[APIKey](../README.md#APIKey), [AccountID](../README.md#AccountID)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json



# **query_post**
> Array&lt;Item&gt; query_post(opts)



### Example
```ruby
# load the gem
require 'InventoryClient'
# setup authorization
InventoryClient.configure do |config|
  # Configure API key authorization: APIKey
  config.api_key['APIKey'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['APIKey'] = 'Bearer'

  # Configure API key authorization: AccountID
  config.api_key['accountid'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['accountid'] = 'Bearer'
end

api_instance = InventoryClient::DefaultApi.new

opts = { 
  page: 3.4, # Float | Current page index.
  categoryid: "categoryid_example", # String | Get items under specified category id.
  sort: "sort_example", # String | Comma delimited Sort string. ie ; +ordprice. Please use number based fields only
  search: "search_example", # String | Performs a regex pattern match against the items within your account
  minprice: 3.4, # Float | Min price in hundreds (cents).
  maxprice: 3.4, # Float | Max price in hundreds (cents).
  query: InventoryClient::ItemRequest.new # ItemRequest | Custom parameters to query against system.
}

begin
  result = api_instance.query_post(opts)
  p result
rescue InventoryClient::ApiError => e
  puts "Exception when calling DefaultApi->query_post: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **Float**| Current page index. | [optional] 
 **categoryid** | **String**| Get items under specified category id. | [optional] 
 **sort** | **String**| Comma delimited Sort string. ie ; +ordprice. Please use number based fields only | [optional] 
 **search** | **String**| Performs a regex pattern match against the items within your account | [optional] 
 **minprice** | **Float**| Min price in hundreds (cents). | [optional] 
 **maxprice** | **Float**| Max price in hundreds (cents). | [optional] 
 **query** | [**ItemRequest**](ItemRequest.md)| Custom parameters to query against system. | [optional] 

### Return type

[**Array&lt;Item&gt;**](Item.md)

### Authorization

[APIKey](../README.md#APIKey), [AccountID](../README.md#AccountID)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json



# **services_delete**
> Response services_delete(id)



### Example
```ruby
# load the gem
require 'InventoryClient'
# setup authorization
InventoryClient.configure do |config|
  # Configure API key authorization: APIKey
  config.api_key['APIKey'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['APIKey'] = 'Bearer'

  # Configure API key authorization: AccountID
  config.api_key['accountid'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['accountid'] = 'Bearer'
end

api_instance = InventoryClient::DefaultApi.new

id = "id_example" # String | ID of the service to update


begin
  result = api_instance.services_delete(id)
  p result
rescue InventoryClient::ApiError => e
  puts "Exception when calling DefaultApi->services_delete: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **String**| ID of the service to update | 

### Return type

[**Response**](Response.md)

### Authorization

[APIKey](../README.md#APIKey), [AccountID](../README.md#AccountID)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json



# **services_get**
> Array&lt;Service&gt; services_get



### Example
```ruby
# load the gem
require 'InventoryClient'
# setup authorization
InventoryClient.configure do |config|
  # Configure API key authorization: APIKey
  config.api_key['APIKey'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['APIKey'] = 'Bearer'

  # Configure API key authorization: AccountID
  config.api_key['accountid'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['accountid'] = 'Bearer'
end

api_instance = InventoryClient::DefaultApi.new

begin
  result = api_instance.services_get
  p result
rescue InventoryClient::ApiError => e
  puts "Exception when calling DefaultApi->services_get: #{e}"
end
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**Array&lt;Service&gt;**](Service.md)

### Authorization

[APIKey](../README.md#APIKey), [AccountID](../README.md#AccountID)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json



# **services_open_get**
> Service services_open_get(id)



### Example
```ruby
# load the gem
require 'InventoryClient'
# setup authorization
InventoryClient.configure do |config|
  # Configure API key authorization: APIKey
  config.api_key['APIKey'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['APIKey'] = 'Bearer'

  # Configure API key authorization: AccountID
  config.api_key['accountid'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['accountid'] = 'Bearer'
end

api_instance = InventoryClient::DefaultApi.new

id = "id_example" # String | ID of service to open


begin
  result = api_instance.services_open_get(id)
  p result
rescue InventoryClient::ApiError => e
  puts "Exception when calling DefaultApi->services_open_get: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **String**| ID of service to open | 

### Return type

[**Service**](Service.md)

### Authorization

[APIKey](../README.md#APIKey), [AccountID](../README.md#AccountID)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json



# **services_post**
> Service services_post(service)



### Example
```ruby
# load the gem
require 'InventoryClient'
# setup authorization
InventoryClient.configure do |config|
  # Configure API key authorization: APIKey
  config.api_key['APIKey'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['APIKey'] = 'Bearer'

  # Configure API key authorization: AccountID
  config.api_key['accountid'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['accountid'] = 'Bearer'
end

api_instance = InventoryClient::DefaultApi.new

service = InventoryClient::ServiceRequest.new # ServiceRequest | Service to create.


begin
  result = api_instance.services_post(service)
  p result
rescue InventoryClient::ApiError => e
  puts "Exception when calling DefaultApi->services_post: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **service** | [**ServiceRequest**](ServiceRequest.md)| Service to create. | 

### Return type

[**Service**](Service.md)

### Authorization

[APIKey](../README.md#APIKey), [AccountID](../README.md#AccountID)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json



# **services_put**
> Response services_put(id, service)



### Example
```ruby
# load the gem
require 'InventoryClient'
# setup authorization
InventoryClient.configure do |config|
  # Configure API key authorization: APIKey
  config.api_key['APIKey'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['APIKey'] = 'Bearer'

  # Configure API key authorization: AccountID
  config.api_key['accountid'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['accountid'] = 'Bearer'
end

api_instance = InventoryClient::DefaultApi.new

id = "id_example" # String | ID of the service to update

service = InventoryClient::ServiceRequest.new # ServiceRequest | New service data to set.


begin
  result = api_instance.services_put(id, service)
  p result
rescue InventoryClient::ApiError => e
  puts "Exception when calling DefaultApi->services_put: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **String**| ID of the service to update | 
 **service** | [**ServiceRequest**](ServiceRequest.md)| New service data to set. | 

### Return type

[**Response**](Response.md)

### Authorization

[APIKey](../README.md#APIKey), [AccountID](../README.md#AccountID)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json



# **variation_delete**
> Response variation_delete(id)



### Example
```ruby
# load the gem
require 'InventoryClient'
# setup authorization
InventoryClient.configure do |config|
  # Configure API key authorization: APIKey
  config.api_key['APIKey'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['APIKey'] = 'Bearer'

  # Configure API key authorization: AccountID
  config.api_key['accountid'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['accountid'] = 'Bearer'
end

api_instance = InventoryClient::DefaultApi.new

id = "id_example" # String | variation id to remove


begin
  result = api_instance.variation_delete(id)
  p result
rescue InventoryClient::ApiError => e
  puts "Exception when calling DefaultApi->variation_delete: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **String**| variation id to remove | 

### Return type

[**Response**](Response.md)

### Authorization

[APIKey](../README.md#APIKey), [AccountID](../README.md#AccountID)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json



# **variation_get**
> Variation variation_get(id)



### Example
```ruby
# load the gem
require 'InventoryClient'
# setup authorization
InventoryClient.configure do |config|
  # Configure API key authorization: APIKey
  config.api_key['APIKey'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['APIKey'] = 'Bearer'

  # Configure API key authorization: AccountID
  config.api_key['accountid'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['accountid'] = 'Bearer'
end

api_instance = InventoryClient::DefaultApi.new

id = "id_example" # String | Variation ID to open.


begin
  result = api_instance.variation_get(id)
  p result
rescue InventoryClient::ApiError => e
  puts "Exception when calling DefaultApi->variation_get: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **String**| Variation ID to open. | 

### Return type

[**Variation**](Variation.md)

### Authorization

[APIKey](../README.md#APIKey), [AccountID](../README.md#AccountID)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json



# **variation_post**
> Response variation_post(id, item)



### Example
```ruby
# load the gem
require 'InventoryClient'
# setup authorization
InventoryClient.configure do |config|
  # Configure API key authorization: APIKey
  config.api_key['APIKey'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['APIKey'] = 'Bearer'

  # Configure API key authorization: AccountID
  config.api_key['accountid'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['accountid'] = 'Bearer'
end

api_instance = InventoryClient::DefaultApi.new

id = "id_example" # String | Valid item id to bind variation to.

item = InventoryClient::Variation.new # Variation | Variation information.


begin
  result = api_instance.variation_post(id, item)
  p result
rescue InventoryClient::ApiError => e
  puts "Exception when calling DefaultApi->variation_post: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **String**| Valid item id to bind variation to. | 
 **item** | [**Variation**](Variation.md)| Variation information. | 

### Return type

[**Response**](Response.md)

### Authorization

[APIKey](../README.md#APIKey), [AccountID](../README.md#AccountID)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json



# **variation_put**
> Response variation_put(id, item)



### Example
```ruby
# load the gem
require 'InventoryClient'
# setup authorization
InventoryClient.configure do |config|
  # Configure API key authorization: APIKey
  config.api_key['APIKey'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['APIKey'] = 'Bearer'

  # Configure API key authorization: AccountID
  config.api_key['accountid'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['accountid'] = 'Bearer'
end

api_instance = InventoryClient::DefaultApi.new

id = "id_example" # String | variation id to update.

item = InventoryClient::Variation.new # Variation | New variation information.


begin
  result = api_instance.variation_put(id, item)
  p result
rescue InventoryClient::ApiError => e
  puts "Exception when calling DefaultApi->variation_put: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **String**| variation id to update. | 
 **item** | [**Variation**](Variation.md)| New variation information. | 

### Return type

[**Response**](Response.md)

### Authorization

[APIKey](../README.md#APIKey), [AccountID](../README.md#AccountID)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json



# **write_delete**
> Response write_delete(opts)



### Example
```ruby
# load the gem
require 'InventoryClient'
# setup authorization
InventoryClient.configure do |config|
  # Configure API key authorization: APIKey
  config.api_key['APIKey'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['APIKey'] = 'Bearer'

  # Configure API key authorization: AccountID
  config.api_key['accountid'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['accountid'] = 'Bearer'
end

api_instance = InventoryClient::DefaultApi.new

opts = { 
  id: "id_example" # String | Will delete event attached to this serviceid
}

begin
  result = api_instance.write_delete(opts)
  p result
rescue InventoryClient::ApiError => e
  puts "Exception when calling DefaultApi->write_delete: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **String**| Will delete event attached to this serviceid | [optional] 

### Return type

[**Response**](Response.md)

### Authorization

[APIKey](../README.md#APIKey), [AccountID](../README.md#AccountID)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json



# **write_post**
> Response write_post(event_request)



Will ovveride the current event of the specified service.

### Example
```ruby
# load the gem
require 'InventoryClient'
# setup authorization
InventoryClient.configure do |config|
  # Configure API key authorization: APIKey
  config.api_key['APIKey'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['APIKey'] = 'Bearer'

  # Configure API key authorization: AccountID
  config.api_key['accountid'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['accountid'] = 'Bearer'
end

api_instance = InventoryClient::DefaultApi.new

event_request = InventoryClient::EventRequest.new # EventRequest | Event to upload


begin
  result = api_instance.write_post(event_request)
  p result
rescue InventoryClient::ApiError => e
  puts "Exception when calling DefaultApi->write_post: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **event_request** | [**EventRequest**](EventRequest.md)| Event to upload | 

### Return type

[**Response**](Response.md)

### Authorization

[APIKey](../README.md#APIKey), [AccountID](../README.md#AccountID)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json



