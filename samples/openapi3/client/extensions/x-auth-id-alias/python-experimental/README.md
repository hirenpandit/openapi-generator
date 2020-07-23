# x-auth-id-alias
This specification shows how to use x-auth-id-alias extension for API keys.

This Python package is automatically generated by the [OpenAPI Generator](https://openapi-generator.tech) project:

- API version: 1.0.0
- Package version: 1.0.0
- Build package: org.openapitools.codegen.languages.PythonClientExperimentalCodegen

## Requirements.

Python 3.4+

## Installation & Usage
### pip install

If the python package is hosted on a repository, you can install directly using:

```sh
pip install git+https://github.com/GIT_USER_ID/GIT_REPO_ID.git
```
(you may need to run `pip` with root permission: `sudo pip install git+https://github.com/GIT_USER_ID/GIT_REPO_ID.git`)

Then import the package:
```python
import x_auth_id_alias
```

### Setuptools

Install via [Setuptools](http://pypi.python.org/pypi/setuptools).

```sh
python setup.py install --user
```
(or `sudo python setup.py install` to install the package for all users)

Then import the package:
```python
import x_auth_id_alias
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```python

import time
import x_auth_id_alias
from pprint import pprint
from x_auth_id_alias.api import usage_api
# Defining the host is optional and defaults to http://petstore.swagger.io:80/v2
# See configuration.py for a list of all supported configuration parameters.
configuration = x_auth_id_alias.Configuration(
    host = "http://petstore.swagger.io:80/v2"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: api_key
configuration = x_auth_id_alias.Configuration(
    host = "http://petstore.swagger.io:80/v2",
    api_key = {
        'api_key': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key'] = 'Bearer'

# Configure API key authorization: api_key_query
configuration = x_auth_id_alias.Configuration(
    host = "http://petstore.swagger.io:80/v2",
    api_key = {
        'api_key_query': 'YOUR_API_KEY'
    }
)
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['api_key_query'] = 'Bearer'


# Enter a context with an instance of the API client
with x_auth_id_alias.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = usage_api.UsageApi(api_client)
    
    try:
        # Use any API key
        api_response = api_instance.any_key()
        pprint(api_response)
    except x_auth_id_alias.ApiException as e:
        print("Exception when calling UsageApi->any_key: %s\n" % e)
```

## Documentation for API Endpoints

All URIs are relative to *http://petstore.swagger.io:80/v2*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*UsageApi* | [**any_key**](docs/UsageApi.md#any_key) | **GET** /any | Use any API key
*UsageApi* | [**both_keys**](docs/UsageApi.md#both_keys) | **GET** /both | Use both API keys
*UsageApi* | [**key_in_header**](docs/UsageApi.md#key_in_header) | **GET** /header | Use API key in header
*UsageApi* | [**key_in_query**](docs/UsageApi.md#key_in_query) | **GET** /query | Use API key in query


## Documentation For Models



## Documentation For Authorization


## api_key

- **Type**: API key
- **API key parameter name**: X-Api-Key
- **Location**: HTTP header


## api_key_query

- **Type**: API key
- **API key parameter name**: api_key
- **Location**: URL query string


## Author




## Notes for Large OpenAPI documents
If the OpenAPI document is large, imports in x_auth_id_alias.apis and x_auth_id_alias.models may fail with a
RecursionError indicating the maximum recursion limit has been exceeded. In that case, there are a couple of solutions:

Solution 1:
Use specific imports for apis and models like:
- `from x_auth_id_alias.api.default_api import DefaultApi`
- `from x_auth_id_alias.model.pet import Pet`

Solution 1:
Before importing the package, adjust the maximum recursion limit as shown below:
```
import sys
sys.setrecursionlimit(1500)
import x_auth_id_alias
from x_auth_id_alias.apis import *
from x_auth_id_alias.models import *
```
