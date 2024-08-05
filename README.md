
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

*Added a shared folder where my Splunk installation lives  (added a user to vboxsf (not shown)
<img width="350" alt="Screenshot 2024-08-05 at 12 58 13 PM" src="https://github.com/user-attachments/assets/204e5f38-e246-4a0e-9120-30a4ac92f613">

