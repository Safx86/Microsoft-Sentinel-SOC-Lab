### Microsoft Sentinel SOC Lab - Deployment & Setup
Overview
This document covers the deployment and configuration of my Microsoft Sentinel SOC lab before beginning the security investigation exercises.

It also documents the configuration challenges I encountered during deployment and how I worked through them.

### Azure Environment
The lab was built within Microsoft Azure using a dedicated Resource Group and Log Analytics workspace.

The environment included:

* Azure Resource Group
* Log Analytics Workspace
* Microsoft Sentinel
* Microsoft Defender XDR integration
* Azure Automation
* User-Assigned Managed Identity
* Microsoft Graph permissions
* Microsoft Sentinel training telemetry

### Log Analytics workspace
The Log Analytics Workspace acts as the central location for the security data used within my lab. Microsoft Sentinel is connected to this workspace, allowing me to query and analyse the collected telemetry for threat hunting, detection and investigation.

While setting up the environment, I developed a better understanding of how the Resource Group, Log Analytics Workspace and Microsoft Sentinel work together:

Resource Group: Used to organise and manage the Azure resources that make up my lab environment.
Log Analytics Workspace: Provides the workspace where log and security telemetry can be stored and queried.
Microsoft Sentinel: Provides the SIEM capabilities I use to analyse the available security data, perform threat hunting and investigate potential threats.

Understanding the purpose of each component helped me see how the different parts of the Azure environment connect together to support Microsoft Sentinel.

<img width="1536" height="1024" alt="image" src="https://github.com/user-attachments/assets/ef73f5ac-5df2-40df-9a2d-ca22145e495f" />

