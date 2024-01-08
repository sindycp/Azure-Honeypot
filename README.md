# Azure-Honeypot-RDP-Cyber-Attack-Simulation
![Azure Honeypot Diagram](https://i.imgur.com/nN8hOBp.png)

## Introduction

In this lab session, my objective is to establish a honeypot within the Microsoft Azure framework. In simple terms, a cybersecurity honeypot functions as a security mechanism, creating a virtual trap within a controlled and secure environment to attract potential attackers. The intention is to utilize this intentionally compromised computer system to study attacker methodologies, analyze various threats, and enhance security protocols. The primary goal of this lab is to acquire proficiency in collecting attack log data from the honeypot, querying it through a Security Information and Event Management (SIEM) system, and presenting the information in a comprehensible manner. Specifically, in this instance, the attack data will be visually represented on a global map, categorized by event count and geolocation.

## Objectives

Configuring and deploying Azure resources, including virtual machines, Log Analytics Workspaces, and Azure Sentinel, is a key focus. The role entails practical experience and understanding of a SIEM, specifically Microsoft’s Azure Sentinel.

## Primary Responsibilities

**1. VM Creation and Configuration** 

- Create and configure a Windows VM, accessible via Remote Desktop Protocol (RDP)

- Monitor security events for failed RDP connections within the Windows Event Viewer

**2. PowerShell Script for Log Enrichment**

- Develop a PowerShell script to extract and log failed RDP connection events

- Enrich the logs with geolocation data using the ipgeolocation.io API

**3. Log Analytics Integration**

- Connect the VM to Log Analytics, utilizing Kusto Query Language (KQL) to extract raw data from failed RDP logs Azure Sentinel Workbook

**4. Azure Sentinel Workbook**

- Transmit enriched data to Microsoft Sentinel's workbook, offering a visual representation of global RDP failed attempts

- Include graphs in the workbook to illustrate the frequency and geographical distribution of failed RDP attempts

## Lab Features

**RDP Event Fail Logs**

![Image](https://i.imgur.com/pTZZzuP.png)

RDP failed logon failures are extracted from the Windows Event Viewer

**Custom PowerShell Script Parsing Data From 3rd Party API**

![Image](https://i.imgur.com/qnVeCcV.png)

A custom PowerShell script is used to enrich logs with geolocation data, providing a comprehensive view of attackers' locations using the ipgeolocation.io API.

**Log Analytics**

![Image](https://i.imgur.com/RzyFs2E.png)

Connects the VM to Log Analytics, using KQL to abstract raw data from RDP failed logs.

**Global Attack Visual via Microsoft Sentinel Workbook**
![Image](https://i.imgur.com/AEtA3RT.png)

After transmitting enriched data to Microsoft Sentinel's workbook this attack map reveals numerous RDP and SMB failures, highlighting persistent attempts by potential attackers. It emphasizes the critical need to secure remote access and file-sharing services against unauthorized access and cyber threats.

## Lessons Learned

**Honeypot Impact:** Implementing a cybersecurity honeypot in Azure proved invaluable for studying attackers and fortifying security.

**SIEM Mastery:** Configuring Azure resources and using Microsoft’s Azure Sentinel deepened practical experience with SIEM tools.

**Effective Data Collection:** Proficiency in collecting attack log data highlighted the importance of meticulous data collection for robust threat analysis.

**Query Language Expertise:** Use of Kusto Query Language (KQL) underscored the need for query language expertise in the SIEM environment.

**Visual Communication:** Creating a global map for RDP failed attempts emphasized the importance of clear visualizations for effective analysis.

**Geolocation Integration:** Incorporating ipgeolocation.io API data showcased the value of enriching logs for a comprehensive view of attackers' locations.

**Continuous Security Focus:** The generated attack map emphasized the persistent nature of attackers, reinforcing the ongoing need to secure remote access and file-sharing services.

In conclusion, this lab project not only enhanced technical skills related to Azure resources and SIEM tools but also reinforced the importance of proactive security measures in the ever-evolving landscape of cybersecurity. The hands-on experience gained is invaluable for addressing real-world challenges and staying ahead of emerging threats.
