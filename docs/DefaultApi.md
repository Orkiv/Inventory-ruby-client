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
[**item_put**](DefaultApi.md#item_put) | **PUT** /item/ | 
[**items_count_post**](DefaultApi.md#items_count_post) | **POST** /items/count/ | 
[**items_post**](DefaultApi.md#items_post) | **POST** /items/ | 
[**itemsallfields_post**](DefaultApi.md#itemsallfields_post) | **POST** /items/?allfields | 
[**orders_post**](DefaultApi.md#orders_post) | **POST** /orders/ | 
[**query_post**](DefaultApi.md#query_post) | **POST** /query/ | 
[**queryallfields_post**](DefaultApi.md#queryallfields_post) | **POST** /query/?allfields | 
[**services_delete**](DefaultApi.md#services_delete) | **DELETE** /services/ | 
[**services_get**](DefaultApi.md#services_get) | **GET** /services/ | 
[**services_post**](DefaultApi.md#services_post) | **POST** /services/ | 
[**services_put**](DefaultApi.md#services_put) | **PUT** /services/ | 
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
  query: InventoryClient::Dictionary.new # Dictionary | Category to query against system
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
 **query** | [**Dictionary**](Dictionary.md)| Category to query against system | [optional] 

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

item = InventoryClient::Item.new # Item | Item to create.


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
 **item** | [**Item**](Item.md)| Item to create. | 

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

items = [InventoryClient::Item.new] # Array<Item> | Items to create.


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
 **items** | [**Array&lt;Item&gt;**](Item.md)| Items to create. | 

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

item = InventoryClient::Dictionary.new # Dictionary | New item information.


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
 **item** | [**Dictionary**](Dictionary.md)| New item information. | 

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
  query: InventoryClient::Dictionary.new # Dictionary | Item to query against system.
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
 **query** | [**Dictionary**](Dictionary.md)| Item to query against system. | [optional] 

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
  query: InventoryClient::Dictionary.new # Dictionary | Item to query against system.
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
 **query** | [**Dictionary**](Dictionary.md)| Item to query against system. | [optional] 

### Return type

[**Array&lt;Item&gt;**](Item.md)

### Authorization

[APIKey](../README.md#APIKey), [AccountID](../README.md#AccountID)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json



# **itemsallfields_post**
> Array&lt;Dictionary&gt; itemsallfields_post(opts)



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
  query: InventoryClient::Dictionary.new # Dictionary | Item to query against system.
}

begin
  result = api_instance.itemsallfields_post(opts)
  p result
rescue InventoryClient::ApiError => e
  puts "Exception when calling DefaultApi->itemsallfields_post: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **query** | [**Dictionary**](Dictionary.md)| Item to query against system. | [optional] 

### Return type

[**Array&lt;Dictionary&gt;**](Dictionary.md)

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
  query: InventoryClient::Dictionary.new # Dictionary | Order to query against system.
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
 **query** | [**Dictionary**](Dictionary.md)| Order to query against system. | [optional] 

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
  minprice: 3.4, # Float | Min price in hundreds.
  maxprice: 3.4, # Float | Max price in hudreds.
  query: InventoryClient::Dictionary.new # Dictionary | Custom parameters to query against system.
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
 **minprice** | **Float**| Min price in hundreds. | [optional] 
 **maxprice** | **Float**| Max price in hudreds. | [optional] 
 **query** | [**Dictionary**](Dictionary.md)| Custom parameters to query against system. | [optional] 

### Return type

[**Array&lt;Item&gt;**](Item.md)

### Authorization

[APIKey](../README.md#APIKey), [AccountID](../README.md#AccountID)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json



# **queryallfields_post**
> Array&lt;Dictionary&gt; queryallfields_post(opts)



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
  minprice: 3.4, # Float | Min price in hundreds.
  maxprice: 3.4, # Float | Max price in hudreds.
  query: InventoryClient::Dictionary.new # Dictionary | Custom parameters to query against system.
}

begin
  result = api_instance.queryallfields_post(opts)
  p result
rescue InventoryClient::ApiError => e
  puts "Exception when calling DefaultApi->queryallfields_post: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **Float**| Current page index. | [optional] 
 **categoryid** | **String**| Get items under specified category id. | [optional] 
 **sort** | **String**| Comma delimited Sort string. ie ; +ordprice. Please use number based fields only | [optional] 
 **search** | **String**| Performs a regex pattern match against the items within your account | [optional] 
 **minprice** | **Float**| Min price in hundreds. | [optional] 
 **maxprice** | **Float**| Max price in hudreds. | [optional] 
 **query** | [**Dictionary**](Dictionary.md)| Custom parameters to query against system. | [optional] 

### Return type

[**Array&lt;Dictionary&gt;**](Dictionary.md)

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

service = InventoryClient::Service.new # Service | Service to create.


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
 **service** | [**Service**](Service.md)| Service to create. | 

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

service = InventoryClient::Service.new # Service | New service data to set.


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
 **service** | [**Service**](Service.md)| New service data to set. | 

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



