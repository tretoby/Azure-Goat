**Real-time Threat Intelligence with Azure Sentinel** 

Objective

To design and implement a robust Security Operations Center (SOC) using Azure Sentinel as the core SIEM platform. This project aims to: 

* **Deploy Azure Sentinel:** Configure and deploy Azure Sentinel to monitor and analyze security logs from various sources.
* **Integrate Threat Intelligence Feed:** Integrate a threat intelligence feed to enhance threat detection capabilities.
* **Create Custom Alerts:** Develop custom alerts for specific security events and anomalies.
* **Automate Incident Response:** Implement automated response actions for high-priority alerts.
* **Visualize Security Data:** Utilize Azure Sentinel's visualization tools to gain insights into security trends and patterns.

Skills Learned

* **Cloud Security:** Deepened understanding of Azure security services and best practices.
* **SIEM Implementation:** Hands-on experience with deploying and configuring Azure Sentinel.
* **Threat Intelligence Integration:** Knowledge of integrating threat intelligence feeds into a SIEM solution.
* **Alert Creation and Tuning:** Ability to create effective alerts and tune detection rules.
* **Incident Response Automation:** Experience in automating incident response workflows.
* **Security Data Analysis and Visualization:** Skill in analyzing security logs and visualizing security trends.
* **Azure Platform:** Proficiency in using Azure services, including virtual machines, storage, and networking.


Steps

Create a virtual machine 
![image](https://github.com/user-attachments/assets/3f91d66d-f1cc-4ae5-9ac6-046a60c10713)

Set up resource group, virtual machine name, and choose a windows image
![image](https://github.com/user-attachments/assets/19cddd3e-e4d0-46b7-ac8e-a5b27c24b1c8)

allow RDP (3389) to be open to attract malicious traffic 
![image](https://github.com/user-attachments/assets/baba3b81-debc-448b-bae8-985daa1aac63)


![image](https://github.com/user-attachments/assets/e77471b4-2429-4c3d-8c0d-9057741aca40)

While the virtual machine is deploying navigate to Microsoft Sentinal
![image](https://github.com/user-attachments/assets/9cdd5cbe-fc37-4d96-81a7-86452ec14e9a)

creat log analytics workspace using the resource group created in the virtual machine setup 
![image](https://github.com/user-attachments/assets/2cdc5ee0-60a0-41e9-9244-a81485c054ff)

deploy workspace 
![image](https://github.com/user-attachments/assets/32084e8e-370b-4922-936a-8c37022e5a59)

add Microsoft Sentinal to a workspace
![image](https://github.com/user-attachments/assets/3a748c71-cd92-48b6-b366-2ab7b805ddba)

navigate to data connectors tab in Microsoft Sentinal
![image](https://github.com/user-attachments/assets/5cb7e3b3-cde5-47b4-8157-697ad3a1414a)

Click on content hub and search for Azure monitor agent and install windows security events 
![image](https://github.com/user-attachments/assets/831d0a8f-cbd7-477c-9d39-5be38275382e)

navigate back to the data connectors tab and hit refresh. Two connectors should be present
![image](https://github.com/user-attachments/assets/acbef597-de41-46de-86e5-55c49b0989bb)

open windows connector page (not the legacy page)!
![image](https://github.com/user-attachments/assets/9daecf6b-efc2-4c59-a143-c1d4432fc9f4)

create a data collection rule
![image](https://github.com/user-attachments/assets/a49f21f0-9832-45af-838f-ecb041d3ef1b)

on resource tabs select the vm group
![image](https://github.com/user-attachments/assets/15ef3fca-2943-40f3-805f-232ccd9b68b7)

create rule
![image](https://github.com/user-attachments/assets/73e91b22-3901-4e63-be45-5e32431f6c02)

navigate to logs and wait for an inident to occur
![image](https://github.com/user-attachments/assets/df38a7c1-0901-4dc4-8d4f-b7484f8fdbd2)

can set custom querys to filter through events 
![image](https://github.com/user-attachments/assets/21d317c7-2d45-4c9c-80db-1b364f4fd448)

special privileges assigned to new login 
![image](https://github.com/user-attachments/assets/978d8af5-550d-49cf-b0ad-3c48d3eec2aa)

select logon activity by account
![image](https://github.com/user-attachments/assets/e523d1c5-daa0-4c3b-91b4-0574094d92d6)

create an alert rule to detect every 5 mins
![image](https://github.com/user-attachments/assets/ae51358e-ffe1-4d17-bb41-54c239c27e5c)

navigate to the nalytics workspace and see new alerts for everytime a logon occurs  
![image](https://github.com/user-attachments/assets/7bd32022-c52f-4d47-8387-c8a8a292f1ef)
























