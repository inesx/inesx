# swagger_client.DefaultApi

All URIs are relative to *https://westus.api.cognitive.microsoft.com/text/analytics/v2.0*

Method | HTTP request | Description
------------- | ------------- | -------------
[**56f30ceeeda5650db055a3c6**](DefaultApi.md#56f30ceeeda5650db055a3c6) | **POST** /keyPhrases | Key Phrases
[**56f30ceeeda5650db055a3c7**](DefaultApi.md#56f30ceeeda5650db055a3c7) | **POST** /languages | Detect Language
[**56f30ceeeda5650db055a3c9**](DefaultApi.md#56f30ceeeda5650db055a3c9) | **POST** /sentiment | Sentiment
[**5ac4251d5b4ccd1554da7634**](DefaultApi.md#5ac4251d5b4ccd1554da7634) | **POST** /entities | Entities


# **56f30ceeeda5650db055a3c6**
> KeyPhraseBatchResultV2 56f30ceeeda5650db055a3c6(multi_language_batch_input_v2=multi_language_batch_input_v2)

Key Phrases

The API returns a list of strings denoting the key talking points in the input text. See the <a href=\"https://docs.microsoft.com/en-us/azure/cognitive-services/text-analytics/text-analytics-supported-languages\">Supported languages in Text Analytics API</a> for the list of enabled languages.

### Example
```python
from __future__ import print_function
import time
import swagger_client
from swagger_client.rest import ApiException
from pprint import pprint

# Configure API key authorization: apiKeyHeader
configuration = swagger_client.Configuration()
configuration.api_key['Ocp-Apim-Subscription-Key'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['Ocp-Apim-Subscription-Key'] = 'Bearer'
# Configure API key authorization: apiKeyQuery
configuration = swagger_client.Configuration()
configuration.api_key['subscription-key'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['subscription-key'] = 'Bearer'

# create an instance of the API class
api_instance = swagger_client.DefaultApi(swagger_client.ApiClient(configuration))
multi_language_batch_input_v2 = swagger_client.MultiLanguageBatchInputV2() # MultiLanguageBatchInputV2 | Collection of documents to analyze. Documents can now contain a language field to indicate the text language (optional)

try:
    # Key Phrases
    api_response = api_instance.56f30ceeeda5650db055a3c6(multi_language_batch_input_v2=multi_language_batch_input_v2)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling DefaultApi->56f30ceeeda5650db055a3c6: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **multi_language_batch_input_v2** | [**MultiLanguageBatchInputV2**](MultiLanguageBatchInputV2.md)| Collection of documents to analyze. Documents can now contain a language field to indicate the text language | [optional] 

### Return type

[**KeyPhraseBatchResultV2**](KeyPhraseBatchResultV2.md)

### Authorization

[apiKeyHeader](../README.md#apiKeyHeader), [apiKeyQuery](../README.md#apiKeyQuery)

### HTTP request headers

 - **Content-Type**: application/json, text/json
 - **Accept**: application/json, text/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **56f30ceeeda5650db055a3c7**
> LanguageBatchResultV2 56f30ceeeda5650db055a3c7(batch_input_v2=batch_input_v2)

Detect Language

The API returns the detected language and a numeric score between 0 and 1. Scores close to 1 indicate 100% certainty that the identified language is true. A total of 120 languages are supported.

### Example
```python
from __future__ import print_function
import time
import swagger_client
from swagger_client.rest import ApiException
from pprint import pprint

# Configure API key authorization: apiKeyHeader
configuration = swagger_client.Configuration()
configuration.api_key['Ocp-Apim-Subscription-Key'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['Ocp-Apim-Subscription-Key'] = 'Bearer'
# Configure API key authorization: apiKeyQuery
configuration = swagger_client.Configuration()
configuration.api_key['subscription-key'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['subscription-key'] = 'Bearer'

# create an instance of the API class
api_instance = swagger_client.DefaultApi(swagger_client.ApiClient(configuration))
batch_input_v2 = swagger_client.BatchInputV2() # BatchInputV2 | Collection of documents to analyze. (optional)

try:
    # Detect Language
    api_response = api_instance.56f30ceeeda5650db055a3c7(batch_input_v2=batch_input_v2)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling DefaultApi->56f30ceeeda5650db055a3c7: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **batch_input_v2** | [**BatchInputV2**](BatchInputV2.md)| Collection of documents to analyze. | [optional] 

### Return type

[**LanguageBatchResultV2**](LanguageBatchResultV2.md)

### Authorization

[apiKeyHeader](../README.md#apiKeyHeader), [apiKeyQuery](../README.md#apiKeyQuery)

### HTTP request headers

 - **Content-Type**: application/json, text/json
 - **Accept**: application/json, text/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **56f30ceeeda5650db055a3c9**
> SentimentBatchResultV2 56f30ceeeda5650db055a3c9(multi_language_batch_input_v2=multi_language_batch_input_v2)

Sentiment

The API returns a numeric score between 0 and 1. Scores close to 1 indicate positive sentiment, while scores close to 0 indicate negative sentiment. A score of 0.5 indicates the lack of sentiment (e.g. a factoid statement). See the <a href=\"https://docs.microsoft.com/en-us/azure/cognitive-services/text-analytics/text-analytics-supported-languages\">Supported languages in Text Analytics API</a> for the list of enabled languages.

### Example
```python
from __future__ import print_function
import time
import swagger_client
from swagger_client.rest import ApiException
from pprint import pprint

# Configure API key authorization: apiKeyHeader
configuration = swagger_client.Configuration()
configuration.api_key['Ocp-Apim-Subscription-Key'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['Ocp-Apim-Subscription-Key'] = 'Bearer'
# Configure API key authorization: apiKeyQuery
configuration = swagger_client.Configuration()
configuration.api_key['subscription-key'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['subscription-key'] = 'Bearer'

# create an instance of the API class
api_instance = swagger_client.DefaultApi(swagger_client.ApiClient(configuration))
multi_language_batch_input_v2 = swagger_client.MultiLanguageBatchInputV2() # MultiLanguageBatchInputV2 | Collection of documents to analyze. (optional)

try:
    # Sentiment
    api_response = api_instance.56f30ceeeda5650db055a3c9(multi_language_batch_input_v2=multi_language_batch_input_v2)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling DefaultApi->56f30ceeeda5650db055a3c9: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **multi_language_batch_input_v2** | [**MultiLanguageBatchInputV2**](MultiLanguageBatchInputV2.md)| Collection of documents to analyze. | [optional] 

### Return type

[**SentimentBatchResultV2**](SentimentBatchResultV2.md)

### Authorization

[apiKeyHeader](../README.md#apiKeyHeader), [apiKeyQuery](../README.md#apiKeyQuery)

### HTTP request headers

 - **Content-Type**: application/json, text/json
 - **Accept**: application/json, text/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **5ac4251d5b4ccd1554da7634**
> EntitiesBatchResultV2 5ac4251d5b4ccd1554da7634(multi_language_batch_input_v2=multi_language_batch_input_v2)

Entities

The API returns a list of recognized entities in a given document. To get even more information on each recognized entity we recommend using the Bing Entity Search API by querying for the recognized entities names. See the <a href=\"https://docs.microsoft.com/en-us/azure/cognitive-services/text-analytics/text-analytics-supported-languages\">Supported languages in Text Analytics API</a> for the list of enabled languages.

### Example
```python
from __future__ import print_function
import time
import swagger_client
from swagger_client.rest import ApiException
from pprint import pprint

# Configure API key authorization: apiKeyHeader
configuration = swagger_client.Configuration()
configuration.api_key['Ocp-Apim-Subscription-Key'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['Ocp-Apim-Subscription-Key'] = 'Bearer'
# Configure API key authorization: apiKeyQuery
configuration = swagger_client.Configuration()
configuration.api_key['subscription-key'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['subscription-key'] = 'Bearer'

# create an instance of the API class
api_instance = swagger_client.DefaultApi(swagger_client.ApiClient(configuration))
multi_language_batch_input_v2 = swagger_client.MultiLanguageBatchInputV2() # MultiLanguageBatchInputV2 | Collection of documents to analyze. (optional)

try:
    # Entities
    api_response = api_instance.5ac4251d5b4ccd1554da7634(multi_language_batch_input_v2=multi_language_batch_input_v2)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling DefaultApi->5ac4251d5b4ccd1554da7634: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **multi_language_batch_input_v2** | [**MultiLanguageBatchInputV2**](MultiLanguageBatchInputV2.md)| Collection of documents to analyze. | [optional] 

### Return type

[**EntitiesBatchResultV2**](EntitiesBatchResultV2.md)

### Authorization

[apiKeyHeader](../README.md#apiKeyHeader), [apiKeyQuery](../README.md#apiKeyQuery)

### HTTP request headers

 - **Content-Type**: application/json, text/json
 - **Accept**: application/json, text/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

