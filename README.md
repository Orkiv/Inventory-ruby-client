# InventoryClient

InventoryClient - the Ruby gem for the InventoryAPI

Orkiv Inventory API client 

This SDK is automatically generated by the [Swagger Codegen](https://github.com/swagger-api/swagger-codegen) project:

- API version: 1.0.0
- Package version: 1.0.0
- Build date: 2016-08-04T12:34:06.018-04:00
- Build package: class io.swagger.codegen.languages.RubyClientCodegen

## Installation

### Build a gem

To build the Ruby code into a gem:

```shell
gem build InventoryClient.gemspec
```

Then either install the gem locally:

```shell
gem install ./InventoryClient-1.0.0.gem
```
(for development, run `gem install --dev ./InventoryClient-1.0.0.gem` to install the development dependencies)

or publish the gem to a gem hosting service, e.g. [RubyGems](https://rubygems.org/).

Finally add this to the Gemfile:

    gem 'InventoryClient', '~> 1.0.0'

### Install from Git

If the Ruby gem is hosted at a git repository: https://github.com/Orkiv/Inventory-ruby-client, then add the following in the Gemfile:

    gem 'InventoryClient', :git => 'https://github.com/Orkiv/Inventory-ruby-client.git'

### Include the Ruby code directly

Include the Ruby code directly using `-I` as follows:

```shell
ruby -Ilib script.rb
```

## Getting Started

Please follow the [installation](#installation) procedure and then run the following code:
```ruby
# Load the gem
require 'InventoryClient'

# Setup authorization
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

## Documentation for API Endpoints

All URIs are relative to *https://www.orkiv.com/i/api*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*InventoryClient::DefaultApi* | [**all_get**](docs/DefaultApi.md#all_get) | **GET** /all/ | 
*InventoryClient::DefaultApi* | [**categories_delete**](docs/DefaultApi.md#categories_delete) | **DELETE** /categories/ | 
*InventoryClient::DefaultApi* | [**categories_post**](docs/DefaultApi.md#categories_post) | **POST** /categories/ | 
*InventoryClient::DefaultApi* | [**categories_put**](docs/DefaultApi.md#categories_put) | **PUT** /categories/ | 
*InventoryClient::DefaultApi* | [**item_add_post**](docs/DefaultApi.md#item_add_post) | **POST** /item/add/ | 
*InventoryClient::DefaultApi* | [**item_addbulk_post**](docs/DefaultApi.md#item_addbulk_post) | **POST** /item/addbulk/ | 
*InventoryClient::DefaultApi* | [**item_delete**](docs/DefaultApi.md#item_delete) | **DELETE** /item/ | 
*InventoryClient::DefaultApi* | [**item_put**](docs/DefaultApi.md#item_put) | **PUT** /item/ | 
*InventoryClient::DefaultApi* | [**items_count_post**](docs/DefaultApi.md#items_count_post) | **POST** /items/count/ | 
*InventoryClient::DefaultApi* | [**items_post**](docs/DefaultApi.md#items_post) | **POST** /items/ | 
*InventoryClient::DefaultApi* | [**itemsallfields_post**](docs/DefaultApi.md#itemsallfields_post) | **POST** /items/?allfields | 
*InventoryClient::DefaultApi* | [**orders_post**](docs/DefaultApi.md#orders_post) | **POST** /orders/ | 
*InventoryClient::DefaultApi* | [**query_post**](docs/DefaultApi.md#query_post) | **POST** /query/ | 
*InventoryClient::DefaultApi* | [**queryallfields_post**](docs/DefaultApi.md#queryallfields_post) | **POST** /query/?allfields | 
*InventoryClient::DefaultApi* | [**services_delete**](docs/DefaultApi.md#services_delete) | **DELETE** /services/ | 
*InventoryClient::DefaultApi* | [**services_get**](docs/DefaultApi.md#services_get) | **GET** /services/ | 
*InventoryClient::DefaultApi* | [**services_post**](docs/DefaultApi.md#services_post) | **POST** /services/ | 
*InventoryClient::DefaultApi* | [**services_put**](docs/DefaultApi.md#services_put) | **PUT** /services/ | 
*InventoryClient::DefaultApi* | [**write_delete**](docs/DefaultApi.md#write_delete) | **DELETE** /write/ | 
*InventoryClient::DefaultApi* | [**write_post**](docs/DefaultApi.md#write_post) | **POST** /write/ | 


## Documentation for Models

 - [InventoryClient::Category](docs/Category.md)
 - [InventoryClient::Dictionary](docs/Dictionary.md)
 - [InventoryClient::Error](docs/Error.md)
 - [InventoryClient::EventRequest](docs/EventRequest.md)
 - [InventoryClient::InventoryGroup](docs/InventoryGroup.md)
 - [InventoryClient::Item](docs/Item.md)
 - [InventoryClient::Order](docs/Order.md)
 - [InventoryClient::Response](docs/Response.md)
 - [InventoryClient::Service](docs/Service.md)


## Documentation for Authorization


### APIKey

- **Type**: API key
- **API key parameter name**: APIKey
- **Location**: HTTP header

### AccountID

- **Type**: API key
- **API key parameter name**: accountid
- **Location**: HTTP header

