# Com.Nvt.Celman.Api.DefaultApi

All URIs are relative to *http://localhost:9003/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**SmsSend**](DefaultApi.md#smssend) | **POST** /sms/send | Send a text message request.



## SmsSend

> SmsSendResponse SmsSend (SmsSendRequest smsSendRequest)

Send a text message request.

### Example

```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Com.Nvt.Celman.Api;
using Com.Nvt.Celman.Client;
using Com.Nvt.Celman.Model;

namespace Example
{
    public class SmsSendExample
    {
        public static void Main()
        {
            Configuration.Default.BasePath = "http://localhost:9003/api/v1";
            // Configure API key authorization: ApiKeyAuth
            Configuration.Default.AddApiKey("X-Auth-Token", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("X-Auth-Token", "Bearer");

            var apiInstance = new DefaultApi(Configuration.Default);
            var smsSendRequest = new SmsSendRequest(); // SmsSendRequest | 

            try
            {
                // Send a text message request.
                SmsSendResponse result = apiInstance.SmsSend(smsSendRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException e)
            {
                Debug.Print("Exception when calling DefaultApi.SmsSend: " + e.Message );
                Debug.Print("Status Code: "+ e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **smsSendRequest** | [**SmsSendRequest**](SmsSendRequest.md)|  | 

### Return type

[**SmsSendResponse**](SmsSendResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **0** | A response to a text message send request. |  -  |

[[Back to top]](#)
[[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)

