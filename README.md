<h1>Managing User Access Controls with Group Policy Manager </h1>


<h2>Description</h2>
In Windows, managing user access control involves defining and enforcing who can access specific resources and perform actions within the system. This is achieved through the careful configuration of permissions, user groups, and security policies. Additionally, establishing a robust password policy is fundamental in safeguarding sensitive information and preventing unauthorized access. A well-crafted password policy includes guidelines on password complexity, expiration, length, and other parameters that ensure passwords are strong and regularly updated
<br />


<h2>Languages and Utilities Used</h2>

- <b>Group Policy Management 
- Windows 

<h2>VPN walk-through:</h2>

<p align="center">
Open Group Policy Manager: <br/>
<img src="https://i.imgur.com/v9eE0lk.png" height="80%" width="80%" alt="hello this is reed"/>
<br />
<br />
Navigate to Forests > Domains > the Domain you want to edit > Domain Policy that will be edited:  <br/>
<img src="https://i.imgur.com/J8jm7BF.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Right-click on the Domain Policy and select edit: <br/>
 * This will launch the Group Policy Management Editor<br/>
<img src="https://i.imgur.com/O0V7yGZ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Here navigate to Computer Configuration > Policies > Window Settings > Security Settings > Local Polices > Security Options.   <br/>
<img src="https://i.imgur.com/IBi882w.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Open User Account Control: Behavior of the elevation prompt for administrators in Admin Approval Mode: <br/>
 * In this dialog box check the define this policy setting checkbox and click OK <br/>
<img src="https://i.imgur.com/WAZhKfZ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
User Account Control: Detect application installations and prompt for elevation, in this dialog box check the Define this policy setting checkbox select the Disabled radio button, and click OK:  <br/>
<img src="https://i.imgur.com/NqzF9r3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Back in the right pane double click User Account Control: Run all administrators in Admin Approval Mode, when this dialog box opens check the Define this policy setting checkbox and click OK:  <br/>
<img src="https://i.imgur.com/YwQfohh.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br/>
<br/>
In the left pane right click Security Options and select Export List to save file name as uac_config and click save:  <br/>
<img src="https://i.imgur.com/oJaiMPB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<p/> 


<br />
<h2>What was Learned</h2>

- <b>Group Policy Management: Group Policy Management is a feature of Windows that allows network administrators to control the working environment of user accounts and computer accounts. It's essential for implementing specific configurations across a network.
</b>

- <b>Default Domain Policy: The Default Domain Policy is a Group Policy object (GPO) that is created automatically when a new domain is created. It contains many of the security settings for the domain.</b>

- <b>Editing the Default Domain Policy: By editing this policy, you're setting rules and configurations that will apply to all computers and users in the domain.</b>

- <b>Navigating to Security Options under Computer Configuration: This path takes you to a range of security-related settings that you can configure for all computers in the domain.</b>

- <b>Configuring UAC Settings:
 
 - The behavior of the elevation prompt for administrators in Admin Approval Mode: This setting determines how administrative users are prompted when they perform a task that requires elevated privileges.
   
 - Detect application installations and prompt for elevation: Disabling this setting means the system will not automatically prompt for elevation when installations are detected, which can streamline certain processes but might reduce security.
   
 - Run all administrators in Admin Approval Mode: Enabling this policy ensures that even administrators operate under standard user privileges by default, increasing overall system security.
   
- <b>Exporting the Security Options: By exporting these settings, you create a record of the current configuration. This can be useful for documentation, auditing, or replicating the same settings on another domain or in a different environment.</b> 

