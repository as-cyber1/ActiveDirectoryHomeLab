# Active Directory Home Lab 

## Objective

The Active Directory Home Lab project aimed to establish a controlled environment to simulate a basic enterprise network. The primary focus was to gain hands-on experience with AD features such as user and group management, domain configuration, DNS, and Group Policy

### Skills Learned

- Setting up and configuring a Domain Controller (DC). 
- Testing and troubleshooting GPOs to enforce configurations like password policies, desktop settings, and software restrictions.
- Understanding IP addressing, network troubleshooting, and configuring static IPs for AD and DNS services.
- Analyzing event logs and monitoring domain health using built-in Windows tools.


### Tools Used

- Windows Server 2022 to et up the Domain Controller, DNS, DHCP, and other services.
- Network configuration tools (such as ipconfig and ping) for verifying network connectivity, DNS resolution, and diagnosing network issues.
- Event viewer to analyze system logs for errors related to AD, DNS, and other server roles

  
### Steps

## Configuring Active Directory on Virtuabox using Windows Server 2022

1. Installed a Windows Server 2022 ISO onto a virtual machine and added it to a preconfigured NatNetwork. Renamed the server to CYBER-DC01, set a static IP address of 192.168.10.7, checked and verified connectivity using ipconfig and ping, and ran all updates. 
![natnetworko](https://github.com/user-attachments/assets/d0c6eedb-9f35-4bb5-a794-06157c6ef1e1)
![net_connect](https://github.com/user-attachments/assets/1fa1588f-1b9c-42d2-a64b-8997b4d27307)


2. In the server manager, I selected manage > add roles and feautures > role-based or feature-based installation > selected my server CYBER-DC01 from the server pool > choose the following sever roles: Active Directory Domain Services, DNS server, and Remote Access
![server_roles](https://github.com/user-attachments/assets/0e175e6b-c5b0-4122-9850-a1a36c7a0745)
![static_ip](https://github.com/user-attachments/assets/f667bc74-a40a-452a-b527-52d9562c9d63)

3. Once post deployment configuration was done, I clicked promote this server to a domain controller.
![promote](https://github.com/user-attachments/assets/1794a00d-159e-4115-b488-f6b4351587a3)

4. I created a new forest named cyberdfir.local and then rebooted the server. 
![promote2](https://github.com/user-attachments/assets/058de596-a823-4405-9abc-3f34fea6e645)
![DC](https://github.com/user-attachments/assets/a272bc08-c5f0-48d1-821c-ec6b9305e762)


6. Back on the server manager, I clicked tools and selected Active Directory Users and Computers and created organizational units (OUs), groups, and users.
![it](https://github.com/user-attachments/assets/5106d649-a911-4384-94c0-e97f9588e52d)


7. Last thing I did, was create group policy objects to my cyberdfir.local domain such as a password policy, default wallpaper, drive mapping, and restrict control panel access.
![gpo](https://github.com/user-attachments/assets/a55599e5-7b50-446b-bed4-e89d154376fb)


