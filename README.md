# Nick's Cybersecurity Projects

Welcome to my cybersecurity projects repository. This space will contain:
- Practice labs
- Security automation tools
- Notes and learning resources

🔐 I'm passionate about ethical hacking, system hardening, and SOC analysis.


# Azure SOC Lab with Microsoft Sentinel

This project simulates a mini-SOC (Security Operations Center) using Microsoft Azure, a Windows VM, and Microsoft Sentinel. It’s based on Josh Madakor’s tutorial, with custom improvements and logs.

## 🛠️ Tools Used
- Microsoft Azure (Free Tier)
- Windows 10/Server VM
- Microsoft Sentinel (SIEM)
- Log Analytics Workspace
- KQL (Kusto Query Language)
- PowerShell (for simulated attacks)

## 🧱 Architecture
- One Windows VM in Azure
- Log Analytics agent installed
- Logs routed to Sentinel
- Detection rules set up
- Custom KQL queries

## 🧪 Simulated Attacks
- Disabled Windows firewall
- Unusual login attempt
- PowerShell downloading files
- Created custom alerts in Sentinel

## 🔍 Sample KQL Query
```kql
SecurityEvent
| where EventID == 4625
| project TimeGenerated, Account, Computer, IPAddress
