# 🛠️ Helpdesk Password Reset Lab

This lab simulates real-world helpdesk tasks like creating users, resetting passwords, and documenting tickets using Active Directory on Windows Server.

## 🎯 Objectives

- Set up a Windows Server as a Domain Controller
- Create Organizational Units (OUs)
- Add users to departments
- Simulate password reset requests via GUI and PowerShell
- Document actions with a ticket log

## 🧱 Lab Architecture

- Windows Server 2022 (AD DS)
- Optional Windows 10 VM for testing
- Domain: `helpdesklab.local`
- OUs: IT, HR, Finance, Sales

## 🧩 Key Tasks

### ✔️ Create Organizational Units (OUs)
Using Active Directory Users and Computers or PowerShell.

### ✔️ Create Users
Scripted creation of users per department.

### ✔️ Password Reset Simulation
Reset passwords via GUI and PowerShell.

```powershell
Set-ADAccountPassword -Identity "jdoe" `
-NewPassword (ConvertTo-SecureString "NewP@ssword456" -AsPlainText -Force) `
-Reset
