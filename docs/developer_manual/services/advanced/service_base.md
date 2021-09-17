# *ServiceBase* class
All service created for Assemblyline must inherit from the `ServiceBase` class which can be imported from `assemblyline_v4_service.common.base`. In this section we will go through the different methods and variables available to you in the `ServiceBase` class.


You can view the source for the class here: [ServiceBase class source](https://github.com/CybercentreCanada/assemblyline-v4-service/blob/master/assemblyline_v4_service/common/base.py)

## Class variables
The `ServiceBase` base class includes many instance variables which can be used to access service related information.

The following tables describes all of the variables of the `ServiceBase` class.

| Variable Name | Description |
|:---|:---|
| config | Reference to the service parameters containing values updated by the user for service configuration. |
| log | Reference to the logger. |
| service_attributes | Service attributes from the [service manifest](../service_manifest). |
| working_directory | Returns the directory path which the service can use to temporarily store files during each task execution. |

## Class functions
This is the list of all the functions that you can override in your service. They are explain in order of important and the likelihood at which you will override them.

### execute()

!!! important "This is where your service processing code lives!"

The `execute` function is called every time the service receives a new file to scan. To this function, a single [Request](../request) object is provided as an input which provides the service all the information available about the file which was requested for scanning.

It is inside this function that you will create a [Result](../result) objects to send your scan results back to the system for storage and display in the user interface. This has to be done before the end of the function execution. Make sure you go through the [tips on writing good results](../result#tips-on-writing-good-results) before starting to built your service.

### get_tool_version()
The purpose of the `get_tool_version` function is to the return a string indicating the version of the tools used by the service or a hash of the signatures it uses. The tool version should be updated to reflect changes in the service tools or signatures, so that Assemblyline can rescan files on the new service version if they are submitted again.

### start()
The `start` function is called when the Assemblyline service is initiated and should be used to prepare your service for task execution.

### get_api_interface()
The purpose of the `get_api_interface` function is to give the service direct access to the [service server](../../core/infrastructure/#core-components) component to perform API request to find out if a file or a tag is meant to be safelisted.

!!! warning
    By using this function, your service will not work using the `run_service_once` command and will be completely tied to the [service server](../../core/infrastructure/#core-components) API.

### stop()
The `stop` function is called when the Assemblyline service is stopped and should be used to cleanup your service.