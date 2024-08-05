
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

