# 🖥️ Active Directory Home Lab (TryHackMe)

## 📌 Project Overview

This project documents a hands-on Active Directory lab completed on TryHackMe, where I simulated the role of a Domain Administrator in a corporate environment. The lab focused on managing a Windows domain, organizing enterprise resources, and implementing administrative controls using Active Directory Domain Services (AD DS).

The environment was based on a fictional company (**THM Inc.**) with a domain structure of **THM.local**.

---

## 🎯 Objectives

* Understand the fundamentals of Active Directory
* Manage users, groups, and computers within a domain
* Organize and structure Organizational Units (OUs)
* Delegate administrative privileges securely
* Explore enterprise-level domain structures (trees, forests, trusts)

---

## 🧠 Key Concepts

* Active Directory Domain Services (AD DS)
* Domain Controllers (DC)
* Organizational Units (OUs)
* Security Groups vs OUs
* Delegation of Control
* Domain Trees & Forests
* Trust Relationships

---

## 🔧 Lab Tasks & Implementation

### 1️⃣ Domain Access & Exploration

* Connected to a Domain Controller via Remote Desktop Protocol (RDP)
* Authenticated using domain credentials (THM\Administrator)
* Explored the domain structure using **Active Directory Users and Computers (ADUC)**

---

### 2️⃣ User & Group Management

* Reviewed existing domain users and groups
* Created and removed users to match organizational requirements
* Worked with built-in groups such as:

  * Domain Admins
  * Domain Users
  * Domain Computers

---

### 3️⃣ Organizational Unit (OU) Management

* Analyzed company organizational structure
* Created and modified OUs for departments:

  * IT
  * Sales
  * Marketing
  * Management
  * R&D
* Removed deprecated OUs after disabling accidental deletion protection

---

### 4️⃣ Delegation of Administrative Control

* Delegated password reset permissions to a non-admin user (Phillip)
* Used the **Delegate Control Wizard** to assign least-privilege access
* Verified delegation using PowerShell:

```powershell
Set-ADAccountPassword sophie -Reset
Set-ADUser -ChangePasswordAtLogon $true
```

* Successfully reset a user password without Domain Admin privileges

---

### 5️⃣ Device & OU Organization

* Created dedicated OUs for:

  * Workstations
  * Servers
* Moved domain-joined machines from the default **Computers** container
* Improved structure for applying future Group Policies

---

### 6️⃣ Domain Architecture Concepts

* Learned how enterprise environments scale using:

  * Domain Trees (shared namespace)
  * Forests (multiple namespaces)
* Understood how **trust relationships** allow cross-domain access

---

## 🛠️ Tools & Technologies

* Windows Server (Domain Controller)
* Active Directory Users and Computers (ADUC)
* PowerShell
* Remote Desktop Protocol (RDP)

---

## 📸 Screenshots

### TryHackMe Lab Completion

![TryHackMe Completion](tryhackme.png)

* Successfully completed Active Directory lab environment
* Demonstrated hands-on domain administration skills



---

## 🚀 Skills Demonstrated

* Active Directory Administration
* Identity & Access Management (IAM)
* Role-Based Access Control (RBAC)
* Enterprise Network Organization
* Basic Security & Privilege Delegation

---

## 🔗 Future Improvements

* Implement Group Policy Objects (GPOs)
* Perform Active Directory hardening
* Simulate AD attacks (Kerberoasting, BloodHound)
* Expand lab into a full home Active Directory environment

---

## 📬 Summary

This lab demonstrates practical, hands-on experience with Active Directory in a simulated enterprise environment. It highlights my ability to manage users, enforce structure, and apply security principles within a Windows domain—skills directly applicable to IT support, system administration, and SOC analyst roles.
