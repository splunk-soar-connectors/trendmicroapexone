# Trend Micro Apex One

Publisher: Splunk Community \
Connector Version: 1.0.3 \
Product Vendor: Trend Micro \
Product Name: Apex One \
Minimum Product Version: 5.3.0

This app provides investigative and containment actions for Trend Micro Apex One

### Configuration variables

This table lists the configuration variables required to operate Trend Micro Apex One. These variables are specified when configuring a Apex One asset in Splunk SOAR.

VARIABLE | REQUIRED | TYPE | DESCRIPTION
-------- | -------- | ---- | -----------
**base_url** | required | string | Apex Server URL |
**application_id** | required | string | Apex Central Application ID |
**api_key** | required | password | Apex Central API Key |

### Supported Actions

[test connectivity](#action-test-connectivity) - Validate the asset configuration for connectivity using supplied configuration \
[quarantine device](#action-quarantine-device) - Quarantine an endpoint \
[unquarantine device](#action-unquarantine-device) - Unquarantine an endpoint \
[list endpoints](#action-list-endpoints) - List all the configured security agents \
[get system info](#action-get-system-info) - Get information about a security agent

## action: 'test connectivity'

Validate the asset configuration for connectivity using supplied configuration

Type: **test** \
Read only: **True**

#### Action Parameters

No parameters are required for this action

#### Action Output

No Output

## action: 'quarantine device'

Quarantine an endpoint

Type: **contain** \
Read only: **False**

#### Action Parameters

PARAMETER | REQUIRED | DESCRIPTION | TYPE | CONTAINS
--------- | -------- | ----------- | ---- | --------
**ip_hostname** | required | Hostname/IP of endpoint to quarantine | string | `host name` `ip` |

#### Action Output

DATA PATH | TYPE | CONTAINS | EXAMPLE VALUES
--------- | ---- | -------- | --------------
action_result.parameter.ip_hostname | string | `host name` `ip` | |
action_result.data.\*.product | string | | |
action_result.data.\*.ad_domain | string | | |
action_result.data.\*.entity_id | string | | |
action_result.data.\*.host_name | string | `host name` | |
action_result.data.\*.folder_path | string | | |
action_result.data.\*.ip_address_list | string | | |
action_result.data.\*.isolation_status | string | | |
action_result.data.\*.mac_address_list | string | | |
action_result.data.\*.managing_server_id | string | | |
action_result.status | string | | success failed |
action_result.message | string | | |
action_result.summary | string | | |
action_result.summary.msg | string | | |
summary.total_objects | numeric | | 1 |
summary.total_objects_successful | numeric | | 1 |

## action: 'unquarantine device'

Unquarantine an endpoint

Type: **correct** \
Read only: **False**

#### Action Parameters

PARAMETER | REQUIRED | DESCRIPTION | TYPE | CONTAINS
--------- | -------- | ----------- | ---- | --------
**ip_hostname** | required | Hostname/IP of endpoint to unquarantine | string | `host name` `ip` |

#### Action Output

DATA PATH | TYPE | CONTAINS | EXAMPLE VALUES
--------- | ---- | -------- | --------------
action_result.parameter.ip_hostname | string | `host name` `ip` | |
action_result.data.\*.product | string | | |
action_result.data.\*.ad_domain | string | | |
action_result.data.\*.entity_id | string | | |
action_result.data.\*.host_name | string | `host name` | |
action_result.data.\*.folder_path | string | | |
action_result.data.\*.ip_address_list | string | | |
action_result.data.\*.isolation_status | string | | |
action_result.data.\*.mac_address_list | string | | |
action_result.data.\*.managing_server_id | string | | |
action_result.status | string | | success failed |
action_result.message | string | | |
action_result.summary | string | | |
action_result.summary.msg | string | | |
summary.total_objects | numeric | | 1 |
summary.total_objects_successful | numeric | | 1 |

## action: 'list endpoints'

List all the configured security agents

Type: **investigate** \
Read only: **True**

#### Action Parameters

No parameters are required for this action

#### Action Output

DATA PATH | TYPE | CONTAINS | EXAMPLE VALUES
--------- | ---- | -------- | --------------
action_result.data.\*.endpoints.\*.product | string | | |
action_result.data.\*.endpoints.\*.ad_domain | string | | |
action_result.data.\*.endpoints.\*.entity_id | string | | |
action_result.data.\*.endpoints.\*.host_name | string | `host name` | |
action_result.data.\*.endpoints.\*.folder_path | string | | |
action_result.data.\*.endpoints.\*.ip_address_list | string | | |
action_result.data.\*.endpoints.\*.isolation_status | string | | |
action_result.data.\*.endpoints.\*.mac_address_list | string | | |
action_result.data.\*.endpoints.\*.managing_server_id | string | | |
action_result.status | string | | success failed |
action_result.message | string | | |
action_result.summary | string | | |
action_result.summary.msg | string | | |
summary.total_objects | numeric | | 1 |
summary.total_objects_successful | numeric | | 1 |

## action: 'get system info'

Get information about a security agent

Type: **investigate** \
Read only: **True**

#### Action Parameters

PARAMETER | REQUIRED | DESCRIPTION | TYPE | CONTAINS
--------- | -------- | ----------- | ---- | --------
**ip_hostname** | required | Hostname/IP address to get info of | string | `host name` `ip` |

#### Action Output

DATA PATH | TYPE | CONTAINS | EXAMPLE VALUES
--------- | ---- | -------- | --------------
action_result.parameter.ip_hostname | string | `host name` `ip` | |
action_result.data.\*.product | string | | |
action_result.data.\*.ad_domain | string | | |
action_result.data.\*.entity_id | string | | |
action_result.data.\*.host_name | string | `host name` | |
action_result.data.\*.folder_path | string | | |
action_result.data.\*.ip_address_list | string | | |
action_result.data.\*.isolation_status | string | | |
action_result.data.\*.mac_address_list | string | | |
action_result.data.\*.managing_server_id | string | | |
action_result.status | string | | success failed |
action_result.message | string | | |
action_result.summary | string | | |
action_result.summary.msg | string | | |
summary.total_objects | numeric | | 1 |
summary.total_objects_successful | numeric | | 1 |

______________________________________________________________________

Auto-generated Splunk SOAR Connector documentation.

Copyright 2025 Splunk Inc.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing,
software distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and limitations under the License.
