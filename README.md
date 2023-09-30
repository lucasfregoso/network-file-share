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

Stage 2
<p>
<img width="1614" alt="Screenshot 2023-09-29 at 8 35 41 PM" src="https://github.com/lucasfregoso/network-file-share/assets/144977615/c5347ca2-19c1-4a07-b1e8-3cf6d227192b">
</p>
<p>
Next, on Client 1 we go to the shared file (\\dc-1) and we just test out the permissions we gave it each of the folders we made and observe that when we try to open up the "no-access" folder it lets us know that we do not have access. Then, when we open up the "read-access" file we notice that we can open up but we cannot add any sort of text file because it had been set to only read access. For our read/write folder we are able to create a text file and read anything that may be placed in there. 
</p>
<br />


Stage 3
<p>
<img width="1614" alt="Screenshot 2023-09-29 at 8 48 28 PM" src="https://github.com/lucasfregoso/network-file-share/assets/144977615/a64dedbb-dbdb-44e3-b72e-2c2a2381a2b3">
------------------------------------------------------------------------------------------------------------------------------
<img width="1372" alt="Screenshot 2023-09-29 at 8 49 04 PM" src="https://github.com/lucasfregoso/network-file-share/assets/144977615/dddebad0-e030-44b7-a06a-8be65e6fdda3">
</p>
<p>
Lastly, we go ahead and create an "ACCOUNTANTS" security group and test access with our user in Client 1. So, first we go back to DC-1 and in active directory we create a security group called "ACCOUNTANTS" and then on our "accounting" folder we set these permissions as follows with the “accounting” folder in the group “ACCOUNTANTS” and the permissions being “Read/Write." Then, going back to Client 1 we try and access the folder and notice that we come to a fail, but then to fix this we go to DC-1 and make our user that is logged into Client 1 (which is bal.ger from our list of users) a member of the "ACCOUNTANTS" security group. Now we'll log out and right back in and test to see if we can open the folder and now we are able to.
</p>
<br />




