# Azure Lab Project 2  

This project builds on Project 1 and helped me practice more everyday Azure tasks. I reset a Linux VM password, set a spending budget, made alert rules, created a secure SAS link for storage and used a resource lock to stop accidental deletion.

---

## Overview  

What I Wanted to Do
- Practice dayto day Azure admin tasks instead of just the setup  
- Add monitoring, alerts and cost controls  
- Simulate helpdesk tasks like password resets  
- Secure storage with private containers + SAS links for temporary sharing 
- Test resource protection with a resource lock

---

## Virtual Network  

**Screenshots:**  
- [Associate Subnets](./Azure%20-%20Project%202/Azure%20-%20Virtual%20Network/vnet-associate-subnets.png)  
- [Subnet IP Ranges](./Azure%20-%20Project%202/Azure%20-%20Virtual%20Network/vnet-subnet-ip-ranges.png)  

- Added two subnets (AppSubnet and MgmtSubnet) to keep the app and management traffic separate.  
- Confirmed IP ranges to ensure the network had room for future growth.  

---

## Network Security Group  

**Screenshot:**  
![NSG Deny Rule](./Azure%20-%20Project%202/Azure%20-%20Network%20Security%20Group/nsg-deny-ssh-rule.png)

- Added a Deny SSH rule to block all SSH (port 22) traffic coming from the internet.

---

## Virtual Machine  

**Screenshot:**  
![Reset Password](./Azure%20-%20Project%202/Azure%20-%20Virtual%20Machine/vm-reset-password.png)

- Used the 'Reset Password' option to practice solving a “user can’t log in” ticket. 
- Successfully set a new password and confirmed VM was still accessible.

---

## Storage Account  

**Screenshot:**  
![Generate SAS Link](./Azure%20-%20Project%202/Azure%20-%20Storage%20Account/storage-generate-sas-link.png)

- Created a private container for uploads.
- Generated a read-only SAS link to securely share files with an expiry time. 

---

## Monitoring & Alerts  

**Screenshots:**  
- [Action Group Setup](./Azure%20-%20Project%202/Azure%20-%20Monitoring/action-group-email-alerts-overview.png)  
- [Alert Rule Condition](./Azure%20-%20Project%202/Azure%20-%20Monitoring/alert-rule-condition.png)  
- [Alert Rule Details](./Azure%20-%20Project%202/Azure%20-%20Monitoring/alert-rule-details.png)  
- [CPU Alert Overview](./Azure%20-%20Project%202/Azure%20-%20Monitoring/alert-rule-percentage-cpu-overview.png)

- Created an Action Group that sends notifications to my email.
- Setup a CPU usage alert to notify me if VM CPU usage > 80% for 5 minutes.
- Looked at the alert rule summary screen to get familiar with alert details

---

## Cost Management  

**Screenshot:**  
![Budget Setup](./Azure%20-%20Project%202/Azure%20-%20Cost%20Management/cost-budget-setup.png)

- Set a monthly budget of £5 for my subscription.
- Setup email alerts at 50%, 80% and 100% usage to avoid surprise charges.

---

## Resource Group Lock  

**Screenshots:**  
- [Lock Setup](./Azure%20-%20Project%202/Azure%20-%20Resource%20Group/resource-lock-setup.png)  
- [Delete Blocked Error](./Azure%20-%20Project%202/Azure%20-%20Resource%20Group/rg-delete-error.png)  

- Added a Delete lock to prevent accidental removal of the resource group.
- Tested lock by trying to delete group and seeing the error message.

---

## Key Takeaways  

- Learned how to set up monitoring, spending alerts, and locks to keep my resources safe and under control  
- Practiced common troubleshooting steps like resetting passwords.  
- Improved security with deny rules, private containers and SAS tokens.  
- Strengthened my understanding of Azure governance and cost control features.  

---

## Cleanup  

After validation, I removed the resource group lock and deleted all resources to avoid ongoing costs.  