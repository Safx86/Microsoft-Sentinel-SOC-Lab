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

One of my first learning points from building the lab came from something as simple as naming a resource. I originally named my Log Analytics Workspace it-rg-sentinel-soc-lab because I hadn't yet understood the importance of using clear Azure resource naming conventions. As I worked further into the project, I learned that rg is typically used to identify a Resource Group, while a prefix such as law would make more sense for a Log Analytics Workspace.

I've left the original name in place because this repository is intended to document the learning process honestly, including the things I would do differently next time.

### Microsoft Sentinel Configuration
Once the Log Analytics Workspace was in place, the next step was to configure Microsoft Sentinel and connect it to the workspace I had created for the lab.

This allowed Microsoft Sentinel to use the security telemetry available within the workspace for monitoring, threat detection, investigation and threat hunting.

As part of the configuration, I:

* Enabled Microsoft Sentinel for my Log Analytics Workspace.
* Connected the lab workspace to Microsoft Sentinel.
* Integrated Microsoft Sentinel with Microsoft Defender XDR.
* Configured the relevant workspace as the primary workspace for the lab.

Working through this configuration helped me understand the relationship between Log Analytics, Microsoft Sentinel and Microsoft Defender XDR. Log Analytics provides the underlying workspace and data, while Sentinel and Defender provide the security tools I use to analyse that data, investigate suspicious activity and build detection's.

Once the configuration was completed, I was able to move into Microsoft Defender Advanced Hunting and begin validating the security telemetry that had been deployed as part of the training environment.

<img width="1342" height="470" alt="image" src="https://github.com/user-attachments/assets/5707285b-5b0b-48fe-8cba-52607b792a17" />
