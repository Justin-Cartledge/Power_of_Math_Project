![Justin](Justin Black.jpeg)

![Banner](github-header-image (4).png)

# To The Power of Math! Application - AWS Project

[Click - AWS-Based Exponential Calculation Application](https://dev.dcszzvgx7dd82.amplifyapp.com/)

<br><ins>Project Summary</ins><br>

This application is built on Amazon Web Services (AWS) to perform mathematical calculations, specifically raising a base number to a given exponent. It utilizes a serverless architecture for scalability and efficiency, leveraging services such as AWS Lambda for backend computation, Amazon API Gateway for secure access, and AWS Amplify or S3 for front-end hosting.


<br><ins>**Part 1. AWS Amplify** </ins>

<br>
Create and host a simple webpage using AWS Amplify for a simple index.html ![Amplify from AWS Console](Amplify from AWS Console.png)

<br>![Amplify Click Deploy App](Amplify Click Deploy App.png)

<br>Choose a create method.

<br>![Amplify Deploy App part 2](Amplify Deploy App part 2.png)

<br>Choose the App Name, Branch Name, and choose the Drag and Drop method to add the simple index.html.zip file.

<br>![Amplify Name App](Amplify Name App.png)

<br>Save and Deploy.

<br>![Amplify drag index zip](Amplify drag index zip.png)<br>

<br><ins>**Part 2. Use AWS Lambda to add the mathematical function code to be triggered with Python code**</ins><br>

Choose the "Author from Scratch" option to create the function, add the Function Name, and choose the Runtime (language for the function).<br>


<br>![Lambda python function](Lambda python function.png)<br>


<br>![Lambda python function 2](Lambda python function 2.png)<br>

Test the Lambda function.<br>

<br>![Lambda python function test](Lambda python function test.png)

<br>![Lambda python function test successful](Lambda python function test successful.png)<br>

Configure the Role Name and Permissions.<br>

<br>![lambda config role name execution](lambda config role name execution.png)<br>
<br>![lambda config role name execution 2](lambda config role name execution 2.png)<br>
<br>![lambda config role name execution 3](lambda config role name execution 3.png)<br>





<br><ins>**Part 3. words**</ins><br>

Within the VM, reviewed the Event Viewer and inspected the Security Logs to confirm that there is incoming log traffic such as event ID: 4625 for failed logins.<br>

<br>![Event Viewer](Azure VM Event View Logs for Failed Login Attemps_1.png)<br>


<br><ins>**Part 4. words**</ins><br>

Created the Log Analytics Workspace (LAW). The LAW is the central hub for collecting, storing, and analyzing log data across Azure and even non-Azure environments. Think of it as a specialized data lake for operational insights.<br>

<br>![LAW Picture](Azure Log Analystics Workspace Log Repository Creation_3.png)<br>

Created a Sentinel Instance and connected it to the LAW. Sentinel is a deployment of Microsoft’s cloud-native SIEM (Security Information and Event Management) and SOAR (Security Orchestration, Automation, and Response) solution within your Azure environment.<br>

<br>![Sentinel Picture](Azure Sentinel SIEM Creation_3.png)<br>

Configured the "Windows Security Events via AMA" connector. This is a data ingestion tool in Microsoft Sentinel that uses the Azure Monitor Agent (AMA) to collect Windows security logs from machines and send them to a Log Analytics Workspace.<br>

<br>![AMA Picture](Azure Sentinel SIEM Log Forwarding_1.png)<br>

<br>![Log Picture](Azure Log Analystics Workspace Log Repository Query_1.jpg)<br>

<br><ins>**Part 5. words**</ins><br>

Created the Data Collection Rule (DCR) within Sentinel, and created a Watchlist. A DCR stands for Data Collection Rule—it’s a configuration that tells Azure Monitor what data to collect, how to process it, and where to send it. A watchlist is a customizable list of data that helps you correlate, filter, and enrich security events. Think of it as a reference table you can use to enhance threat detection and response.<br>

<br>Imported a spreadsheet (as a “Sentinel Watchlist”) which contains geographic information for each block of IP addresses.<br>

<br>![GeoMapping Pic 1](Azure Create Watch List with GeoMapping of IPs for Log Attempts_1.jpg)<br>

<br>![GeoMapping Pic 2](Azure Create Watch List with GeoMapping_1.jpg)<br>

<br><ins>**Part 6. words**</ins><br>

<br>![Attack Map](Azure Attack Map_1.jpg)<br>

<br>As a project overview, a honeypot environment was established within Microsoft Azure by provisioning a virtual machine (VM) intentionally exposed to the public internet. Steps involve: Honeypot Configuration, Log Collection and Forwarding, SIEM Integration, and Attack Source Visualization. Below is a visual representation of what was created.<br>

<br>![Attack Map](Azure Project Overview_1.png)<br>



