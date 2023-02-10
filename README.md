[![Ansible Galaxy](https://github.com/simeononsecurity/Windows_STIG_Ansible/actions/workflows/ansible_galaxy_collection.yml/badge.svg)](https://github.com/simeononsecurity/Windows_STIG_Ansible/actions/workflows/ansible_galaxy_collection.yml)[![VirusTotal Scan](https://github.com/simeononsecurity/Windows_STIG_Ansible/actions/workflows/virustotal.yml/badge.svg)](https://github.com/simeononsecurity/Windows_STIG_Ansible/actions/workflows/virustotal.yml)

#  Windows_STIG_Ansible
Ansible Playbooks for SimeonOnSecurity's STIG Scripts

## Notes: 
- Offline support is only supported when downloading direct from this github. 
- Ansible galaxy collection does not include the offline copies of the dependencies

## Requirements:
- Requires you have secure WinRM over HTTPS already configured on your Windows Systems
  - STIGs mandate you have WinRM over HTTPs if you use WinRM. This in mind, this collection enforces changes that enforce WinRM over HTTPs. If you're using plaintext WinRM this collection will break your communication with your windows hosts.
  - Read the following for more information:
    - [Ansible - Setting up a Windows Host](https://docs.ansible.com/ansible/2.5/user_guide/windows_setup.html)
    - [Microsoft - Security Considerations for PowerShell Remoting using WinRM](https://docs.microsoft.com/en-us/powershell/scripting/learn/remoting/winrmsecurity?view=powershell-7.2)
    - [Microsoft - How to configure WINRM for HTTPS](https://docs.microsoft.com/en-us/troubleshoot/windows-client/system-management-components/configure-winrm-for-https)
 - Must be using a domain account for your ansible user
   - UAC is enforced with implementing STIGs and with this Collection
   - With UAC enabled, winrm disallows all local accounts even with specific exceptions 

## Usage:
```bash
```

## Installation:
- [Ansible Galaxy](https://galaxy.ansible.com/simeononsecurity/windows_stigs)
```bash
ansible-galaxy collection install simeononsecurity.windows_stigs
```

## Based on:
- [simeononsecurity/STIG-Compliant-Domain-Prep](https://github.com/simeononsecurity/STIG-Compliant-Domain-Prep)
- [simeononsecurity/Standalone-Windows-STIG-Script](https://github.com/simeononsecurity/Standalone-Windows-STIG-Script)
- [simeononsecurity/Standalone-Windows-Server-STIG-Script](https://github.com/simeononsecurity/Standalone-Windows-Server-STIG-Script)
- [simeononsecurity/Windows-Defender-STIG-Script](https://github.com/simeononsecurity/Windows-Defender-STIG-Script)
- [simeononsecurity/.NET-STIG-Script](https://github.com/simeononsecurity/.NET-STIG-Script)
- [simeononsecurity/FireFox-STIG-Script](https://github.com/simeononsecurity/FireFox-STIG-Script)
- [simeononsecurity/Oracle-JRE-8-STIG-Script](https://github.com/simeononsecurity/Oracle-JRE-8-STIG-Script)
- [simeononsecurity/Adobe-Reader-DC-STIG-Script](https://github.com/simeononsecurity/Adobe-Reader-DC-STIG-Script)
