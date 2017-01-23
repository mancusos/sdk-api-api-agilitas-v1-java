# TransferenciasApi

All URIs are relative to *https://api-visa.sensedia.com/sandbox/visa/agillitas/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**transferenciasCadastrosPost**](TransferenciasApi.md#transferenciasCadastrosPost) | **POST** /transferencias/cadastros | Cadastro de beneficiário
[**transferenciasPost**](TransferenciasApi.md#transferenciasPost) | **POST** /transferencias | Transferência de valor


<a name="transferenciasCadastrosPost"></a>
# **transferenciasCadastrosPost**
> transferenciasCadastrosPost(beneficiario)

Cadastro de beneficiário

&lt;p&gt;Permite o cadastro de beneficiário para uma transferencia.&lt;/p&gt;

### Example
```java
// Import classes:
//import io.swagger.client.ApiClient;
//import io.swagger.client.ApiException;
//import io.swagger.client.Configuration;
//import io.swagger.client.auth.*;
//import io.swagger.client.api.TransferenciasApi;

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

TransferenciasApi apiInstance = new TransferenciasApi();
TransferenciaCadastroBenificiario beneficiario = new TransferenciaCadastroBenificiario(); // TransferenciaCadastroBenificiario | Objeto de requisição
try {
    apiInstance.transferenciasCadastrosPost(beneficiario);
} catch (ApiException e) {
    System.err.println("Exception when calling TransferenciasApi#transferenciasCadastrosPost");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **beneficiario** | [**TransferenciaCadastroBenificiario**](TransferenciaCadastroBenificiario.md)| Objeto de requisição |

### Return type

null (empty response body)

### Authorization

[access_token](../README.md#access_token), [key_id](../README.md#key_id), [client_id](../README.md#client_id)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="transferenciasPost"></a>
# **transferenciasPost**
> transferenciasPost(transferencia)

Transferência de valor

&lt;p&gt;Permite a transferência de valor entre dois cartões pré cadastrados.&lt;/p&gt;

### Example
```java
// Import classes:
//import io.swagger.client.ApiClient;
//import io.swagger.client.ApiException;
//import io.swagger.client.Configuration;
//import io.swagger.client.auth.*;
//import io.swagger.client.api.TransferenciasApi;

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

TransferenciasApi apiInstance = new TransferenciasApi();
Transferencia transferencia = new Transferencia(); // Transferencia | Objeto de requisição
try {
    apiInstance.transferenciasPost(transferencia);
} catch (ApiException e) {
    System.err.println("Exception when calling TransferenciasApi#transferenciasPost");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **transferencia** | [**Transferencia**](Transferencia.md)| Objeto de requisição |

### Return type

null (empty response body)

### Authorization

[access_token](../README.md#access_token), [key_id](../README.md#key_id), [client_id](../README.md#client_id)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

