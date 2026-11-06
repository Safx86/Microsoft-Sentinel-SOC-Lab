# Microsoft Sentinel SOC Lab
A personal SOC lab documenting my journey with Microsoft Sentinel and Defender, including KQL threat hunting, security investigations, MITRE ATT&CK mapping, and custom detection engineering.

### About This Project

Cybersecurity is something I have wanted to get into for a long time, but for years I was never really sure what route to take or where to start.

Throughout my IT career, I have been fortunate to work with some great mentors who have encouraged me to keep learning, challenge myself, and think about where I want to take my career next. With their guidance, along with my own growing interest in cloud and security, I decided that Azure security and cybersecurity is the direction I want to pursue as my next career path.

After completing my AZ-900 and SC-900 certifications, I wanted to take the knowledge I had gained from studying and actually put it into practice. Rather than continuing to learn security purely through courses and theory, I wanted to build something hands-on where I could make mistakes, troubleshoot problems, investigate security activity and develop skills that are closer to what I would experience in a real SOC environment.

This project documents my journey building and working through a Microsoft Sentinel SOC lab, where I am gaining practical experience with Microsoft Sentinel, Microsoft Defender, KQL, security telemetry, threat hunting, MITRE ATT&CK mapping and detection engineering.

I also want this repository to show the reality of the learning process. I am not just documenting the parts that worked. I am recording the problems I ran into, the things I broke, what caused them, how I investigated them and, most importantly, what I learned from fixing them. Troubleshooting has been one of the most valuable parts of this project because it has helped me develop a much better understanding of Azure, Microsoft Sentinel, identity, permissions and security operations.

Ultimately, this project represents more than just completing a lab. It is part of my journey from EUC and IT support into cybersecurity, building practical skills alongside my existing IT experience and creating a portfolio that I can eventually use to showcase my skills, knowledge and progression to future employers.

### Objectives
* Build and configure a Microsoft Sentinel SOC lab in Azure
* Integrate Microsoft Sentinel with Microsoft Defender
* Analyse endpoint, network, identity, and cloud security telemetry
* Develop practical KQL threat-hunting skills
* Understand and apply the MITRE ATT&CK framework
* Build custom detection rules based on suspicious behaviour
* Develop practical incident investigation skills
* Document troubleshooting and lessons learned throughout the project

### Technologies & Concepts
* Microsoft Sentinel
* Microsoft Defender
* Microsoft Azure
* Azure Log Analytics
* Microsoft Entra ID
* Azure Automation
* Microsoft Graph
* Kusto Query Language (KQL)
* MITRE ATT&CK
* Crowdstrike Telemetry
* Palo Alto Firewall Telemetry
* Okta Identity Telemetry
* AWS CloudTrail Telemetry
* Azure RBAC
* Managed Identities

### Lab Architecture
<img width="1536" height="1024" alt="image" src="https://github.com/user-attachments/assets/4136e447-a834-4c7d-b81a-5f6940b141f7" />

### Project Progress

01	Multi-Source Threat Hunting & Detection Engineering	✅ Completed

02	Threat Intelligence	🔄 In Progress

03	MITRE ATT&CK Coverage	⏳ Planned

04	Automation Rules	⏳ Planned

### Exercise 01 - Multi-Source Threat Hunting
During Exercise 1, I explored security telemetry from multiple sources using KQL within Microsoft Defender Advanced Hunting.

Data sources investigated included:

* CrowdStrike endpoint telemetry
* Palo Alto firewall telemetry
* Okta identity telemetry
* AWS CloudTrail activity
  
I used this telemetry to investigate suspicious activity across endpoint, network, identity and cloud environments and developed a custom detection for multi-tactic activity affecting a single endpoint.

exercises/exercise-01/README.md

### Troubleshooting Highlights

Building the lab involved several Azure and Sentinel deployment challenges. Rather than rebuilding the environment after each failure, I investigated the underlying errors and worked through them individually.

* Resolved Azure Free Trial regional restrictions by rebuilding the environment in North Europe.
* Diagnosed missing Microsoft.Web and Microsoft.Automation resource provider registrations.
* Configured a User-Assigned Managed Identity and Microsoft Graph permissions for detection deployment.
* Troubleshot Azure RBAC versus Microsoft Entra role requirements.
* Diagnosed an Azure Automation regional quota that prevented a second Automation account from being created.
* Identified KQL time-window issues when prerecorded telemetry wasn't appearing in Advanced Hunting.

docs/troubleshooting.md

### Skills Demonstrated

* SIEM deployment and configuration
* KQL threat hunting
* Multi-source security analysis
* Endpoint security investigation
* Identity security investigation
* Network security analysis
* Cloud security analysis
* MITRE ATT&CK mapping
* Detection engineering
* Azure RBAC
* Managed identities
* Microsoft Graph permissions
* Microsoft Sentinel troubleshooting

### Lessons Learned

One of the biggest lessons from this project has been that deploying the technology is only part of building a SOC environment. Troubleshooting permissions, Azure resource providers, regional restrictions, managed identities, telemetry ingestion and KQL query scope helped me develop a much better understanding of how the different components of Microsoft Sentinel and Defender interact.

I also learned the importance of validating each stage individually rather than assuming that a successful deployment means every component is functioning correctly.

### Acknowledgements

This project uses the Microsoft Sentinel Training Lab to provide simulated security telemetry and investigation scenarios. This repository documents my own deployment, troubleshooting, KQL analysis, investigations, detections and learning outcomes.
