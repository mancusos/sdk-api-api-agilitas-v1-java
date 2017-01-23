# CartoesApi

All URIs are relative to *https://api-visa.sensedia.com/sandbox/visa/agillitas/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**cartoesGet**](CartoesApi.md#cartoesGet) | **GET** /cartoes | Obtém o número de identificação (Proxy) de um cartão
[**cartoesIdCartaoExtratoGet**](CartoesApi.md#cartoesIdCartaoExtratoGet) | **GET** /cartoes/{idCartao}/extrato | Extrato do cartão
[**cartoesIdCartaoPortadorGet**](CartoesApi.md#cartoesIdCartaoPortadorGet) | **GET** /cartoes/{idCartao}/portador | Informações do portador do cartão
[**cartoesIdCartaoSaldoGet**](CartoesApi.md#cartoesIdCartaoSaldoGet) | **GET** /cartoes/{idCartao}/saldo | Saldo do cartão
[**cartoesIdCartaoSaldoPut**](CartoesApi.md#cartoesIdCartaoSaldoPut) | **PUT** /cartoes/{idCartao}/saldo | Credita ou debita valor da conta de um cartão.
[**cartoesIdCartaoStatusGet**](CartoesApi.md#cartoesIdCartaoStatusGet) | **GET** /cartoes/{idCartao}/status | Status do cartão
[**cartoesIdCartaoStatusPut**](CartoesApi.md#cartoesIdCartaoStatusPut) | **PUT** /cartoes/{idCartao}/status | Altera status do cartão
[**cartoesPost**](CartoesApi.md#cartoesPost) | **POST** /cartoes | Requisita um cartão de debito


<a name="cartoesGet"></a>
# **cartoesGet**
> CartaoDisponivel cartoesGet(tipoCartao)

Obtém o número de identificação (Proxy) de um cartão

&lt;p&gt;Permite a verificação de disponibilidade de cartão e qual o número de identificação (Proxy) para posterior requisição.&lt;/p&gt;&lt;br/&gt;&lt;p class&#x3D;&#39;obs obs-danger&#39;&gt; Este recurso só poderá ser utilizado em produção mediante aprovação.&lt;/p&gt;

### Example
```java
// Import classes:
//import io.swagger.client.ApiClient;
//import io.swagger.client.ApiException;
//import io.swagger.client.Configuration;
//import io.swagger.client.auth.*;
//import io.swagger.client.api.CartoesApi;

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

CartoesApi apiInstance = new CartoesApi();
String tipoCartao = "fisico"; // String | Identifica qual o tipo do cartão, físico ou virtual.
try {
    CartaoDisponivel result = apiInstance.cartoesGet(tipoCartao);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling CartoesApi#cartoesGet");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **tipoCartao** | **String**| Identifica qual o tipo do cartão, físico ou virtual. | [default to fisico] [enum: fisico, virtual]

### Return type

[**CartaoDisponivel**](CartaoDisponivel.md)

### Authorization

[access_token](../README.md#access_token), [key_id](../README.md#key_id), [client_id](../README.md#client_id)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="cartoesIdCartaoExtratoGet"></a>
# **cartoesIdCartaoExtratoGet**
> ExtratoResponse cartoesIdCartaoExtratoGet(idCartao, dataInicial, dataFinal)

Extrato do cartão

&lt;p&gt;Permite a consulta dos movimentos por período, de um determinado cartão. A janela máxima de observação é de 30 dias, e as datas inicial e final de observação pode ser configuradas, conforme necessidade.&lt;/p&gt;

### Example
```java
// Import classes:
//import io.swagger.client.ApiClient;
//import io.swagger.client.ApiException;
//import io.swagger.client.Configuration;
//import io.swagger.client.auth.*;
//import io.swagger.client.api.CartoesApi;

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

CartoesApi apiInstance = new CartoesApi();
String idCartao = "idCartao_example"; // String | Número identificador referente ao proxy localizado no verso do cartão.
String dataInicial = "dataInicial_example"; // String | Data inicial para a consulta.
String dataFinal = "dataFinal_example"; // String | Data final para a consulta.
try {
    ExtratoResponse result = apiInstance.cartoesIdCartaoExtratoGet(idCartao, dataInicial, dataFinal);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling CartoesApi#cartoesIdCartaoExtratoGet");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **idCartao** | **String**| Número identificador referente ao proxy localizado no verso do cartão. |
 **dataInicial** | **String**| Data inicial para a consulta. |
 **dataFinal** | **String**| Data final para a consulta. |

### Return type

[**ExtratoResponse**](ExtratoResponse.md)

### Authorization

[access_token](../README.md#access_token), [key_id](../README.md#key_id), [client_id](../README.md#client_id)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="cartoesIdCartaoPortadorGet"></a>
# **cartoesIdCartaoPortadorGet**
> PortadorResponse cartoesIdCartaoPortadorGet(idCartao)

Informações do portador do cartão

&lt;p&gt;Permite a consulta de informações cadastrais de um determinado portador de cartão.&lt;/p&gt;

### Example
```java
// Import classes:
//import io.swagger.client.ApiClient;
//import io.swagger.client.ApiException;
//import io.swagger.client.Configuration;
//import io.swagger.client.auth.*;
//import io.swagger.client.api.CartoesApi;

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

CartoesApi apiInstance = new CartoesApi();
String idCartao = "idCartao_example"; // String | Número identificador referente ao proxy localizado no verso do cartão.
try {
    PortadorResponse result = apiInstance.cartoesIdCartaoPortadorGet(idCartao);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling CartoesApi#cartoesIdCartaoPortadorGet");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **idCartao** | **String**| Número identificador referente ao proxy localizado no verso do cartão. |

### Return type

[**PortadorResponse**](PortadorResponse.md)

### Authorization

[access_token](../README.md#access_token), [key_id](../README.md#key_id), [client_id](../README.md#client_id)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="cartoesIdCartaoSaldoGet"></a>
# **cartoesIdCartaoSaldoGet**
> Saldo cartoesIdCartaoSaldoGet(idCartao)

Saldo do cartão

&lt;p&gt;Permite a consulta do saldo disponível de um determinado cartão.&lt;/p&gt;

### Example
```java
// Import classes:
//import io.swagger.client.ApiClient;
//import io.swagger.client.ApiException;
//import io.swagger.client.Configuration;
//import io.swagger.client.auth.*;
//import io.swagger.client.api.CartoesApi;

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

CartoesApi apiInstance = new CartoesApi();
String idCartao = "idCartao_example"; // String | Número identificador referente ao proxy localizado no verso do cartão.
try {
    Saldo result = apiInstance.cartoesIdCartaoSaldoGet(idCartao);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling CartoesApi#cartoesIdCartaoSaldoGet");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **idCartao** | **String**| Número identificador referente ao proxy localizado no verso do cartão. |

### Return type

[**Saldo**](Saldo.md)

### Authorization

[access_token](../README.md#access_token), [key_id](../README.md#key_id), [client_id](../README.md#client_id)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="cartoesIdCartaoSaldoPut"></a>
# **cartoesIdCartaoSaldoPut**
> cartoesIdCartaoSaldoPut(idCartao, saldo)

Credita ou debita valor da conta de um cartão.

&lt;p&gt;Permite creditar ou debitar um valor especifico em um determinado cartão.&lt;/p&gt;&lt;br/&gt;&lt;p class&#x3D;&#39;obs obs-danger&#39;&gt;Este recurso deve ser utilizado somente pelo reseller e quando o credito do cartão for de responsabilidade e propriedade do Reseller.&lt;/p&gt;

### Example
```java
// Import classes:
//import io.swagger.client.ApiClient;
//import io.swagger.client.ApiException;
//import io.swagger.client.Configuration;
//import io.swagger.client.auth.*;
//import io.swagger.client.api.CartoesApi;

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

CartoesApi apiInstance = new CartoesApi();
String idCartao = "idCartao_example"; // String | Número identificador referente ao proxy localizado no verso do cartão.
SetSaldo saldo = new SetSaldo(); // SetSaldo | Objeto de requisição
try {
    apiInstance.cartoesIdCartaoSaldoPut(idCartao, saldo);
} catch (ApiException e) {
    System.err.println("Exception when calling CartoesApi#cartoesIdCartaoSaldoPut");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **idCartao** | **String**| Número identificador referente ao proxy localizado no verso do cartão. |
 **saldo** | [**SetSaldo**](SetSaldo.md)| Objeto de requisição |

### Return type

null (empty response body)

### Authorization

[access_token](../README.md#access_token), [key_id](../README.md#key_id), [client_id](../README.md#client_id)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="cartoesIdCartaoStatusGet"></a>
# **cartoesIdCartaoStatusGet**
> StatusCartaoResponse cartoesIdCartaoStatusGet(idCartao)

Status do cartão

&lt;p&gt;Permite a consulta do status de um determinado cartão. O status do cartão nos permite saber se o cartão esta ativo, bloqueado , desbloqueado ou cancelado.&lt;/p&gt;

### Example
```java
// Import classes:
//import io.swagger.client.ApiClient;
//import io.swagger.client.ApiException;
//import io.swagger.client.Configuration;
//import io.swagger.client.auth.*;
//import io.swagger.client.api.CartoesApi;

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

CartoesApi apiInstance = new CartoesApi();
String idCartao = "idCartao_example"; // String | Número identificador referente ao proxy localizado no verso do cartão.
try {
    StatusCartaoResponse result = apiInstance.cartoesIdCartaoStatusGet(idCartao);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling CartoesApi#cartoesIdCartaoStatusGet");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **idCartao** | **String**| Número identificador referente ao proxy localizado no verso do cartão. |

### Return type

[**StatusCartaoResponse**](StatusCartaoResponse.md)

### Authorization

[access_token](../README.md#access_token), [key_id](../README.md#key_id), [client_id](../README.md#client_id)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="cartoesIdCartaoStatusPut"></a>
# **cartoesIdCartaoStatusPut**
> cartoesIdCartaoStatusPut(idCartao, status)

Altera status do cartão

&lt;p&gt;Permite o bloqueio e desbloqueio de um determinado cartão.&lt;/p&gt;

### Example
```java
// Import classes:
//import io.swagger.client.ApiClient;
//import io.swagger.client.ApiException;
//import io.swagger.client.Configuration;
//import io.swagger.client.auth.*;
//import io.swagger.client.api.CartoesApi;

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

CartoesApi apiInstance = new CartoesApi();
String idCartao = "idCartao_example"; // String | Número identificador referente ao proxy localizado no verso do cartão.
SetCardStatus status = new SetCardStatus(); // SetCardStatus | Objeto de requisição
try {
    apiInstance.cartoesIdCartaoStatusPut(idCartao, status);
} catch (ApiException e) {
    System.err.println("Exception when calling CartoesApi#cartoesIdCartaoStatusPut");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **idCartao** | **String**| Número identificador referente ao proxy localizado no verso do cartão. |
 **status** | [**SetCardStatus**](SetCardStatus.md)| Objeto de requisição |

### Return type

null (empty response body)

### Authorization

[access_token](../README.md#access_token), [key_id](../README.md#key_id), [client_id](../README.md#client_id)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="cartoesPost"></a>
# **cartoesPost**
> cartoesPost(cartao)

Requisita um cartão de debito

&lt;p&gt;Permite a carga de um valor especifico a um determinado cartão.&lt;/p&gt;&lt;br/&gt;&lt;p class&#x3D;&#39;obs obs-danger&#39;&gt;Este recurso deve ser utilizado somente pelo reseller e com fundo disponível na conta e ainda dependente de aprovação pelo agente financeiro&lt;/p&gt; 

### Example
```java
// Import classes:
//import io.swagger.client.ApiClient;
//import io.swagger.client.ApiException;
//import io.swagger.client.Configuration;
//import io.swagger.client.auth.*;
//import io.swagger.client.api.CartoesApi;

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

CartoesApi apiInstance = new CartoesApi();
SetNovoCartao cartao = new SetNovoCartao(); // SetNovoCartao | Objeto de requisição
try {
    apiInstance.cartoesPost(cartao);
} catch (ApiException e) {
    System.err.println("Exception when calling CartoesApi#cartoesPost");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **cartao** | [**SetNovoCartao**](SetNovoCartao.md)| Objeto de requisição |

### Return type

null (empty response body)

### Authorization

[access_token](../README.md#access_token), [key_id](../README.md#key_id), [client_id](../README.md#client_id)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

