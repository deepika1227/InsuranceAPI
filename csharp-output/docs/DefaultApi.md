# IO.Swagger.Api.DefaultApi

All URIs are relative to *https://virtserver.swaggerhub.com/DEEPIKA_2/InsuranceAgentAPI/2.0.0*

Method | HTTP request | Description
------------- | ------------- | -------------
[**AgentAgentIDGet**](DefaultApi.md#agentagentidget) | **GET** /agent/{AgentID} | 
[**AgentAgentIDPatch**](DefaultApi.md#agentagentidpatch) | **PATCH** /agent/{AgentID} | 
[**AgentGet**](DefaultApi.md#agentget) | **GET** /agent | 
[**AgentPost**](DefaultApi.md#agentpost) | **POST** /agent | 
[**PolicyGet**](DefaultApi.md#policyget) | **GET** /policy | 
[**PolicyPost**](DefaultApi.md#policypost) | **POST** /policy | 
[**QuoteGet**](DefaultApi.md#quoteget) | **GET** /quote | 
[**QuotePost**](DefaultApi.md#quotepost) | **POST** /quote | 
[**QuoteQuoteIDGet**](DefaultApi.md#quotequoteidget) | **GET** /quote/{quoteID} | 
[**SubmissionGet**](DefaultApi.md#submissionget) | **GET** /submission | 
[**SubmissionPost**](DefaultApi.md#submissionpost) | **POST** /submission | 

<a name="agentagentidget"></a>
# **AgentAgentIDGet**
> AgentList AgentAgentIDGet (string agentID)



Retrieves a agent by ID

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class AgentAgentIDGetExample
    {
        public void main()
        {
            var apiInstance = new DefaultApi();
            var agentID = agentID_example;  // string | The ID of the agent to retrieve

            try
            {
                AgentList result = apiInstance.AgentAgentIDGet(agentID);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling DefaultApi.AgentAgentIDGet: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **agentID** | **string**| The ID of the agent to retrieve | 

### Return type

[**AgentList**](AgentList.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)
<a name="agentagentidpatch"></a>
# **AgentAgentIDPatch**
> AgentPatch AgentAgentIDPatch (AgentPatch agentID)



Update Agent

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class AgentAgentIDPatchExample
    {
        public void main()
        {
            var apiInstance = new DefaultApi();
            var agentID = new AgentPatch(); // AgentPatch | The ID of the agent to retrieve

            try
            {
                AgentPatch result = apiInstance.AgentAgentIDPatch(agentID);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling DefaultApi.AgentAgentIDPatch: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **agentID** | [**AgentPatch**](AgentPatch.md)| The ID of the agent to retrieve | 

### Return type

[**AgentPatch**](AgentPatch.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)
<a name="agentget"></a>
# **AgentGet**
> AgentList AgentGet (int? bodylimit = null, int? pagelimit = null)



get agent list.

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class AgentGetExample
    {
        public void main()
        {
            var apiInstance = new DefaultApi();
            var bodylimit = 56;  // int? | The amount of agents returned (optional) 
            var pagelimit = 56;  // int? | The page to return insurance information (optional) 

            try
            {
                AgentList result = apiInstance.AgentGet(bodylimit, pagelimit);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling DefaultApi.AgentGet: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **bodylimit** | **int?**| The amount of agents returned | [optional] 
 **pagelimit** | **int?**| The page to return insurance information | [optional] 

### Return type

[**AgentList**](AgentList.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)
<a name="agentpost"></a>
# **AgentPost**
> void AgentPost (Agent body)



Submits a new agent,By passing in the appropriate options, you can Add new Agent in the system

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class AgentPostExample
    {
        public void main()
        {
            var apiInstance = new DefaultApi();
            var body = new Agent(); // Agent | 

            try
            {
                apiInstance.AgentPost(body);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling DefaultApi.AgentPost: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**Agent**](Agent.md)|  | 

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json, application/xml
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)
<a name="policyget"></a>
# **PolicyGet**
> Policy PolicyGet (string policyID, string fromDate, string toDate, int? rowsPerPage, int? preFetchPages)



Retrieves a Policy by ID

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class PolicyGetExample
    {
        public void main()
        {
            var apiInstance = new DefaultApi();
            var policyID = policyID_example;  // string | The ID of the Policy to retrieve
            var fromDate = fromDate_example;  // string | Enter From Date
            var toDate = toDate_example;  // string | Enter to Date
            var rowsPerPage = 56;  // int? | Enter Rows Per Page
            var preFetchPages = 56;  // int? | pre Fetch Pages

            try
            {
                Policy result = apiInstance.PolicyGet(policyID, fromDate, toDate, rowsPerPage, preFetchPages);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling DefaultApi.PolicyGet: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **policyID** | **string**| The ID of the Policy to retrieve | 
 **fromDate** | **string**| Enter From Date | 
 **toDate** | **string**| Enter to Date | 
 **rowsPerPage** | **int?**| Enter Rows Per Page | 
 **preFetchPages** | **int?**| pre Fetch Pages | 

### Return type

[**Policy**](Policy.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)
<a name="policypost"></a>
# **PolicyPost**
> void PolicyPost (Policy body)



Submits a new policy,By passing in the appropriate options, you can Add new policy in the system

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class PolicyPostExample
    {
        public void main()
        {
            var apiInstance = new DefaultApi();
            var body = new Policy(); // Policy | 

            try
            {
                apiInstance.PolicyPost(body);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling DefaultApi.PolicyPost: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**Policy**](Policy.md)|  | 

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json, application/xml
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)
<a name="quoteget"></a>
# **QuoteGet**
> QuotePost QuoteGet (int? bodylimit = null, int? pagelimit = null)



Retrieves a list of quotes.

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class QuoteGetExample
    {
        public void main()
        {
            var apiInstance = new DefaultApi();
            var bodylimit = 56;  // int? | The amount of quotes returned (optional) 
            var pagelimit = 56;  // int? | The page to return insurance information (optional) 

            try
            {
                QuotePost result = apiInstance.QuoteGet(bodylimit, pagelimit);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling DefaultApi.QuoteGet: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **bodylimit** | **int?**| The amount of quotes returned | [optional] 
 **pagelimit** | **int?**| The page to return insurance information | [optional] 

### Return type

[**QuotePost**](QuotePost.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)
<a name="quotepost"></a>
# **QuotePost**
> void QuotePost (QuotePost body)



Submits a new quote.

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class QuotePostExample
    {
        public void main()
        {
            var apiInstance = new DefaultApi();
            var body = new QuotePost(); // QuotePost | 

            try
            {
                apiInstance.QuotePost(body);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling DefaultApi.QuotePost: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**QuotePost**](QuotePost.md)|  | 

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json, application/xml
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)
<a name="quotequoteidget"></a>
# **QuoteQuoteIDGet**
> QuotePost QuoteQuoteIDGet (string quoteID)



Retrieves a quote by ID

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class QuoteQuoteIDGetExample
    {
        public void main()
        {
            var apiInstance = new DefaultApi();
            var quoteID = quoteID_example;  // string | The ID of the quote to retrieve

            try
            {
                QuotePost result = apiInstance.QuoteQuoteIDGet(quoteID);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling DefaultApi.QuoteQuoteIDGet: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **quoteID** | **string**| The ID of the quote to retrieve | 

### Return type

[**QuotePost**](QuotePost.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)
<a name="submissionget"></a>
# **SubmissionGet**
> Submission SubmissionGet (int? bodylimit = null, int? pagelimit = null)



Retrieves a list of quotes.

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class SubmissionGetExample
    {
        public void main()
        {
            var apiInstance = new DefaultApi();
            var bodylimit = 56;  // int? | The amount of quotes returned (optional) 
            var pagelimit = 56;  // int? | The page to return insurance information (optional) 

            try
            {
                Submission result = apiInstance.SubmissionGet(bodylimit, pagelimit);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling DefaultApi.SubmissionGet: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **bodylimit** | **int?**| The amount of quotes returned | [optional] 
 **pagelimit** | **int?**| The page to return insurance information | [optional] 

### Return type

[**Submission**](Submission.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)
<a name="submissionpost"></a>
# **SubmissionPost**
> void SubmissionPost (SubmissionPost body)



Submits a new submission.

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class SubmissionPostExample
    {
        public void main()
        {
            var apiInstance = new DefaultApi();
            var body = new SubmissionPost(); // SubmissionPost | 

            try
            {
                apiInstance.SubmissionPost(body);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling DefaultApi.SubmissionPost: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**SubmissionPost**](SubmissionPost.md)|  | 

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json, application/xml
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)
