## Resource Group  

**Screenshot:**  
![Resource Group Creation](./Azure%20-%20Project%201/Azure%20-%20Resource%20Group/resource-group-creation.png)

- **Name:** `AzureProject-RG`  
- **Region:** UK South  
- This is the container for all project resources which simplifies management and cleanup.  

---

## Virtual Network  

**Screenshots:**  
- [IP Address Space](./Azure%20-%20Project%201/Azure%20-%20Virtual%20Network/vnet-ip-addresses.png)  
- [Tags](./Azure%20-%20Project%201/Azure%20-%20Virtual%20Network/vnet-tags.png)  

- **Name:** `AzureProject-VNet`  
- **Address Space:** `10.0.0.0/16`  
- **Subnet:** `10.0.0.0/24`  
- Created to provide an isolated network for the VM and other resources. I used the environment and lab tags to clearly label my project as a safe, test-only setup so it wouldn't be confused with real work.  

---

## Network Security Group  

**Screenshot:**  
![NSG Rule](./Azure%20-%20Project%201/Azure%20-%20Network%20Security%20Group/secure-ssh-nsg-rule.png)

- **Rule:** Allow SSH (port 22)  
- **Source:** My public IP address only (not open to all)  
- This improves security by restricting SSH access to trusted sources.  

---

## Virtual Machine  

**Screenshots:**  
- [VM Basics](./Azure%20-%20Project%201/Azure%20-%20Virtual%20Machine/vm-basics.png)  
- [VM Disks](./Azure%20-%20Project%201/Azure%20-%20Virtual%20Machine/vm-disk.png)  
- [VM Networking](./Azure%20-%20Project%201/Azure%20-%20Virtual%20Machine/vm-overview.png)  
- [VM Monitoring](./Azure%20-%20Project%201/Azure%20-%20Virtual%20Machine/vm-monitoring.png)  
- [SSH Login](./Azure%20-%20Project%201/Azure%20-%20Virtual%20Machine/vm-ssh-connection-success.png)

- **OS:** Ubuntu Server 22.04 LTS  
- **Size:** Standard B1s (Free Tier eligible)  
- **Authentication:** Password-based login  
- These screenshots show the full setup of an Azure Virtual Machine including the basics, disks, networking and monitoring. I then successfully logged in via SSH.  

---

## Storage Account  

**Screenshots:**  
- [Basics](./Azure%20-%20Project%201/Azure%20-%20Storage%20Account/storage-account-basics.png)  
- [Networking](./Azure%20-%20Project%201/Azure%20-%20Storage%20Account/storage-account-network.png)  
- [Data Protection](./Azure%20-%20Project%201/Azure%20-%20Storage%20Account/storage-account-data-protection.png)  
- [Tags](./Azure%20-%20Project%201/Azure%20-%20Storage%20Account/storage-account-tags.png)

- **Name:** `azureprojectstorage01`  
- **Replication:** Locally Redundant Storage (LRS)  
- **Data Protection:** Enabled blob soft delete, container soft delete and versioning to protect against accidental deletion. Tags added again for easier resource tracking and cost management.  

---

## ARM Templates  

**Files:**  
- [VNet Deployment Template](./Azure%20-%20Project%201/Azure%20-%20Virtual%20Network/vnet-deployment/deployment.json)  
- [VM Deployment Template](./Azure%20-%20Project%201/Azure%20-%20Virtual%20Machine/vm-deployment/deployment.json)  
- [Storage Account Template](./Azure%20-%20Project%201/Azure%20-%20Storage%20Account/storage-account-deployment/deployment.json)  

Exported all resources as ARM templates so the entire lab setup can be quickly redeployed in the future or shared as infrastructure-as-code.