[comment]: # "Auto-generated SOAR connector documentation"
# Trend Micro Apex One

Publisher: Splunk Community  
Connector Version: 1\.0\.1  
Product Vendor: Trend Micro  
Product Name: Apex One  
Product Version Supported (regex): "\.\*"  
Minimum Product Version: 4\.9\.39220  

This app provides investigative and containment actions for Trend Micro Apex One

[comment]: # ""
[comment]: # "File: readme.md"
[comment]: # "Copyright (c) 2021 Splunk Inc."
[comment]: # ""
[comment]: # "Licensed under Apache 2.0 (https://www.apache.org/licenses/LICENSE-2.0.txt)"
[comment]: # ""
### SDK and SDK Licensing details for the app

##### PyJWT

This app uses the PyJWT module, which is licensed under the MIT License (MIT), Copyright (c) Jose
Padilla.

## Setting up Trend Micro Apex One

This app requires an API Key to access the Trend Micro Apex One environment. Please refer to the
documentation ["Obtain an Application ID and API
Key"](https://automation.trendmicro.com/apex-central/Guides/Relocate-a-Security-_001) on Apex
Central to learn how to create and access such a key.  

## Phantom Trend Micro Apex One Asset

When creating an asset for **Trend Micro Apex One** app, place the Apex Server URL (eg.
https://myapexenv.manage.trendmicro.com) into the Apex Server URL field. Next, enter the Application
ID and API Key pair into their respective input fields. After saving the asset, run the **Test
Connectivity** action under *Asset Settings* to ensure the asset has been configured correctly.


### Configuration Variables
The below configuration variables are required for this Connector to operate.  These variables are specified when configuring a Apex One asset in SOAR.

VARIABLE | REQUIRED | TYPE | DESCRIPTION
-------- | -------- | ---- | -----------
**base\_url** |  required  | string | Apex Server URL
**application\_id** |  required  | string | Apex Central Application ID
**api\_key** |  required  | password | Apex Central API Key

### Supported Actions  
[test connectivity](#action-test-connectivity) - Validate the asset configuration for connectivity using supplied configuration  
[quarantine device](#action-quarantine-device) - Quarantine an endpoint  
[unquarantine device](#action-unquarantine-device) - Unquarantine an endpoint  
[list endpoints](#action-list-endpoints) - List all the configured security agents  
[get system info](#action-get-system-info) - Get information about a security agent  

## action: 'test connectivity'
Validate the asset configuration for connectivity using supplied configuration

Type: **test**  
Read only: **True**

#### Action Parameters
No parameters are required for this action

#### Action Output
No Output  

## action: 'quarantine device'
Quarantine an endpoint

Type: **contain**  
Read only: **False**

#### Action Parameters
PARAMETER | REQUIRED | DESCRIPTION | TYPE | CONTAINS
--------- | -------- | ----------- | ---- | --------
**ip\_hostname** |  required  | Hostname/IP of endpoint to quarantine | string |  `host name`  `ip` 

#### Action Output
DATA PATH | TYPE | CONTAINS
--------- | ---- | --------
action\_result\.parameter\.ip\_hostname | string |  `host name`  `ip` 
action\_result\.data\.\*\.product | string | 
action\_result\.data\.\*\.ad\_domain | string | 
action\_result\.data\.\*\.entity\_id | string | 
action\_result\.data\.\*\.host\_name | string |  `host name` 
action\_result\.data\.\*\.folder\_path | string | 
action\_result\.data\.\*\.ip\_address\_list | string | 
action\_result\.data\.\*\.isolation\_status | string | 
action\_result\.data\.\*\.mac\_address\_list | string | 
action\_result\.data\.\*\.managing\_server\_id | string | 
action\_result\.status | string | 
action\_result\.message | string | 
action\_result\.summary | string | 
action\_result\.summary\.msg | string | 
summary\.total\_objects | numeric | 
summary\.total\_objects\_successful | numeric |   

## action: 'unquarantine device'
Unquarantine an endpoint

Type: **correct**  
Read only: **False**

#### Action Parameters
PARAMETER | REQUIRED | DESCRIPTION | TYPE | CONTAINS
--------- | -------- | ----------- | ---- | --------
**ip\_hostname** |  required  | Hostname/IP of endpoint to unquarantine | string |  `host name`  `ip` 

#### Action Output
DATA PATH | TYPE | CONTAINS
--------- | ---- | --------
action\_result\.parameter\.ip\_hostname | string |  `host name`  `ip` 
action\_result\.data\.\*\.product | string | 
action\_result\.data\.\*\.ad\_domain | string | 
action\_result\.data\.\*\.entity\_id | string | 
action\_result\.data\.\*\.host\_name | string |  `host name` 
action\_result\.data\.\*\.folder\_path | string | 
action\_result\.data\.\*\.ip\_address\_list | string | 
action\_result\.data\.\*\.isolation\_status | string | 
action\_result\.data\.\*\.mac\_address\_list | string | 
action\_result\.data\.\*\.managing\_server\_id | string | 
action\_result\.status | string | 
action\_result\.message | string | 
action\_result\.summary | string | 
action\_result\.summary\.msg | string | 
summary\.total\_objects | numeric | 
summary\.total\_objects\_successful | numeric |   

## action: 'list endpoints'
List all the configured security agents

Type: **investigate**  
Read only: **True**

#### Action Parameters
No parameters are required for this action

#### Action Output
DATA PATH | TYPE | CONTAINS
--------- | ---- | --------
action\_result\.data\.\*\.endpoints\.\*\.product | string | 
action\_result\.data\.\*\.endpoints\.\*\.ad\_domain | string | 
action\_result\.data\.\*\.endpoints\.\*\.entity\_id | string | 
action\_result\.data\.\*\.endpoints\.\*\.host\_name | string |  `host name` 
action\_result\.data\.\*\.endpoints\.\*\.folder\_path | string | 
action\_result\.data\.\*\.endpoints\.\*\.ip\_address\_list | string | 
action\_result\.data\.\*\.endpoints\.\*\.isolation\_status | string | 
action\_result\.data\.\*\.endpoints\.\*\.mac\_address\_list | string | 
action\_result\.data\.\*\.endpoints\.\*\.managing\_server\_id | string | 
action\_result\.status | string | 
action\_result\.message | string | 
action\_result\.summary | string | 
action\_result\.summary\.msg | string | 
summary\.total\_objects | numeric | 
summary\.total\_objects\_successful | numeric |   

## action: 'get system info'
Get information about a security agent

Type: **investigate**  
Read only: **True**

#### Action Parameters
PARAMETER | REQUIRED | DESCRIPTION | TYPE | CONTAINS
--------- | -------- | ----------- | ---- | --------
**ip\_hostname** |  required  | Hostname/IP address to get info of | string |  `host name`  `ip` 

#### Action Output
DATA PATH | TYPE | CONTAINS
--------- | ---- | --------
action\_result\.parameter\.ip\_hostname | string |  `host name`  `ip` 
action\_result\.data\.\*\.product | string | 
action\_result\.data\.\*\.ad\_domain | string | 
action\_result\.data\.\*\.entity\_id | string | 
action\_result\.data\.\*\.host\_name | string |  `host name` 
action\_result\.data\.\*\.folder\_path | string | 
action\_result\.data\.\*\.ip\_address\_list | string | 
action\_result\.data\.\*\.isolation\_status | string | 
action\_result\.data\.\*\.mac\_address\_list | string | 
action\_result\.data\.\*\.managing\_server\_id | string | 
action\_result\.status | string | 
action\_result\.message | string | 
action\_result\.summary | string | 
action\_result\.summary\.msg | string | 
summary\.total\_objects | numeric | 
summary\.total\_objects\_successful | numeric | 