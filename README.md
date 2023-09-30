<p align="center">
<img width="407" alt="Screenshot 2023-09-29 at 8 11 59 PM" src="https://github.com/lucasfregoso/network-file-share/assets/144977615/8cb6f1a2-4c08-4767-a7f4-ed2823c44f80">
</p>

<h1>Network Files Shares and Permissions</h1>
This tutorial outlines the process of sharing files and folders over the network and allowing users and groups to different levels of access.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Files

<h2>Operating Systems Used </h2>

- Windows 10 Pro</b> (22H2)
- Windows Server Datacenter 2022 Azure Edition

<h2>Network Files and Permissions Steps</h2>

- Stage 1
- Stage 2
- Stage 3

(Images going from left to right)
<h2>Installation Steps</h2>

Stage 1
<p>
<img width="1386" alt="Screenshot 2023-09-29 at 8 23 55 PM" src="https://github.com/lucasfregoso/network-file-share/assets/144977615/ec72243c-d34f-46e4-bcde-15593b63ef64">
</p>
<p>
In this lab we will also have the same virtual machines as in the Active Directory lab with DC-1 and Client 1 while being logged in to both of them, with Client 1 being logged in as one of our auto generated users that we created in Active Directory lab. Firstly, we are going to create a few folders named:  “read-access”, “write-access”, “no-access”, “accounting." For the folder “read-access”, we will put it the group “Domain Users”, and the permission we will give it will be “Read." For the next folder “write-access”, we will put it the group “Domain Users”, and the permission we will give it will be “Read/Write." For the third folder “no-access”, we will put it the group “Domain Admins”, and the permission we will give it will be “Read/Write."
</p>
<br />
