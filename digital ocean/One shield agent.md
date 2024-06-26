## Overview

- Remote management of one panel configurations
- Collection and reporting of real-time onepanel performance and operating system metrics
- Notifications of vps events
## How it Works
- Oneshield-agent run as a companion process on a system running onepanel. 
- Its will provide gRPC and REST interface for configuration manament and metrics collection from the onepanel process and operating system. 
- Oneshield-agent enables remote interaction with onepanel using common cli tools and unlocks the ability to build sophisticated monitoring and control systems that can manage large collection of onepanel instances.
## Configuration Management
- Oneshield-agent provides an API interface for submission of updated configurations files.
- Upon receipt of a new files, its then validate the new configuration before apply it via a signal HUP to the Onepanel process.
## Collecting Metrics
- Oneshield-agent enables vps metrics to be gathered and sent to One shield to provide resource usage graphs and alerting.
- Parses access and error logs to calculate and report metrics
- Parses logs from onepanel to check for panic and critical error in onepanel process
## Event Notifications
- Oneshield-agent allows a gRPC connected control system to register a listener for a specific event. 
- The control mechanism is then invoked when agent sends an associated system signal.
- Here’s a list of currently supported events:

| Event                           | Description                                     |
| ------------------------------- | ----------------------------------------------- |
| AGENT_START_MESSAGE             | Agent process started                           |
| AGENT_STOP_MESSAGE              | Agent process stopped                           |
| ONEPANEL_FOUND_MESSAGE          | Onepanel process detected on system             |
| ONEPANEL_STOP_MESSAGE           | Onepanel process stopped                        |
| ONEPANEL_RELOAD_SUCCESS_MESSAGE | Onepanel process reloaded successfully          |
| ONEPANEL_RELOAD_FAILED_MESSAGE  | Onepanel process failed to reload               |
| CONFIG_APPLY_SUCCESS_MESSAGE    | Successfully applied new Onepanel configuration |
| CONFIG_APPLY_FAILURE_MESSAGE    | Failed to apply new Onepanel configuration      |



![[Pasted image 20240626121230.png]]