
A foothold in the lab will be gained by leveraging a file upload function in a web application to upload a PHP web shell. Privileges will then be escalated to svc_mysql, abusing SeManageVolumePrivilege to achieve system access. This lab focuses on *exploiting file upload vulnerabilities and privilege escalation methods*.

## Learning Objectives

**After completion of this lab, learners will be able to:**

- Exploit the file upload functionality to upload a *.htaccess* file and a *PHP web shell*.
- Use the web shell to establish a reverse shell as the svc_apache user.
- Perform a Kerberoasting attack to crack the svc_mssql account password.
- Exploit the SeManageVolumePrivilege to grant full control over the Windows directory.
- Exploit the unrestricted file write privileges to gain SYSTEM-level access and validate control over a vulnerable service. The exploitation of this service must be performed correctly, else a subsequent attack will fail. Please be sure to revert the lab between privilege escalation attempts.

## Lab Description

This lab demonstrates exploiting a file upload vulnerability in a web application to gain initial access by uploading a .htaccess file and a web shell. Learners escalate privileges by leveraging the svc_mssql account's SeManageVolumePrivilege to gain full control over the C: drive, followed by executing a SYSTEM shell using a Windows Error Reporting (WER) exploit. This lab emphasizes web exploitation, Kerberoasting, and privilege escalation through volume management.