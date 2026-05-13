# LthnApi::RunnerApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**get_v1_runner_models**](RunnerApi.md#get_v1_runner_models) | **GET** /v1/runner/models | List configured runner model routes |
| [**post_v1_runner_chat**](RunnerApi.md#post_v1_runner_chat) | **POST** /v1/runner/chat | Multi-turn chat completion |
| [**post_v1_runner_generate**](RunnerApi.md#post_v1_runner_generate) | **POST** /v1/runner/generate | Single-prompt generation |


## get_v1_runner_models

> <GetV1RunnerModels200Response> get_v1_runner_models

List configured runner model routes



### Examples

```ruby
require 'time'
require 'lthn_api'
# setup authorization
LthnApi.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = LthnApi::RunnerApi.new

begin
  # List configured runner model routes
  result = api_instance.get_v1_runner_models
  p result
rescue LthnApi::ApiError => e
  puts "Error when calling RunnerApi->get_v1_runner_models: #{e}"
end
```

#### Using the get_v1_runner_models_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GetV1RunnerModels200Response>, Integer, Hash)> get_v1_runner_models_with_http_info

```ruby
begin
  # List configured runner model routes
  data, status_code, headers = api_instance.get_v1_runner_models_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GetV1RunnerModels200Response>
rescue LthnApi::ApiError => e
  puts "Error when calling RunnerApi->get_v1_runner_models_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**GetV1RunnerModels200Response**](GetV1RunnerModels200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## post_v1_runner_chat

> <PostV1RunnerChat200Response> post_v1_runner_chat(post_v1_runner_chat_request)

Multi-turn chat completion



### Examples

```ruby
require 'time'
require 'lthn_api'
# setup authorization
LthnApi.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = LthnApi::RunnerApi.new
post_v1_runner_chat_request = LthnApi::PostV1RunnerChatRequest.new({messages: [LthnApi::PostV1RunnerChatRequestMessagesInner.new({content: 'content_example', role: 'role_example'})]}) # PostV1RunnerChatRequest | 

begin
  # Multi-turn chat completion
  result = api_instance.post_v1_runner_chat(post_v1_runner_chat_request)
  p result
rescue LthnApi::ApiError => e
  puts "Error when calling RunnerApi->post_v1_runner_chat: #{e}"
end
```

#### Using the post_v1_runner_chat_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PostV1RunnerChat200Response>, Integer, Hash)> post_v1_runner_chat_with_http_info(post_v1_runner_chat_request)

```ruby
begin
  # Multi-turn chat completion
  data, status_code, headers = api_instance.post_v1_runner_chat_with_http_info(post_v1_runner_chat_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PostV1RunnerChat200Response>
rescue LthnApi::ApiError => e
  puts "Error when calling RunnerApi->post_v1_runner_chat_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **post_v1_runner_chat_request** | [**PostV1RunnerChatRequest**](PostV1RunnerChatRequest.md) |  |  |

### Return type

[**PostV1RunnerChat200Response**](PostV1RunnerChat200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## post_v1_runner_generate

> <PostV1RunnerChat200Response> post_v1_runner_generate(post_v1_runner_generate_request)

Single-prompt generation



### Examples

```ruby
require 'time'
require 'lthn_api'
# setup authorization
LthnApi.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = LthnApi::RunnerApi.new
post_v1_runner_generate_request = LthnApi::PostV1RunnerGenerateRequest.new({prompt: 'prompt_example'}) # PostV1RunnerGenerateRequest | 

begin
  # Single-prompt generation
  result = api_instance.post_v1_runner_generate(post_v1_runner_generate_request)
  p result
rescue LthnApi::ApiError => e
  puts "Error when calling RunnerApi->post_v1_runner_generate: #{e}"
end
```

#### Using the post_v1_runner_generate_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PostV1RunnerChat200Response>, Integer, Hash)> post_v1_runner_generate_with_http_info(post_v1_runner_generate_request)

```ruby
begin
  # Single-prompt generation
  data, status_code, headers = api_instance.post_v1_runner_generate_with_http_info(post_v1_runner_generate_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PostV1RunnerChat200Response>
rescue LthnApi::ApiError => e
  puts "Error when calling RunnerApi->post_v1_runner_generate_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **post_v1_runner_generate_request** | [**PostV1RunnerGenerateRequest**](PostV1RunnerGenerateRequest.md) |  |  |

### Return type

[**PostV1RunnerChat200Response**](PostV1RunnerChat200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

