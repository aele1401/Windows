# Windows System Administration
### GPO: Disable Local Link Multicast Name Resolution (LLMNR)
- Local Link Multicast Name Resolution (LLMNR) is a Windows network protocol used to resolve hostnames to IP address which is susceptible to several threats and is a vulnerability that will be disabled.
    * LLMNR accepts any response, unable to differentiate between real and fake responses allowing threats like spoofing, credential theft, and DOS.
    * Disabling this feature will prevent this vulnerability from being exploited.
    ![Diagram](https://github.com/aele1401/Linux/blob/main/Bash_Scripting/sshd_config.png)
### GPO: Account Lockout
- Account lockouts disable access to accounts for a certain amount of time after a set number of failed login attempts.
    * This mitigates against brute force attacks where attackers password spray accounts.
### GPO: Enabling Verbose PowerShell Logging & Transcription
- PowerShell is a task automation and configuration management framework from Microsoft, consisting of a command-line shell and the associated scripting language. Built on the .NET framework, it allows administrators to perform administrative tasks on local and remote Windows systems, including managing system settings, automating workflows, and managing processes. It's often used as a "live off the land (LotL)" tool by attackers.
    * Despite its legitimate administrative uses, attackers exploit PowerShell for malicious purposes due to its powerful capabilities and deep integration with Windows.
    * PowerShell is a tool that cannot just be disabled as many operations and security tools rely on its use, such as workstation and software deployment, security logging and analytics, and forensics operations.
- A common PowerShell practice that is important for all devices is enabling *enhanced PowerShell logging and visibility through verbosity.
    * This is important for tools like SIEM and forensics to help combat obfuscated PowerShell payloads.
![Diagram]()
![Diagram]()
![Diagram]()

### Enumerate Access Control Lists Script
- A PowerShell script that will enumerate the Access Control List of each file or subdirectory within the current working directory.
    * In Windows, access to files and directories are managed by Access Control Lists (ACLs). These identify which entities (known as security principals), such as users and groups, can access which resources. ACLs use security identifers to manage which principals can access which resources.
![Diagram]()

### Verifying PowerShell Logging GPO
