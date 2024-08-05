
# Active-Directory-Lab

## Objective

The aim of this project is to create a home lab Active Directory setup integrating Splunk, Kali Linux, and Atomic Red Team. The objective is to understand domain environments, enhance proficiency in event ingestion for a SIEM, and generate telemetry for improved detection of real-world attacks in the future.

### Skills Learned

- Installing and configuring windows server 2022, Ubuntu server 22.04, Windows 10 and Kali Linux
- Installing and configuring Sysmon and Splunk on to Windows 10 and Windows server
### Tools Used

- Windows Server 2022 | For Active Directory
- Ubuntu Server 22.04 | For Splunk
- Windows 10 | As my target machine
- Kali Linux | As my attacker machine
- Splunk
- Sysmon
- Atomic Red Team 

## Steps


*This is the Logical Diagram to help understand how the data is going to flow!
![Paragon AD Logical Diagram 1](https://github.com/user-attachments/assets/38792190-d4fa-4226-8ae7-8126675b8784)


*The assets/ virtual machines (Windows server 2022 (ADDC02), Kali Linux, Windows 10 (Demo), Ubuntu Server 2022 (Splunk)
<img width="523" alt="Screenshot 2024-08-05 at 11 39 18 AM" src="https://github.com/user-attachments/assets/93d47480-8095-4fc4-978f-ae17e46ba7d1">

*Setting up a static IP on my splunk server to reflect the static IP from my diagram 
<img width="638" alt="Screenshot 2024-08-05 at 12 36 28 PM" src="https://github.com/user-attachments/assets/a75f6495-1132-44f8-b38e-be5df519598e">

*Added a shared folder where my Splunk installation lives 
![Shared folder](https://github.com/user-attachments/assets/03dff41e-45de-4ddd-b79e-411f278ccba3)

** Added a user to vboxsf (not shown) and mounted my shared folder onto my directory called "Shared" 
<img width="639" alt="Screenshot 2024-08-05 at 1 28 26 PM" src="https://github.com/user-attachments/assets/057924a3-702d-4fcf-bc49-1afcd340e787">

![Loading splunk into ubuntu server](https://github.com/user-attachments/assets/6e27c600-e3a9-42d2-8636-7d6f5f875fd3)

* Installing Splunk
  
![installing splunk](https://github.com/user-attachments/assets/aad666ee-0eb2-4d1a-8d85-b9fcb59b7a5a)
![Screenshot 2024-07-17 at 8 31 55 PM](https://github.com/user-attachments/assets/912eeff7-23e8-4341-b2fc-8bc7719755b8)

*Updating the target machine (windows 10) ip address <img width="889" alt="Pointing windows machine to domain controller" src="https://github.com/user-attachments/assets/155cdfd0-a552-4763-82d4-166f56b90323">

*installing splunk universal forwarder 

![Setting up splunk univesal forwarde](https://github.com/user-attachments/assets/1fa70b22-d56b-40e1-9a08-d37f9ba199ef)

*Installing sysmon and using the olaf configuration 


![downloading sysmon64 to windows ](https://github.com/user-attachments/assets/933f0412-a8d5-49b7-a2dc-2162def2905a)
![Sysmon config file olaf](https://github.com/user-attachments/assets/fe7f2729-5f69-4050-af1f-f389615df987)

*Instructing Splunk forwarder on what to send to Splunk server by configuring a index file ( I created this file under the local directory and not the default directory) (Instructing splunk forwarder to push events related to Application, Security, System as well as Sysmon over to Splunk service)

![Endpoing config for splunk](https://github.com/user-attachments/assets/630c4101-779f-4934-889a-5c744135aa04)

*Creating the index in splunk called "Endpoint" (all events from the inputs file are being pushed to an index called enpoints) && showing that the it is receiving the events!

<img width="888" alt="Creating the endpoint index for splunk" src="https://github.com/user-attachments/assets/88928d9a-b0c7-4201-9a87-40585a2879e5">
<img width="879" alt="splunk showing events from windows 10" src="https://github.com/user-attachments/assets/2bef49df-4d99-43df-b3ee-5b2909e546ee">

*Installing Active Directory 
<img width="807" alt="Screenshot 2024-07-31 at 12 20 11 PM" src="https://github.com/user-attachments/assets/81a2ed60-6977-43eb-a93f-2d7d33fa6f65">
<img width="815" alt="Installing AD" src="https://github.com/user-attachments/assets/31fd98bb-153a-4182-8dcb-788da6c188e2">

*Promoting the server to a Domain Controller (didn't take screenshot after I already created it) 
![Screenshot 2024-08-05 at 3 55 07 PM](https://github.com/user-attachments/assets/024c9698-a2d8-4a58-af38-6db078f4da44)
