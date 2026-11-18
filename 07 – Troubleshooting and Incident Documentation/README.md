## 1. Lab Overview

This lab demonstrates the process of recording, investigating, troubleshooting, and documenting IT support incidents using osTicket. It focuses on identifying technical issues, recording investigation findings, communicating progress, and documenting incident resolutions.

## 2. Objectives

- Understand the incident management process.
- Record and classify technical incidents.
- Identify reported symptoms and potential causes.
- Document troubleshooting activities.
- Record investigation findings and internal notes.
- Communicate incident updates to users.
- Document solutions and incident closure.
- 
## 3. Environment and Tools
  
-Understand the incident management process.
-Record and classify technical incidents.
-Identify reported symptoms and potential causes.
-Document troubleshooting activities.
-Record investigation findings and internal notes.
-Communicate incident updates to users.
-Document solutions and incident closure.

## 4. Incident Reporting

A customer reported that their workstation was unable to connect to the internet. The issue was recorded in osTicket as a network connectivity incident for investigation and resolution.

## 5. Initial Assessment and Impact Analysis

The initial assessment focused on identifying whether the issue was related to the physical network connection or the workstation's network configuration.
The network cable was inspected for visible damage, and the network port indicator light was confirmed to be on. The affected workstation was unable to access the internet, while other office workstations were operating normally.

## 6. Troubleshooting and Investigation

The following troubleshooting steps were performed:

1. Checked the network cable or Wi-Fi connection.
2. Inspected the network cable for visible physical damage.
3. Confirmed that the network port indicator light was on.
4. Investigated the workstation's IP address configuration.
5. Identified that the default gateway was unavailable.
6. Checked another office workstation and confirmed that its network connectivity was working.
7. Investigated the affected workstation and identified that the DHCP Client service was stopped.

## 7. Root Cause and Corrective Action

**Root Cause:** The DHCP Client service on the affected workstation was stopped, preventing it from obtaining the necessary network configuration automatically.

**Corrective Action:** Started the DHCP Client service.

After starting the service, the workstation successfully obtained an IP address and default gateway.

## 8. Resolution and Closure

The workstation's network configuration was restored successfully. Internet connectivity was verified, and the customer was able to access the internet again.

The troubleshooting findings, identified root cause, corrective action, and resolution were documented in the osTicket incident record.

## 9. Key Skills Demonstrated

- Network connectivity troubleshooting
- Physical network cable inspection
- IP address and default gateway investigation
- DHCP Client service troubleshooting
- Root cause identification
- Corrective action implementation
- Incident documentation and resolution

  ## 10. Screenshots
