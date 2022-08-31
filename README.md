# THM-Writeups
This will be a repository featuring notes taken from THM rooms. 


# AD DS Consists of Objects which include:
1. Users which can be people or services.
2. Machines, which get a (shouldn't really be accessed)local admin account.
# Machine naming convention is: <MACHINENAME>$
3. Security groups which can consist of both users and machines. These groups include:
- Domain Admins 
- Server Operators 
- Backup Operators 
- Account Operators 
- Domain Users
- Domain Computers 
- Domain Controllers 


# To configure users, groups or machines in Active Directory, we need to log in to the Domain Controller and run "Active Directory Users and Computers" from the start menu:

![image](https://user-images.githubusercontent.com/70596795/187562349-0344129e-6cff-4e44-ba80-66a659f68d4e.png)

List of defaut OUs and their purpose: 
1. Builtin: Contains default groups available to any Windows host.
2. Computers: Any machine joining the network will be put here by default. You can move them if needed.
3. Domain Controllers: Default OU that contains the DCs in your network.
4. Users: Default users and groups that apply to a domain-wide context.
5. Managed Service Accounts: Holds accounts used by services in your Windows domain.


To disable accidental OU deleteion protection, go to view -> enable "Advanced Features" -> right click OU and go to properties and uncheck the protection box

# Delegation: Giving control to a user over lower privledged user for support cases. EX: IT over Accounting. 
  
Powershell Reseting User Password: 
  
  Set-ADAccountPassword sophie -Reset -NewPassword (Read-Host -AsSecureString -Prompt 'New Password') -Verbose
  
# Segregating Devices/Machine into Categories: 
  1. Workstations 
  2. Servers 
  3. Domain controllers 
  
  
