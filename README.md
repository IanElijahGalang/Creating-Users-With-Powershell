<h1>Creating Users With Powershell</h1>

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Powershell

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)
- Windows Server 2022</b>

<h2>1. Allowing Non-Administrative Users to Access Client-1</h2>
Before creating users, we want to allow normal, non-administrative users to be able to access and login to Client-1.
	Doing so we have to login with the admin user in Client-1.<br>
<ul>
   <li>Go to Remote Desktop in the Systems App and allow “Domain Users” to access remote desktop</li> 
</ul>
<img width="1023" alt="Allow RD" src="https://github.com/user-attachments/assets/c2b0474f-f716-41f5-98f7-a1e7b6721121" />

<h2>2. Creating Users Using PowerShell</h2>
In the Domain Controller, run Windows Powershell ISE as an administrator and type out this code into a new script.<br>
<ul>
  <li>This script automates the process of creating multiple Active Directory user accounts with randomized names and passwords.</li>
  <li>This script relies on the EMPLOYEES Organizational Unit that we made earlier to exist.</li>
  <li>Running this script will create thousands of users with different letters as names.</li>
</ul>
<img width="1512" alt="run powershell ISE" src="https://github.com/user-attachments/assets/fb707cf6-c651-481e-9dbf-1664f91c9c85" />
<img width="1128" alt="Script Code" src="https://github.com/user-attachments/assets/2ec8c70b-f825-45a2-91e2-36741180bcf5" />

<h2>3. Verifying the Created Users</h2>
After running the script, you will have multiple users created under the Employees OU in Active Directory.
<img width="1118" alt="code running " src="https://github.com/user-attachments/assets/a1d842df-6196-4d25-b8ca-ebcdaeaa699f" />
<img width="1000" alt="names in ADUC" src="https://github.com/user-attachments/assets/918cb8e8-9a05-4199-acb1-00ffbbc3fdd3" />

<h2>4. Testing User Login on Client-1</h2>
Choosing any of these newly made accounts, we can try logging into the Client-1 VM and observe the end result.
<ul>
 <li>This example I chose “bas.kob”</li> 
</ul>
<img width="423" alt="Member oF" src="https://github.com/user-attachments/assets/7ed15ade-d614-4fb2-acd9-056b291a2bfb" />
<img width="745" alt="bas2" src="https://github.com/user-attachments/assets/040b05de-e34c-46f7-9981-f1615c1f3274" />




