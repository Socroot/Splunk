# 🔎 Macro Hunting Dashboard

A Splunk dashboard designed for detecting and investigating suspicious Microsoft Office macro activities in enterprise environments.

This dashboard helps SOC Analysts, Blue Teamers, and Detection Engineers identify malicious document execution, suspicious Office behaviors, abnormal process relationships, and potential attacker activity.

## 🎯 Dashboard Purpose

The main purpose of this dashboard is to provide visibility into:

- Suspicious macro-enabled document activity
- Office application abuse
- Malicious process execution
- LOLBin abuse detection
- Suspicious command-line activity
- User and host impact analysis
- Network connections initiated by Office processes

## 📊 Dashboard Visualizations

### Total Suspicious Macro Events
Shows the total number of suspicious macro-related events detected in the environment and provides an overview of current macro activity.

### Unique Affected Hosts
Displays the number of unique endpoints where suspicious macro activity was detected to identify the scope of impact.

### Unique Affected Users
Shows users associated with suspicious macro execution events for identifying potentially targeted accounts.

### Macro-Enabled Documents Detected
Displays detected macro-enabled Office documents such as:

- `.docm`
- `.xlsm`
- `.pptm`

This helps identify potentially malicious documents used for initial access.

### Suspicious Office Process Spawns Over Time
Tracks suspicious child processes created by Office applications over time.

Examples:

- WINWORD.EXE → powershell.exe
- EXCEL.EXE → cmd.exe

Useful for detecting malicious document execution.

### Top Hosts/Users by Alert Count
Ranks the most active hosts and users based on suspicious macro alert volume to help prioritize investigations.

### Office → LOLBin Parent-Child Pairs
Shows suspicious relationships between Microsoft Office applications and Windows Living Off The Land Binaries (LOLBins).

Useful for detecting abuse of trusted Windows tools.

### Suspicious Command-Line Analysis
Provides visibility into suspicious command-line activity related to Office processes, including scripts, PowerShell execution, and encoded commands.

### Direct Network Connections from Office Processes
Displays outbound network connections initiated by Office applications to identify possible malicious communication or C2 activity.

## ⚙️ Requirements

- Splunk Enterprise
- Windows Event Logs
- Sysmon Process and Network Events
- Proper field extractions and data onboarding

## 🚀 Usage

1. Import `Macro_Hunting_Dashboard.json` into Splunk.
2. Configure required indexes and data sources.
3. Verify searches and field mappings.
4. Start hunting suspicious macro activity.

⭐ If you find this dashboard useful, consider giving this repository a star.

Created by **SocRoot**
