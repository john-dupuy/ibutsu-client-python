# ibutsu-client
A system to store and query test results

This Python package is automatically generated by the [OpenAPI Generator](https://openapi-generator.tech) project:

- API version: 1.9.0
- Package version: 1.0.8
- Build package: org.openapitools.codegen.languages.PythonClientCodegen

## Requirements.

Python 2.7 and 3.4+

## Installation & Usage
### pip install

If the python package is hosted on a repository, you can install directly using:

```sh
pip install git+https://github.com/GIT_USER_ID/GIT_REPO_ID.git
```
(you may need to run `pip` with root permission: `sudo pip install git+https://github.com/GIT_USER_ID/GIT_REPO_ID.git`)

Then import the package:
```python
import ibutsu_client
```

### Setuptools

Install via [Setuptools](http://pypi.python.org/pypi/setuptools).

```sh
python setup.py install --user
```
(or `sudo python setup.py install` to install the package for all users)

Then import the package:
```python
import ibutsu_client
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```python
from __future__ import print_function

import time
import ibutsu_client
from ibutsu_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost/api
# See configuration.py for a list of all supported configuration parameters.
configuration = ibutsu_client.Configuration(
    host = "http://localhost/api"
)



# Enter a context with an instance of the API client
with ibutsu_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = ibutsu_client.ArtifactApi(api_client)
    id = 'id_example' # str | ID of artifact to delete

    try:
        # Delete an artifact
        api_instance.delete_artifact(id)
    except ApiException as e:
        print("Exception when calling ArtifactApi->delete_artifact: %s\n" % e)
    
```

## Documentation for API Endpoints

All URIs are relative to *http://localhost/api*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*ArtifactApi* | [**delete_artifact**](docs/ArtifactApi.md#delete_artifact) | **DELETE** /artifact/{id} | Delete an artifact
*ArtifactApi* | [**download_artifact**](docs/ArtifactApi.md#download_artifact) | **GET** /artifact/{id}/download | Download an artifact
*ArtifactApi* | [**get_artifact**](docs/ArtifactApi.md#get_artifact) | **GET** /artifact/{id} | Get a single artifact
*ArtifactApi* | [**get_artifact_list**](docs/ArtifactApi.md#get_artifact_list) | **GET** /artifact | Get a (filtered) list of artifacts
*ArtifactApi* | [**upload_artifact**](docs/ArtifactApi.md#upload_artifact) | **POST** /artifact | Uploads a test run artifact
*ArtifactApi* | [**view_artifact**](docs/ArtifactApi.md#view_artifact) | **GET** /artifact/{id}/view | Stream an artifact directly to the client/browser
*GroupApi* | [**add_group**](docs/GroupApi.md#add_group) | **POST** /group | Create a new group
*GroupApi* | [**get_group**](docs/GroupApi.md#get_group) | **GET** /group/{id} | Get a group
*GroupApi* | [**get_group_list**](docs/GroupApi.md#get_group_list) | **GET** /group | Get a list of groups
*GroupApi* | [**update_group**](docs/GroupApi.md#update_group) | **PUT** /group/{id} | Update a group
*HealthApi* | [**get_database_health**](docs/HealthApi.md#get_database_health) | **GET** /health/database | Get a health report for the database
*HealthApi* | [**get_health**](docs/HealthApi.md#get_health) | **GET** /health | Get a general health report
*HealthApi* | [**get_health_info**](docs/HealthApi.md#get_health_info) | **GET** /health/info | Get information about the server
*ImportApi* | [**add_import**](docs/ImportApi.md#add_import) | **POST** /import | Import a file into Ibutsu. This can be either a JUnit XML file, or an Ibutsu archive
*ImportApi* | [**get_import**](docs/ImportApi.md#get_import) | **GET** /import/{id} | Get the status of an import
*ProjectApi* | [**add_project**](docs/ProjectApi.md#add_project) | **POST** /project | Create a project
*ProjectApi* | [**get_project**](docs/ProjectApi.md#get_project) | **GET** /project/{id} | Get a single project by ID
*ProjectApi* | [**get_project_list**](docs/ProjectApi.md#get_project_list) | **GET** /project | Get a list of projects
*ProjectApi* | [**update_project**](docs/ProjectApi.md#update_project) | **PUT** /project/{id} | Update a project
*ReportApi* | [**add_report**](docs/ReportApi.md#add_report) | **POST** /report | Create a new report
*ReportApi* | [**delete_report**](docs/ReportApi.md#delete_report) | **DELETE** /report/{id} | Delete a report
*ReportApi* | [**download_report**](docs/ReportApi.md#download_report) | **GET** /report/{id}/download/{filename} | Download a report
*ReportApi* | [**get_report**](docs/ReportApi.md#get_report) | **GET** /report/{id} | Get a report
*ReportApi* | [**get_report_list**](docs/ReportApi.md#get_report_list) | **GET** /report | Get a list of reports
*ReportApi* | [**get_report_types**](docs/ReportApi.md#get_report_types) | **GET** /report/types | Get a list of report types
*ReportApi* | [**view_report**](docs/ReportApi.md#view_report) | **GET** /report/{id}/view/{filename} | View a report
*ResultApi* | [**add_result**](docs/ResultApi.md#add_result) | **POST** /result | Create a test result
*ResultApi* | [**get_result**](docs/ResultApi.md#get_result) | **GET** /result/{id} | Get a single result
*ResultApi* | [**get_result_list**](docs/ResultApi.md#get_result_list) | **GET** /result | Get the list of results.
*ResultApi* | [**update_result**](docs/ResultApi.md#update_result) | **PUT** /result/{id} | Updates a single result
*RunApi* | [**add_run**](docs/RunApi.md#add_run) | **POST** /run | Create a run
*RunApi* | [**get_run**](docs/RunApi.md#get_run) | **GET** /run/{id} | Get a single run by ID
*RunApi* | [**get_run_list**](docs/RunApi.md#get_run_list) | **GET** /run | Get a list of the test runs
*RunApi* | [**update_run**](docs/RunApi.md#update_run) | **PUT** /run/{id} | Update a single run
*WidgetApi* | [**get_widget**](docs/WidgetApi.md#get_widget) | **GET** /widget/{id} | Generate data for a dashboard widget
*WidgetApi* | [**get_widget_types**](docs/WidgetApi.md#get_widget_types) | **GET** /widget/types | Get a list of widget types
*WidgetConfigApi* | [**add_widget_config**](docs/WidgetConfigApi.md#add_widget_config) | **POST** /widget-config | Create a widget configuration
*WidgetConfigApi* | [**delete_widget_config**](docs/WidgetConfigApi.md#delete_widget_config) | **DELETE** /widget-config/{id} | Delete a widget configuration
*WidgetConfigApi* | [**get_widget_config**](docs/WidgetConfigApi.md#get_widget_config) | **GET** /widget-config/{id} | Get a single widget configuration
*WidgetConfigApi* | [**get_widget_config_list**](docs/WidgetConfigApi.md#get_widget_config_list) | **GET** /widget-config | Get the list of widget configurations
*WidgetConfigApi* | [**update_widget_config**](docs/WidgetConfigApi.md#update_widget_config) | **PUT** /widget-config/{id} | Updates a single widget configuration


## Documentation For Models

 - [Artifact](docs/Artifact.md)
 - [ArtifactList](docs/ArtifactList.md)
 - [Group](docs/Group.md)
 - [GroupList](docs/GroupList.md)
 - [Health](docs/Health.md)
 - [HealthInfo](docs/HealthInfo.md)
 - [InlineResponse200](docs/InlineResponse200.md)
 - [ModelImport](docs/ModelImport.md)
 - [Pagination](docs/Pagination.md)
 - [Project](docs/Project.md)
 - [ProjectList](docs/ProjectList.md)
 - [Report](docs/Report.md)
 - [ReportList](docs/ReportList.md)
 - [ReportParameters](docs/ReportParameters.md)
 - [Result](docs/Result.md)
 - [ResultList](docs/ResultList.md)
 - [Run](docs/Run.md)
 - [RunList](docs/RunList.md)
 - [WidgetConfig](docs/WidgetConfig.md)
 - [WidgetConfigList](docs/WidgetConfigList.md)
 - [WidgetParam](docs/WidgetParam.md)
 - [WidgetType](docs/WidgetType.md)
 - [WidgetTypeList](docs/WidgetTypeList.md)


## Documentation For Authorization


## api_key

- **Type**: API key
- **API key parameter name**: api_key
- **Location**: HTTP header


## Author




