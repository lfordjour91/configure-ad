<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>Installation and Setting up Active Directory (Azure)</h1>
This project demonstrates the configuration of Active Directory Domain Services within a cloud-based virtual environment. A domain controller was created and promoted, organizational units were made, administrative users were made, and a client machine was successfully joined to the domain. The setup simulates a real-world enterprise environment where centralized identity and access management is required.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
  - Domain Controller (Windows Server)
  - Client Machine(Windows 10)
- Active Directory Domain Services
- Private Virtual Network

<h2>Prerequisites</h2>

- Need two virtual machines
  -The Domain Controller running a Window Server VM
  -The Client Machine running a Windows 10 VM
- Both machines on the same virtual network

<h2>Steps of Setting Up Active Directory</h2>

<p>
<img width="757" height="535" alt="Screenshot 2026-04-14 at 11 45 43 AM" src="https://github.com/user-attachments/assets/c3c5853a-07da-4ba2-8f8d-c3366abd9997" />

</p>
<p>
Active Directory Domain Services was installed on the domain controller (DC-1). The server was then promoted to a domain controller by creating a new forest using a custom domain name (e.g., mydomain.com). After promotion, the system was restarted and accessed using domain credentials.
</p>
<br />

<p>
<img width="668" height="518" alt="Screenshot 2026-04-14 at 11 48 53 AM" src="https://github.com/user-attachments/assets/802af723-6a90-4804-a4da-54b243fdf198" />
</p>
<p>
Within Active Directory Users and Computers (ADUC), organizational units were created to organize directory objects, including “_EMPLOYEES” and “_ADMINS.” A new administrative user named Jane Doe (username: jane_admin) was created and added to the Domain Admins security group to grant elevated privileges. The system was then accessed using this new domain admin account for all future administrative tasks.
</p>
<br />

<p>
<img width="1172" height="744" alt="Screenshot 2026-04-14 at 11 52 55 AM" src="https://github.com/user-attachments/assets/caa88b87-5b8a-4aef-b87c-52b5f00f5449" />
</p>
<p>
The client machine (Client-1) was configured to use the domain controller’s private IP address as its DNS server within the Azure portal. After restarting the client machine, it was joined to the domain (mydomain.com) using local administrator credentials, which required another restart to complete the process.
</p>
<br />
<p>
<img width="668" height="518" alt="Screenshot 2026-04-14 at 11 48 53 AM" src="https://github.com/user-attachments/assets/69d27687-a631-4d67-81ba-045ca7373fc2" />
</p>

<p>
After the domain join was completed, the domain controller was used to verify that Client-1 appeared in Active Directory Users and Computers. A new organizational unit named “_CLIENTS” was created, and the client machine object was moved into this OU to maintain proper directory structure and organization.
</p>
<br />

