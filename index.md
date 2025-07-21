![Justin](Justin Black.jpeg)

![Banner](github-header-image (4).png)

# Home Security Operation Center (SOC) - Honey Pot Project - Monitoring Live Attacks

<br><ins>**Part 1. Setup Azure Subscription and Virtual Machine** (VM)</ins>

<br>
Created an Azure Subscription, and logged in at: [Microsoft Azure](https://portal.azure.com/#home)

<br>![Account Creation Picture](Azure Account Creation Resize.jpeg)

<br>Created Azure Resource Group. A Resource Group is like a container that holds related resources for your cloud solution—think of it as a folder for organizing everything you deploy in Azure.

<br>![Resource Group Picture](Azure Resource group creation_2.jpg)

<br>Created the Azure Virtual Network (VNET). A VNET is the backbone of networking in Microsoft Azure—it’s your private cloud network where you can securely run and connect resources like virtual machines, databases, and web apps.

<br>![VNET Picture](Azure Virtual Network Creation_2.png)

<br>Created the Azure Virtual Machine (VM). A VM is a cloud-based computer you can create and run on Microsoft Azure—without needing to buy or maintain physical hardware.

<br>![VM Picture 1](Azure Virtual Machine Deployed_1.jpg)<br>

<br>![VM Picture 2](Azure Virtual Machine Deployed_2.jpg)

<br><ins>**Part 2. Create the Honey Pot - Azure Virtual Machine**</ins><br>

In order to create the Honey Pot, the Security Group rule, which only allows Inbound RDP traffic, was deleted, and a rule was created in the Network Security Group for the virtual machine (VM) that allows ALL traffic inbound.<br>

<br>![Network Sec Group Picture 1](Azure Network Security Group_1.jpg)<br>

<br>![Network Sec Group Picture 2](Azure Network Security Group_2.jpg)<br>

Using the newly created VM's Public IP address, and Remote Desktop Protocol (RDP), the VM was logged into in order to turn off the Windows firewall.<br>

<br>![Delete Firewall Picture 1](Azure Logging into VM to disable internal Firewall_2.png)

<br>![Delete Firewall Picture 2](Azure Logging into VM to disable internal Firewall_3.png)

<br>![Delete Firewall Picture 3](Azure Logging into VM to disable internal Firewall_4.png)


<br><ins>**Part 3. Logging into the VM and inspecting logs**</ins><br>

Within the VM, reviewed the Event Viewer and inspected the Security Logs to confirm that there is incoming log traffic such as event ID: 4625 for failed logins.<br>

<br>![Event Viewer](Azure VM Event View Logs for Failed Login Attemps_1.png)<br>


<br><ins>**Part 4. Log Forwarding and KQL**</ins><br>

Created the Log Analytics Workspace (LAW). The LAW is the central hub for collecting, storing, and analyzing log data across Azure and even non-Azure environments. Think of it as a specialized data lake for operational insights.<br>

<br>![LAW Picture](Azure Log Analystics Workspace Log Repository Creation_3.png)<br>

Created a Sentinel Instance and connected it to the LAW. Sentinel is a deployment of Microsoft’s cloud-native SIEM (Security Information and Event Management) and SOAR (Security Orchestration, Automation, and Response) solution within your Azure environment.<br>

<br>![Sentinel Picture](Azure Sentinel SIEM Creation_3.png)<br>

Configured the "Windows Security Events via AMA" connector. This is a data ingestion tool in Microsoft Sentinel that uses the Azure Monitor Agent (AMA) to collect Windows security logs from machines and send them to a Log Analytics Workspace.<br>

<br>![AMA Picture](Azure Sentinel SIEM Log Forwarding_1.png)<br>

<br>![Log Picture](Azure Log Analystics Workspace Log Repository Query_1.jpg)<br>

<br><ins>**Part 5. Log Enrichment and Finding Location Data**</ins><br>

Created the Data Collection Rule (DCR) within Sentinel, and created a Watchlist. A DCR stands for Data Collection Rule—it’s a configuration that tells Azure Monitor what data to collect, how to process it, and where to send it. A watchlist is a customizable list of data that helps you correlate, filter, and enrich security events. Think of it as a reference table you can use to enhance threat detection and response.<br>

<br>Imported a spreadsheet (as a “Sentinel Watchlist”) which contains geographic information for each block of IP addresses.<br>

<br>![GeoMapping Pic 1](Azure Create Watch List with GeoMapping of IPs for Log Attempts_1.jpg)<br>

<br>![GeoMapping Pic 2](Azure Create Watch List with GeoMapping_1.jpg)<br>

<br><ins>**Part 6. Attack Map Creation**</ins><br>

<br>![Attack Map](Azure Attack Map_1.jpg)<br>

<br>As a project overview, a honeypot environment was established within Microsoft Azure by provisioning a virtual machine (VM) intentionally exposed to the public internet. Steps involve: Honeypot Configuration, Log Collection and Forwarding, SIEM Integration, and Attack Source Visualization. Below is a visual representation of what was created.<br>

<br>![Attack Map](Azure Project Overview_1.png)<br>



