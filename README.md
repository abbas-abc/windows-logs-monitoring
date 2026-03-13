# Windows Logs Monitoring & Analysis

A beginner-level cybersecurity and system administration project focused on understanding Windows log monitoring using the built-in Windows Event Viewer tool.

## Overview

Real log data was collected and analyzed from a live Windows machine across three log categories: Security, System, and Application. Each log was explored in detail, individual events were opened and documented, and screenshots were taken as evidence throughout the process.

## What Was Analyzed

| Log Type | Total Events | Key Finding |
|---|---|---|
| Security | 35,165 | 1 Audit Failure (failed login — Event 4625) |
| System | 40,469 | NetBIOS naming conflict (Event 2505) |
| Application | 32,588 | Licensing cycle via Security-SPP |

## Key Event IDs Covered

- **4624** — Successful Logon
- **4625** — Failed Logon (Audit Failure)
- **4634** — Account Logoff
- **6013** — System Uptime (170,584 seconds / ~47.4 hours)
- **105** — Power Source Change
- **2505** — Network Transport Binding Error
- **16384** — SPP Service Restart Scheduled
- **16394** — Licensing Migration Succeeded
- **0** — Generic edgeupdate Event

## Most Significant Finding

**Event ID 2505** — A real NetBIOS naming conflict was discovered in the System log. Another device on the same network was using the same computer name (Abbas), which was silently preventing the server service from starting. This finding would have been nearly impossible to diagnose without log analysis.

## Tools Used

- Windows Event Viewer (eventvwr.msc)
- Microsoft Windows (live machine)

## Files

- `Windows_Logs_Project_Report_FINAL.docx` — Full project report with screenshots and analysis

## Skills Demonstrated

- Windows log navigation and analysis
- Event ID identification and interpretation
- Security event monitoring
- System fault detection through log data
- Documentation and reporting
