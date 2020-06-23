# About JuliaRT
Pentest Cyber Range for a small Active Directory Domain.  Automated templates for building your own Pentest/Red Team/Cyber Range in the Azure cloud!  JuliaRT is a small Active Directory enteprise deployment automated with Terraform / Ansible Playbook templates to be deployed in Azure.
# Quick Fun Facts:
* Deploys one (1) Windows 2019 Domain Controller and three (3) Windows 10 Pro Endpoints
* Automatically joins the three Windows 10 computers to the AD Domain
* Uses Terraform templates to automatically deploy in Azure with VMs
* Terraform templates write Ansible Playbook configuration, which can be customized
* Post-deploy Powershell script that adds registry entries on each Windows 10 Pro endpoint to automatically log in each username into the Domain as respective user
* Automatically uploads Badblood (but does not install) if you prefer to generate thousands of simulated users https://github.com/davidprowe/BadBlood
* Post-deployment Powershell script provisions three domain users on the 2019 Domain Controller 
* Domain Users:  olivia (Domain Admin); lars (Domain User); liem (Domain User)
* All Domain User passwords:  Password123
* Domain:  RTC.LOCAL
* Domain Administrator Creds:  RTCAdmin:Password123

# JuliaRT Deployment Instructions
**Note:**  Tested on Ubuntu Linux 20.04 

Requirements:
* Azure subscription
* Terraform:  Tested on v0.12.26
* Ansible:  Tested on 2.9.6

## Installation Steps

**Note:**  Tested on Ubuntu Linux 18.04 built on Digital Ocean.

**Step 1:** Install Terraform and Ansible on your Linux system

Download and install Terraform for your platform --> https://www.terraform.io/downloads.html

Install Ansible
```
$ sudo apt-get install ansible
```
