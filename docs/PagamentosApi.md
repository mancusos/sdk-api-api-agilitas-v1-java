# PagamentosApi

All URIs are relative to *https://api-visa.sensedia.com/sandbox/visa/agillitas/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**pagamentosPost**](PagamentosApi.md#pagamentosPost) | **POST** /pagamentos | Pagamento de boletos.


<a name="pagamentosPost"></a>
# **pagamentosPost**
> pagamentosPost(boleto)

Pagamento de boletos.

&lt;p&gt;Permite o pagamento de boletos.&lt;/p&gt;

### Example
```java
// Import classes:
//import io.swagger.client.ApiClient;
//import io.swagger.client.ApiException;
//import io.swagger.client.Configuration;
//import io.swagger.client.auth.*;
//import io.swagger.client.api.PagamentosApi;

ApiClient defaultClient = Configuration.getDefaultApiClient();

// Configure API key authorization: access_token
ApiKeyAuth access_token = (ApiKeyAuth) defaultClient.getAuthentication("access_token");
access_token.setApiKey("YOUR API KEY");
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//access_token.setApiKeyPrefix("Token");

// Configure API key authorization: key_id
ApiKeyAuth key_id = (ApiKeyAuth) defaultClient.getAuthentication("key_id");
key_id.setApiKey("YOUR API KEY");
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//key_id.setApiKeyPrefix("Token");

// Configure API key authorization: client_id
ApiKeyAuth client_id = (ApiKeyAuth) defaultClient.getAuthentication("client_id");
client_id.setApiKey("YOUR API KEY");
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//client_id.setApiKeyPrefix("Token");

PagamentosApi apiInstance = new PagamentosApi();
Pagamento boleto = new Pagamento(); // Pagamento | Objeto de requisição
try {
    apiInstance.pagamentosPost(boleto);
} catch (ApiException e) {
    System.err.println("Exception when calling PagamentosApi#pagamentosPost");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **boleto** | [**Pagamento**](Pagamento.md)| Objeto de requisição |

### Return type

null (empty response body)

### Authorization

[access_token](../README.md#access_token), [key_id](../README.md#key_id), [client_id](../README.md#client_id)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

