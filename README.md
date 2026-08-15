# YAML Architecture for Kubernetes Pod Manifest

This project provides a native, declarative Infrastructure-as-Code (IaC) configuration manifest to deploy a high-performance Nginx web server pod instance inside an active Kubernetes cluster node runtime environment.

---

## 💻 Kubernetes Configuration Spec (`pod.yaml`)

This schema  is optimized to interface directly with the Kubernetes API Control Plane:

```yaml
apiVersion: v1
kind: Pod
metadata:
  name: nginx-pod          # Globally unique identifier within the cluster namespace
spec:
  containers:
  - name: nginx            # Isolated operational logic name tag
    image: nginx:latest    # Image target pulling from the container hub registry

```
<img width="1458" height="593" alt="image" src="https://github.com/user-attachments/assets/f96034cc-80b0-447a-9f46-edf30980b84b" />


---

## Basic Concepts Applied
*1. API Version*

  ```yaml
apiVersion: v1
```

<img width="287" height="69" alt="image" src="https://github.com/user-attachments/assets/bef2a4d1-a0de-43d2-870f-8bde4ab01718" />




*2. Resource Type*  

```yaml
kind: Pod
```
  
<img width="299" height="101" alt="image" src="https://github.com/user-attachments/assets/4cd4e40b-ba2a-4c05-aa28-4ec607996ac4" />




*3. Parent- child structure*

```yaml
metadata:
  name: nginx-pod          # Globally unique identifier within the cluster namespace
```

<img width="274" height="64" alt="image" src="https://github.com/user-attachments/assets/d475e3fe-9af2-4766-92c8-847092a43415" />




*4. Nested list: array*
    
```yaml
spec:
  containers:
  - name: nginx            # Isolated operational logic name tag
    image: nginx:latest    # Image target pulling from the container hub registry
```

<img width="327" height="101" alt="image" src="https://github.com/user-attachments/assets/cd86aa1e-d456-40d1-ac2b-1aaa20c98d89" />

  The hyphen (-) instantiates a specific container entry, assigning it a unique runtime logging tag

  ---

  
## 🛠️ Architectural Layer and functions

| Architectural Layer | Terminal Execution Command | Functional Operational Description |
|---|---|---|
| API Version | echo "apiVersion: v1" > pod.yaml | Creates a new pod.yaml file (overwriting old content) and inserts the core, stable Kubernetes API schema version. |
| Resource Type | echo "kind: Pod" >> pod.yaml | Appends the resource classification to the file, defining the deployment type as an atomic compute Pod capsule. |
| Resource Metadata | echo "metadata:" >> pod.yaml | Appends the parent organizational block used by the cluster to hold names, tracking labels, and indexing context. |
| Unique Identifier | echo " name: nginx-pod" >> pod.yaml | Appends the unique name identifier string under the metadata layer to locate the running Pod instance within the cluster namespace. |
| Desired State Specification | echo "spec:" >> pod.yaml | Appends the technical engineering blueprint block that defines the target configuration constraints the cluster must actively maintain. |
| Container Manifest Array | echo " containers:" >> pod.yaml | Appends the array list parent indicator that hosts the collection of isolated virtual application workflows inside this Pod. |
| Container Isolation Runtime Name | echo " - name: nginx" >> pod.yaml | Appends a distinct container entry using the hyphen (-) indicator, assigning it a specific runtime tracking tag. |
| Container Registry Image Target | echo " image: nginx:latest" >> pod.yaml | Appends the execution target, instructing the worker node container runtime to pull and execute the newest Nginx server binary package. |
| Print Manifest Verification | cat pod.yaml | Executes a terminal read operation to output the completed configuration file layout to the console for a final structural verification pass. |

---

## 📁 Repository Project Structure

```text
yaml-architecture/
├── .git/               # Initialized local Git version tracking database
├── README.md           # Deployment manual and workspace architecture guide
└── pod.yaml            # Fixed structural declarative Kubernetes manifest
```

---

## 🚀 Version Control & Cluster Operations Guide

These sequential execution steps inside the terminal to sync the codebase and track revisions.

### 📦 1. Repository Initialization & Initial History
These commands initialize workspace database tracker and establish first operational checkpoint save.

* Initialize a blank local Git repository inside the workspace folder:

git init

* Stage the corrected pod.yaml and new README.md files for tracking:

git add pod.yaml README.md

* Review the staging area to verify which new files are ready to be saved:

git status

* Force rename the local timeline tracking branch to the industry-standard name main:

git branch -M main


<img width="1446" height="248" alt="image" src="https://github.com/user-attachments/assets/3a49b878-6fa7-4b2f-9b50-936fb22a67e2" />


### 📁 2. Commit History
* This saves the staged files permanently into the local Git timeline history log:
```powershell
git commit -m "feat: create nginx pod YAML manifest and add documentation"
```
### 🔗 3. Remote Cloud Synchronization
* Link the local repository to the remote public cloud repository layout:
```powershell
git remote add origin https://github.com/Berenice2425/YAML-architecture-for-Kubernetes-Pod-Manifest.git
```

### 🔄 4. Sync Remote Changes and Push
Because the remote cloud repository contains a pre-generated file (a LICENSE), merge the separate timeline histories into one unified track before finalizing the push operation:
```powershell
git pull origin main --allow-unrelated-histories --no-edit
git push -u origin main
```
<img width="1673" height="862" alt="image" src="https://github.com/user-attachments/assets/233fb418-e59a-498d-b222-74926dfada45" />

---


## ⚠️ Essential Schema Engineering Principles

* **Immutable Whitespace Constraints**: YAML blocks rely completely on spatial offsets rather than curly brackets. Avoid typing the Tab key completely; enforce a strict structure using **2 character spaces** for child elements.
*    **The Array Hyphen Protocol (`-`)**: The hyphen preceding `name: nginx` states that this block is an entry within a list array structure (`containers:`). Ensure uniform block spacing around this parameter.
* **Declarative Manifest State**: This manifest defines the ultimate execution goals. When pushed via `kubectl apply -f pod.yaml`, Kubernetes continually drives hardware parameters to align with this configuration baseline.


I cannot directly create a downloadable file, but I have extracted **all questions, correct answers, and brief explanations** from the AZ-104 document. You can copy the content below and paste it into Word, Google Docs, or Notepad to save as your own downloadable document.

---

# AZ-104 EXAM QUESTIONS AND ANSWERS

## Complete Study Guide

---

## TOPIC 1 - QUESTION SET 1

---

### Question #1
**Question:** Your company has several departments with VMs in RG1. How do you associate each VM with its department?

**Answer:** C. Assign tags to the virtual machines.

**Explanation:** Tags are metadata that can be used to logically organize resources. Each resource can have tags applied to identify its department.

---

### Question #2
**Question:** Configure Conditional Access policy requiring Global Administrators to use MFA and Azure AD-joined device from untrusted locations. Solution: Access multi-factor authentication page to alter user settings.

**Answer:** B. No

**Explanation:** Conditional Access policies are configured in the Conditional Access blade, not in the MFA user settings page.

---

### Question #3
**Question:** Same scenario. Solution: Access Azure portal to alter session control of Conditional Access policy.

**Answer:** B. No

**Explanation:** Session controls don't enforce MFA or device requirements. Grant controls are used to require MFA.

---

### Question #4
**Question:** Same scenario. Solution: Access Azure portal to alter grant control of Conditional Access policy.

**Answer:** A. Yes

**Explanation:** Grant controls in Conditional Access policies can require MFA and device compliance.

---

### Question #5
**Question:** Deploy Ubuntu Server with custom trusted root CA. Which command should you use?

**Answer:** D. The az vm create command

**Explanation:** The az vm create command with the --custom-data parameter can deploy VMs with cloud-init scripts for custom configurations.

---

### Question #6
**Question:** Company uses MFA Per Authentication. Need to switch to Per Enabled User for new employees. Solution: Reconfigure existing usage model via Azure portal.

**Answer:** B. No

**Explanation:** You cannot change the usage model of an existing MFA provider. You must create a new provider.

---

### Question #7
**Question:** Same scenario. Solution: Reconfigure existing usage model via Azure CLI.

**Answer:** B. No

**Explanation:** The usage model cannot be changed on an existing provider regardless of the tool used.

---

### Question #8
**Question:** Same scenario. Solution: Create a new MFA provider with backup from existing provider data.

**Answer:** A. Yes

**Explanation:** Creating a new MFA provider is the correct solution since the usage model cannot be changed on an existing provider.

---

### Question #9
**Question:** Hybrid Azure AD with DirSync server. Created new AD user, need immediate replication to Azure AD. Solution: Run Start-ADSyncSyncCycle -PolicyType Initial.

**Answer:** A. Yes

**Explanation:** The Start-ADSyncSyncCycle cmdlet triggers a manual synchronization cycle in Azure AD Connect.

---

### Question #10
**Question:** Same scenario. Solution: Use Active Directory Sites and Services to force replication of Global Catalog.

**Answer:** B. No

**Explanation:** AD Sites and Services replicates within on-premises AD, not to Azure AD. The Azure AD Connect sync cycle is needed.

---

### Question #11
**Question:** Same scenario. Solution: Restart the NetLogon service on a domain controller.

**Answer:** B. No

**Explanation:** Restarting NetLogon doesn't trigger Azure AD synchronization. The Azure AD Connect sync cycle is required.

---

### Question #12
**Question:** Storage redundancy for geo-clustered sites. Requirements: multiple nodes, separate geographic locations, read from secondary.

**Answer:** B. Read-only geo-redundant storage (RA-GRS)

**Explanation:** RA-GRS provides three copies in the primary region and three in the secondary region with read access to the secondary location.

---

### Question #13
**Question:** Review ARM template used by Jon Ross. Solution: Access Virtual Machine blade.

**Answer:** B. No

**Explanation:** The deployment history and template are accessed from the Resource Group blade, not the Virtual Machine blade.

---

### Question #14
**Question:** Same scenario. Solution: Access Resource Group blade.

**Answer:** A. Yes

**Explanation:** The Resource Group blade shows deployment history where you can view the ARM template used.

---

### Question #15
**Question:** Same scenario. Solution: Access Container blade.

**Answer:** B. No

**Explanation:** The Container blade doesn't contain deployment history. The Resource Group blade must be used.

---

### Question #16
**Question:** Three VMs in availability set. VM resize fails with allocation failure. What should you do?

**Answer:** C. Stop all three VMs.

**Explanation:** All VMs in an availability set must be stopped before resizing any VM that requires different hardware.

---

### Question #17
**Question:** Attach data disk to another VM with minimal downtime. What should you do FIRST?

**Answer:** A. Stop the VM that includes the data disk.

**Explanation:** You must stop the VM containing the disk before detaching it. The disk can then be attached to another VM.

---

### Question #18
**Question:** ARM template for VMs in availability set. What value for platformFaultDomainCount to maximize availability?

**Answer:** D. Max Value

**Explanation:** Fault domains represent physical racks. Using the maximum value (2 or 3 depending on region) provides the best protection.

---

### Question #19
**Question:** Same scenario. What value for platformUpdateDomainCount?

**Answer:** B. 20

**Explanation:** Update domains can be increased to up to 20 in Resource Manager deployments. More update domains means fewer VMs rebooted at once.

---

### Question #20
**Question:** ARM template references administrative password. Password cannot be in plain text. What should you create?

**Answer:** Azure Key Vault and an access policy

**Explanation:** Key Vault stores secrets securely. The ARM template retrieves the password from Key Vault, keeping it out of plain text.

---

### Question #21
**Question:** PowerShell scripts to automate VM configuration. What is the best solution?

**Answer:** A. Configure a SetupComplete.cmd batch file in the %windir%\setup\scripts directory.

**Explanation:** The Custom Script Extension or SetupComplete.cmd runs scripts automatically during VM provisioning.

---

### Question #22
**Question:** Upload generalized VM image to Azure. Which PowerShell cmdlet should you use?

**Answer:** B. Add-AzVhd

**Explanation:** The Add-AzVhd cmdlet uploads on-premises VHD files to Azure blob storage.

---

### Question #23
**Question:** Replicate on-premises Hyper-V VM (VM1) to Azure. What objects must be created?

**Answer:** The answer involves creating: Recovery Services vault, replication policy, and enabling replication for VM1.

**Explanation:** Azure Site Recovery requires a Recovery Services vault and replication settings to protect on-premises VMs.

---

### Question #24
**Question:** Point-to-site VPN from Windows 10 to VirtualNetworkA. Can access VNetB from on-premises but not from workstation. Solution: Allow gateway transit on VirtualNetworkA.

**Answer:** B. No

**Explanation:** You must re-download and install the VPN client configuration package after enabling gateway transit.

---

### Question #25
**Question:** Same scenario. Solution: Allow gateway transit on VirtualNetworkB.

**Answer:** B. No

**Explanation:** Gateway transit should be enabled on the peered network that has the gateway (VirtualNetworkA), not on the peered network.

---

### Question #26
**Question:** Same scenario. Solution: Download and re-install VPN client configuration package.

**Answer:** A. Yes

**Explanation:** The VPN client package must be updated to include routes to the peered virtual network.

---

### Question #27
**Question:** Remote workers need access to VMs in VNet1. What should you do?

**Answer:** C. Configure a Point-to-Site (P2S) VPN.

**Explanation:** P2S VPN provides secure connections from individual client computers to an Azure virtual network.

---

### Question #28
**Question:** SQL Server Always On availability group. Configure internal load balancer as listener. Solution: Create HTTP health probe on port 1433.

**Answer:** B. No

**Explanation:** SQL Server Always On availability groups require a custom health probe, typically on a port other than 1433.

---

### Question #29
**Question:** Same scenario. Solution: Set Session persistence to Client IP.

**Answer:** B. No

**Explanation:** For SQL Server Always On, Floating IP must be enabled. Session persistence is not the correct configuration.

---

### Question #30
**Question:** Same scenario. Solution: Enable Floating IP.

**Answer:** A. Yes

**Explanation:** Floating IP (Direct Server Return) must be enabled for SQL Server Always On availability group listeners.

---

### Question #31
**Question:** Two on-premises servers with application calling service by IP. Migrate to Azure VMs, need static internal IP addresses.

**Answer:** E. Run the Set-AzureStaticVNetIP PowerShell cmdlet.

**Explanation:** The Set-AzureStaticVNetIP cmdlet configures a static internal IP address for an Azure VM.

---

### Question #32
**Question:** Deploy 5 VMs with public and private IP addresses. Inbound/outbound security rules identical. Minimum network interfaces needed?

**Answer:** A. 5

**Explanation:** Each VM needs one network interface that can have both public and private IP addresses assigned.

---

### Question #33
**Question:** Deploy 5 VMs with identical security rules. Minimum number of security groups needed?

**Answer:** D. 1

**Explanation:** One network security group can be associated to multiple network interfaces and subnets, applying the same rules.

---

### Question #34
**Question:** VM backed up daily with Azure Backup Instant Restore. VM infected with ransomware. Need to recover files.

**Answer:** A. You can only recover the files to the infected VM.

**Explanation:** File-level recovery from Azure Backup can only restore files to the original VM.

---

### Question #35
**Question:** Same scenario. Need to restore the entire VM.

**Answer:** B. You should restore the VM to any VM within the company's subscription.

**Explanation:** Azure Backup can restore a VM to a new VM or replace the existing VM.

---

### Question #36
**Question:** Performance issues. Need to find cause of metrics on Azure infrastructure. Which tool?

**Answer:** B. Azure Monitor

**Explanation:** Azure Monitor collects and analyzes metrics from Azure resources, making it ideal for performance troubleshooting.

---

### Question #37
**Question:** Schedule backup of VMs to Recovery Services vault. Which VMs can you back up?

**Answer:** ABCDE (All of the above)

**Explanation:** Azure Backup supports Windows Server 2012+, Windows 10, Debian 8.2+, and both running and stopped VMs.

---

### Question #38
**Question:** Create guest user accounts for 500 external users from CSV. Solution: PowerShell with New-AzureADUser.

**Answer:** B. No

**Explanation:** New-AzureADUser creates internal users. New-AzureADMSInvitation is used for guest users.

---

### Question #39
**Question:** Same scenario. Solution: Bulk create user operation.

**Answer:** B. No

**Explanation:** Bulk create is for internal users. Bulk invite is needed for guest users.

---

### Question #40
**Question:** Same scenario. Solution: New-AzureADMSInvitation cmdlet.

**Answer:** A. Yes

**Explanation:** New-AzureADMSInvitation is the correct cmdlet for inviting external guest users.

---

## TOPIC 2 - QUESTION SET 2

---

### Question #1
**Question:** Admin1 needs to manage LB1 and LB2. What role should be assigned?

**Answer:** The role assignments depend on the specific permissions needed. For managing load balancers, Network Contributor or specific load balancer roles are typically used.

**Explanation:** Roles should follow the principle of least privilege - assign only the permissions needed.

---

### Question #2
**Question:** Unable to grant access to AKS cluster to contoso.com users. What should you do first?

**Answer:** B. From contoso.com, create an OAuth 2.0 authorization endpoint.

**Explanation:** AKS uses Azure AD for authentication. OAuth 2.0 endpoints enable Azure AD integration.

---

### Question #3
**Question:** Grant 3 users access to SharePoint document library for 180 days. Which groups should you create?

**Answer:** AC. A Microsoft 365 group that uses Assigned membership type and a Microsoft 365 group that uses Dynamic User membership type.

**Explanation:** Expiration policies can only be set on Microsoft 365 groups. Assigned or Dynamic membership types both work.

---

### Question #4
**Question:** Access review scenario with users and groups. Can User3 perform access review of User1, UserA, UserB?

**Answer:** The answers depend on the specific access review configuration. User3 can review members of Group1 if configured as reviewer.

**Explanation:** Access review settings determine who can perform reviews.

---

### Question #5
**Question:** Management groups and Azure policies scenario. Which statements are true?

**Answer:** Box 1: No (Deny overrides allowed), Box 2: Yes, Box 3: Yes

**Explanation:** Deny policies at higher scopes override allow policies. VMs can be created with proper permissions. Subscriptions can be moved between management groups.

---

### Question #6
**Question:** Azure Policy: Not allowed resource types - Microsoft.Sql/servers. Scope: Subscription1, Exclusions: ContosoRG1.

**Answer:** B. You can create Azure SQL servers in ContosoRG1 only.

**Explanation:** The policy prevents SQL server creation everywhere except the excluded resource group.

---

### Question #7
**Question:** Tags and policies for VNET1 and VNET2. Which tags apply?

**Answer:** VNET1: Department: D1 and Label:Value1. VNET2: Label:Value1 only.

**Explanation:** Tags applied to resource groups aren't inherited by resources. VNET1 has its own tag. VNET2 gets the policy-applied tag.

---

### Question #8
**Question:** Admin1 fails to deploy Marketplace resource. Error: Legal terms not accepted. What should you do?

**Answer:** C. From Azure PowerShell, run the Set-AzMarketplaceTerms cmdlet.

**Explanation:** The Set-AzMarketplaceTerms cmdlet accepts legal terms for Marketplace items programmatically.

---

### Question #9
**Question:** Assign User Administrator role to AdminUser1. What should you do from user account properties?

**Answer:** B. From the Directory role blade, modify the directory role.

**Explanation:** Directory roles are assigned from the Directory role blade of the user's properties.

---

### Question #10
**Question:** Purchase 10 Azure AD Premium P2 licenses. Need 10 users to use Azure AD Premium features.

**Answer:** A. From the Licenses blade of Azure AD, assign a license.

**Explanation:** Licenses are assigned to users from the Licenses blade in Azure AD.

---

### Question #11
**Question:** Set alert in Service Manager when VM1 memory below 10%. What should you do first?

**Answer:** C. Deploy the IT Service Management Connector (ITSM).

**Explanation:** ITSM Connector integrates Azure alerts with System Center Service Manager.

---

### Question #12
**Question:** Add admin1@contoso.com as administrator on all Azure AD joined computers. What should you configure?

**Answer:** A. Device settings from the Devices blade.

**Explanation:** Additional local administrators on Azure AD joined devices are configured in Device settings.

---

### Question #13
**Question:** Device and group configuration scenario. Which statements are true?

**Answer:** Box 1: Yes (Cloud Device Administrator can manage Azure AD joined devices), Box 2: No (User Administrator cannot manage Azure AD registered devices)

**Explanation:** Device administrator roles have specific permissions based on device join type.

---

### Question #14
**Question:** Provide Developers group ability to create logic apps in Dev resource group. Solution: Assign DevTest Labs User role.

**Answer:** B. No

**Explanation:** DevTest Labs User only manages VMs. Logic App Contributor is needed for logic apps.

---

### Question #15
**Question:** Same scenario. Solution: Assign Logic App Operator role.

**Answer:** B. No

**Explanation:** Logic App Operator can only view and run logic apps. Logic App Contributor can create them.

---

### Question #16
**Question:** Same scenario. Solution: Assign Contributor role on Dev resource group.

**Answer:** A. Yes

**Explanation:** Contributor has full management permissions on resources, including creating logic apps.

---

### Question #17
**Question:** Send cost report to finance department by department. What three actions in sequence?

**Answer:** 1. Assign a tag to each resource, 2. From Cost analysis blade, filter by tag, 3. Download the usage report.

**Explanation:** Tags categorize resources by department. Cost analysis can filter by tags. Reports can be exported.

---

### Question #18
**Question:** Query error events from Event table in Log Analytics. Which query to run?

**Answer:** B. Event | search "error"

**Explanation:** The search operator provides multi-table/multi-column search capabilities.

---

### Question #19
**Question:** ARM template deploying VMs to zones. VM1 and VM2 can connect to VNET1?

**Answer:** Box 1: Yes, Box 2: Yes, Box 3: No

**Explanation:** VMs in the same VNet can connect. Availability zones protect against datacenter failure, not region failure.

---

### Question #20
**Question:** Move WebApp1 from RG1 to RG2. What is the effect?

**Answer:** A. The App Service plan remains in West Europe. Policy2 applies to WebApp1.

**Explanation:** App Service plans are region-bound and can't move regions. Policies are inherited from the new resource group.

---

### Question #21
**Question:** Create custom RBAC role CR1 for Subscription1 resource groups. What should be in assignable scopes and permissions?

**Answer:** Assignable Scopes: /subscriptions/[SubscriptionID]/resourceGroups/*. Permissions: "Microsoft.Resources/*"

**Explanation:** The role must be scoped to resource groups and include permissions for all resource management.

---

### Question #22
**Question:** Spread connections to App1 across VMs. Which two services can you use?

**Answer:** AE. An internal load balancer and An Azure Application Gateway.

**Explanation:** Both internal load balancer and Application Gateway can distribute traffic across VMs.

---

### Question #23
**Question:** Identify underutilized VMs for cost optimization. Which blade should you use?

**Answer:** B. Advisor

**Explanation:** Azure Advisor provides cost recommendations including underutilized resources.

---

### Question #24
**Question:** Conditional Access policy requiring MFA for Azure portal access. Which settings to configure?

**Answer:** Name: Policy1, Assignments: Users and groups, Cloud apps: Azure portal, Access controls: Grant - Require MFA

**Explanation:** Conditional Access policies require assignments (who, what) and access controls (how).

---

### Question #25
**Question:** Admin1 unable to invite external partner. Error: "Generic authorization exception." What should you do?

**Answer:** A. From the Users settings blade, modify the External collaboration settings.

**Explanation:** External collaboration settings control guest user invitations.

---

### Question #26
**Question:** Ensure User1 can assign policy to tenant root management group. What should you do?

**Answer:** B. Assign Owner role for Azure subscription to User1, then instruct User1 to configure access management.

**Explanation:** The User Access Administrator role at the root management group level is needed to assign policies.

---

### Question #27
**Question:** Dynamic group membership for User1 and User2. Which groups are they members of?

**Answer:** User1: Group1 only. User2: Group1 and Group2.

**Explanation:** Dynamic group rules evaluate user attributes (city and department) to determine membership.

---

### Question #28
**Question:** Modify JobTitle and UsageLocation for users from different sources.

**Answer:** User1 and User3 only for JobTitle. User1, User2, and User3 for UsageLocation.

**Explanation:** On-premises AD users must be modified on-premises. Azure AD users can be modified in Azure AD.

---

### Question #29
**Question:** Assign role for Traffic Analytics. Solution: Network Contributor role.

**Answer:** A. Yes

**Explanation:** Network Contributor is one of the roles that can enable Traffic Analytics.

---

### Question #30
**Question:** Assign role for Traffic Analytics. Solution: Owner role.

**Answer:** A. Yes

**Explanation:** Owner has full permissions and can enable Traffic Analytics.

---

### Question #31
**Question:** Assign role for Traffic Analytics. Solution: Reader role.

**Answer:** A. Yes

**Explanation:** Reader is one of the roles that can enable Traffic Analytics.

---

### Question #32
**Question:** User1 needs to deploy VMs and manage virtual networks with least privilege. Which RBAC role?

**Answer:** C. Contributor

**Explanation:** Contributor can manage all resources but cannot assign roles. This provides the needed permissions with least privilege.

---

### Question #33
**Question:** Azure AD tenant with 3 global admins. Subscription access control configured. Can Admin1 assign ownership?

**Answer:** Box 1: No, Box 2: Yes, Box 3: No

**Explanation:** Only the Owner can assign ownership. Global admins don't have automatic subscription permissions.

---

### Question #34
**Question:** Service on VM1 needs to manage resources in RG1 using VM1's identity. What should you do first?

**Answer:** A. From the Azure portal, modify the Managed Identity settings of VM1.

**Explanation:** Managed Identity must be enabled on VM1 before it can be assigned permissions.

---

### Question #35
**Question:** Delete TestRG containing VM1, Vault1, and VNET1 with Delete lock. What should you do first?

**Answer:** B. Remove the resource lock from VNET1 and delete all data in Vault1.

**Explanation:** Locks must be removed before deletion. Backup data in Vault1 must be deleted before the vault can be deleted.

---

### Question #36
**Question:** Delegate subdomain research.adatum.com to different DNS server. What should you do?

**Answer:** A. Create an NS record named research in the adatum.com zone.

**Explanation:** NS records delegate DNS authority for a subdomain.

---

### Question #37
**Question:** Add custom domain name to Azure AD. What three actions in sequence?

**Answer:** 1. Add custom domain name to directory, 2. Add DNS entry at registrar, 3. Verify custom domain name.

**Explanation:** Azure AD requires verification of custom domain ownership through DNS records.

---

### Question #38
**Question:** Query error events from Event table. Which query to run?

**Answer:** B. Event | search "error"

**Explanation:** The search operator provides multi-table/multi-column search capabilities.

---

### Question #39
**Question:** Public Azure DNS zone contoso.com created. Need records resolvable from internet. What should you do?

**Answer:** D. Modify the NS records in the DNS domain registrar.

**Explanation:** The domain registrar must delegate the zone to Azure DNS name servers.

---

### Question #40
**Question:** Storage account with Azure Files identity-based authentication. Can assign roles to User1, Computer1, User2?

**Answer:** Yes for User1 and Computer1 (AD synced), No for User2 (Azure AD only)

**Explanation:** Azure Files supports AD DS authentication for AD-joined identities. Azure AD only users need different authentication.

---

### Question #41
**Question:** Subnet creation permissions. Which user can create subnets?

**Answer:** User1 (Owner) and User3 (Network Contributor)

**Explanation:** Owner and Network Contributor can manage network resources.

---

### Question #42
**Question:** Locks and tags - which resources can have locks and tags applied?

**Answer:** Locks: Sub1, RG1, and VM1 only. Tags: Sub1, RG1, and VM1 only.

**Explanation:** Locks and tags can be applied to subscriptions, resource groups, and resources.

---

### Question #43
**Question:** Bulk delete users. Which user attributes should be included in the file?

**Answer:** B. The user principal name of each user only.

**Explanation:** User principal name is the required attribute for bulk delete operations.

---

### Question #44
**Question:** Azure Policy with tags. Which tags apply to RG1, Storage1, VNET1?

**Answer:** RG1: Tag2:IT and Tag4:value4. Storage1: Tag1:subscription, Tag2:IT, Tag3:value1, Tag4:value4. VNET1: Tag3:value2 only.

**Explanation:** Policy appends tags to resources within scope. VNET1 is excluded from the policy.

---

### Question #45
**Question:** Assign role for Traffic Analytics. Solution: Traffic Manager Contributor.

**Answer:** B. No

**Explanation:** Traffic Manager Contributor doesn't enable Traffic Analytics. Network Contributor, Owner, or Reader is needed.

---

### Question #46
**Question:** Grant user management permissions to local administrator in each office. What should you use?

**Answer:** B. Administrative units

**Explanation:** Administrative units scope Azure AD role permissions to specific organizational units.

---

### Question #47
**Question:** Provide Developers group ability to create logic apps. Solution: Logic App Contributor role.

**Answer:** A. Yes

**Explanation:** Logic App Contributor can create and manage logic apps.

---

### Question #48
**Question:** User1 assignments with User Access Administrator and Virtual Machine Contributor roles. What can User1 do?

**Answer:** User1 can assign roles to LB1 and modify the resource group.

**Explanation:** User Access Administrator can assign roles at the resource scope. Virtual Machine Contributor applies to resources in the resource group.

---

### Question #49
**Question:** Ensure User1 can assign Reader role for VNet1. What should you do?

**Answer:** B. Assign User1 the Owner role for VNet1.

**Explanation:** Owner or User Access Administrator role is needed to assign roles to others.

---

### Question #50
**Question:** Custom role1 configuration. To allow VM sign-in and restrict to RG1, which sections to modify?

**Answer:** roletype for sign-in, assignableScopes for RG1 restriction.

**Explanation:** roletype determines login permissions. assignableScopes limits where the role can be assigned.

---

### Question #51
**Question:** Grant Group1 Storage File Data SMB Share Elevated Contributor role for share1. What should you do first?

**Answer:** A. Enable Active Directory Domain Service (AD DS) authentication for storage1.

**Explanation:** AD DS authentication must be enabled before assigning Azure AD-based roles to file shares.

---

### Question #52
**Question:** Ensure Group1 can manage role assignments for existing and planned subscriptions with least privilege.

**Answer:** B. Assign Group1 the User Access Administrator role for the root management group.

**Explanation:** User Access Administrator at the root management group enables role management for all subscriptions.

---

### Question #53
**Question:** Assign Policy1. Which resources can you assign policy to and which can you exclude?

**Answer:** Assign to: Tenant Root Group, ManagementGroup1, Subscription1, RG1, and VM1. Exclude: ManagementGroup1, Subscription1, RG1, and VM1.

**Explanation:** Policies can be assigned at any scope. Exclusions can be at lower scopes.

---

### Question #54
**Question:** User1 creates external tenant. Need to create user accounts. Who can do this?

**Answer:** User2 only (Global Administrator)

**Explanation:** Only Global Administrators can create users in a new Azure AD tenant.

---

### Question #55
**Question:** Custom role with assignable scope to RG1. Need to apply to any resource group in Sub1 and Sub2.

**Answer:** A. Select custom role and add Sub1 and Sub2 to assignable scopes. Remove RG1.

**Explanation:** Assignable scopes can be modified to include entire subscriptions.

---

### Question #56
**Question:** User1 assignments for storageacc1234. Which actions can User1 perform?

**Answer:** BD. Upload blob data and View blob data.

**Explanation:** Storage Blob Data Contributor allows read/write to blob data. Reader allows view.

---

### Question #57
**Question:** Query error events from Event table. Which query to run?

**Answer:** B. Event | search "error"

**Explanation:** The search operator provides multi-table/multi-column search capabilities.

---

### Question #58
**Question:** Developers need to deploy to App1 using Azure AD credentials with least privilege.

**Answer:** C. Assign the Website Contributor role to the developers.

**Explanation:** Website Contributor can deploy content to web apps.

---

### Question #59
**Question:** Create guest user accounts from CSV. Solution: Bulk invite users operation.

**Answer:** B. No

**Explanation:** Bulk invite is the correct operation for guest users, not bulk create.

---

### Question #60
**Question:** Create custom roles Role3 (Azure subscription) and Role4 (Azure AD role). Which roles can you clone?

**Answer:** Role3 from existing Azure subscription role, Role4 from existing Azure AD role.

**Explanation:** Azure subscription roles and Azure AD roles are different types with different cloning capabilities.

---

### Question #61
**Question:** Assign RBAC roles to User1 and User2 for storage accounts.

**Answer:** User1: Storage Blob Data Reader or Reader, User2: User Access Administrator or Owner.

**Explanation:** User1 needs read access. User2 needs role assignment permissions.

---

### Question #62
**Question:** VMs need to access Vault1. NSG blocks outbound internet traffic. Least privilege solution?

**Answer:** B. A service tag

**Explanation:** Service Tag for Azure Key Vault allows VMs to access Key Vault without internet access.

---

### Question #63
**Question:** License assignment to Group1 and User4. Which users get the license?

**Answer:** B. User1 and User4 only

**Explanation:** License assignment to Group1 applies only to direct members of Group1, not nested members.

---

### Question #64
**Question:** External user lifecycle settings for access package. Can litwareinc users be assigned? After 365 days, removed from Group1? After 395 days, removed from tenant?

**Answer:** Yes, Yes, Yes (based on the specific configuration)

**Explanation:** Connected organizations and lifecycle settings control external user access.

---

### Question #65
**Question:** Ensure User1 can assign Reader role for VNet1. What should you do?

**Answer:** C. Assign User1 the Owner role for VNet1.

**Explanation:** Owner or User Access Administrator role is needed to assign roles to others.

---

### Question #66
**Question:** Group membership and role assignment for RG1. Can User2 and User3 be assigned Owner role?

**Answer:** User2 can be assigned by adding Group2 to Group1. User3 cannot be assigned.

**Explanation:** Security groups can be nested for RBAC assignments. Microsoft 365 groups cannot be used for RBAC.

---

### Question #67
**Question:** Ensure User1 can assign Reader role for VNet1. What should you do?

**Answer:** B. Assign User1 the Owner role for VNet1.

**Explanation:** Owner or User Access Administrator role is needed to assign roles to others.

---

### Question #68
**Question:** Ensure traffic from VM1 to storage1 travels across Microsoft backbone. What should you configure?

**Answer:** B. private endpoints

**Explanation:** Private endpoints connect resources to Azure services over the Microsoft backbone network.

---

### Question #69
**Question:** User1 role assignments for NSG1. Can User1 modify NSG1, associate NSG1 to VM1, and assign roles?

**Answer:** Based on specific role assignments, the answers vary.

**Explanation:** Permissions depend on the combination of role assignments at different scopes.

---

### Question #70
**Question:** Ensure User1 can assign Reader role for VNet1. What should you do?

**Answer:** B. Assign User1 the Access Administrator role for VNet1.

**Explanation:** User Access Administrator or Owner role is needed to assign roles to others.

---

### Question #71
**Question:** Management group role assignments for Sub1 and Sub2. Can Group1 view Azure functions? Can User1 assign Owner role? Can User1 create resource group and deploy VM?

**Answer:** Yes, Yes, No (depending on specific permissions)

**Explanation:** Role assignments at management group level apply to all subscriptions in the group.

---

### Question #72
**Question:** Assign Storage File Data SMB Share Contributor role for share1. What should you do first?

**Answer:** A. Enable identity-based data access for file shares in storage1.

**Explanation:** Identity-based authentication must be enabled before assigning Azure AD roles to file shares.

---

### Question #73
**Question:** Ensure User1 can assign Reader role for VNet1. What should you do?

**Answer:** B. Assign User1 the User Access Administrator role for VNet1.

**Explanation:** User Access Administrator or Owner role is needed to assign roles to others.

---

### Question #74
**Question:** License assignment to Group1. Can User1 be assigned Microsoft Defender for Cloud Apps license? Can User2 be assigned Azure AD Premium P2?

**Answer:** No, Yes (depending on license inheritance)

**Explanation:** License assignment to Group1 applies to direct members. Group2 members may inherit through group nesting.

---

## TOPIC 3 - QUESTION SET 3 (STORAGE)

---

### Question #1
**Question:** Azure Import/Export service to export data. Which storage account can be used?

**Answer:** D. storage4

**Explanation:** Export supports Blob storage accounts. storage4 is a BlobStorage account.

---

### Question #2
**Question:** Storage accounts with different configurations. Which support lifecycle management?

**Answer:** storageaccount1 and storageaccount2 only

**Explanation:** Lifecycle management is supported on General Purpose v2 and Blob Storage accounts.

---

### Question #3
**Question:** Export data using Azure Import/Export job. Which data can be exported?

**Answer:** B. container1

**Explanation:** Import/Export supports export of blob data only.

---

### Question #4
**Question:** App1 and App2 need to read blobs from storage1. Minimize secrets, App2 access for 30 days.

**Answer:** App1: Managed Identity with Reader role. App2: Managed Identity with Reader role and time-limited SAS token.

**Explanation:** Managed identities eliminate secrets. SAS tokens can be time-limited.

---

### Question #5
**Question:** Create storage account with hot, cool, archive tiers and disaster protection. Minimize costs.

**Answer:** StorageV2 with Standard_GRS

**Explanation:** StorageV2 supports all tiers. GRS provides cross-region disaster protection.

---

### Question #6
**Question:** Sync files from file share to on-premises Server1. Which three actions?

**Answer:** BCE. Install Azure File Sync agent, Register Server1, Create a sync group.

**Explanation:** Azure File Sync requires agent installation, server registration, and sync group creation.

---

### Question #7
**Question:** Azure Policy with exclusions. Can create VM and VNet in excluded resources?

**Answer:** No, Yes (based on the specific exclusions)

**Explanation:** Exclusions prevent policy application to specific resources.

---

### Question #8
**Question:** Transfer data using Azure Import/Export service. Correct order of actions?

**Answer:** 1. Attach external disk and run waimportexport.exe, 2. Create import job in portal, 3. Detach disks and ship to Azure, 4. Update import job with tracking number.

**Explanation:** The Import/Export process involves preparing drives, creating a job, shipping, and tracking.

---

### Question #9
**Question:** Azure File Sync with group and endpoints. Can add share2 as cloud endpoint? Can add Server2 endpoints?

**Answer:** No (only one cloud endpoint per group), Yes (multiple server endpoints allowed)

**Explanation:** A sync group can have only one cloud endpoint but multiple server endpoints.

---

### Question #10
**Question:** UNC path for Azure file share script. Which values to use?

**Answer:** \\contosostorage.file.core.windows.net\data

**Explanation:** Azure file shares use the format \\[storageaccount].file.core.windows.net\[sharename].

---

### Question #11
**Question:** Copy VM image to container vimages. Which command should you run?

**Answer:** The command uses AzCopy or Azure CLI to copy the VHD to the container.

**Explanation:** The specific command depends on the tool being used.

---

### Question #12
**Question:** Azure File Sync with cloud tiering. File1 and File2 availability on endpoints.

**Answer:** File1 on all endpoints, File2 on server endpoints only.

**Explanation:** Cloud tiering affects how files are cached locally.

---

### Question #13
**Question:** Storage account firewall and virtual network settings. VM connectivity to file shares, Azure Backup access.

**Answer:** Never for both.

**Explanation:** Firewall rules restrict access. Trusted Microsoft services must be enabled for Azure Backup.

---

### Question #14
**Question:** Azure File Sync with cloud endpoint. File1.txt, File2.txt on endpoints.

**Answer:** File1.txt on all endpoints, File2.txt on server endpoints only.

**Explanation:** Files from cloud endpoints sync to all endpoints. Server endpoint files sync to other server endpoints.

---

### Question #15
**Question:** Convert storage account to ZRS replication by live migration. Which account?

**Answer:** B. storage2 (Standard General Purpose v2 with LRS)

**Explanation:** Live migration to ZRS is supported for standard GPv2 accounts with LRS replication.

---

### Question #16
**Question:** Upload disk files from on-premises network (131.107.1.0/24) to storage account for VM1 in VNet1.

**Answer:** AE. Select Selected networks, add VNet1 service endpoint.

**Explanation:** Selected networks restricts access. Service endpoint secures VNet access.

---

### Question #17
**Question:** Synchronize files from Server1 to Azure File Sync. Three actions in sequence?

**Answer:** 1. Install Azure File Sync agent, 2. Register Server1, 3. Add server endpoint.

**Explanation:** The process requires agent installation, server registration, and endpoint configuration.

---

### Question #18
**Question:** Create storage account with synchronous replication and availability during datacenter failure.

**Answer:** Zone-redundant storage (ZRS) with StorageV2

**Explanation:** ZRS replicates synchronously across availability zones. Only GPv2 supports ZRS.

---

### Question #19
**Question:** Azure Import/Export to copy files. Which two files should you create?

**Answer:** BE. A dataset CSV file and a driveset CSV file.

**Explanation:** Dataset CSV specifies files to import. Driveset CSV specifies drives to use.

---

### Question #20
**Question:** Delete Recovery Services vault with protected VMs. What should you do first?

**Answer:** D. From the Recovery Service vault, stop the backup of each backup item.

**Explanation:** Backup must be stopped and data deleted before a vault can be deleted.

---

### Question #21
**Question:** Resources that can be backed up to Vault1 and Vault2.

**Answer:** Vault1: VM1 only. Vault2: Share1 only.

**Explanation:** Vaults must be in the same region as the resources they protect.

---

### Question #22
**Question:** Azure Import/Export destination for 5 TB of data. What can you use?

**Answer:** C. Azure File Storage

**Explanation:** Import/Export can import to Azure Blob Storage and Azure Files.

---

### Question #23
**Question:** Storage account with LRS. Minimum number of copies? Reduce cost for infrequently accessed data?

**Answer:** 3 copies, modify Access tier.

**Explanation:** LRS maintains 3 copies. Changing from Hot to Cool tier reduces cost.

---

### Question #24
**Question:** Use AzCopy to copy data to storage1. Which storage services can you copy to?

**Answer:** B. blob and file only

**Explanation:** AzCopy supports blob and file storage services only.

---

### Question #25
**Question:** Use AzCopy to copy data to blob and file storage. Which authentication methods?

**Answer:** Blob: Azure AD, access keys, and SAS. File: Access keys and SAS only.

**Explanation:** Azure AD authentication is supported for blob but not file storage with AzCopy.

---

### Question #26
**Question:** Container instance with SQL Server requiring persistent storage. What should you use?

**Answer:** A. Azure Files

**Explanation:** Azure Files provides persistent storage that can be mounted to container instances.

---

### Question #27
**Question:** App1 on VM1 and VM2. Availability during planned maintenance. What to include in Availability Set?

**Answer:** D. two update domains

**Explanation:** Update domains ensure VMs aren't rebooted simultaneously during planned maintenance.

---

### Question #28
**Question:** Azure Import/Export destination for 5 TB of data. What can you use?

**Answer:** B. Azure Blob storage

**Explanation:** Import/Export can import to Azure Blob Storage and Azure Files.

---

### Question #29
**Question:** Prepare subscription for Azure File Sync. Which two actions in Azure subscription?

**Answer:** Create a Storage Sync Service, Install the Azure File Sync agent.

**Explanation:** Storage Sync Service is the management resource. Agent is installed on servers.

---

### Question #30
**Question:** Azure File Sync group Sync1 with cloud endpoint. Can add share3? Can add data2 and data3?

**Answer:** No (only one cloud endpoint), Yes for data2, No for data3.

**Explanation:** Sync groups have one cloud endpoint. Server endpoints require registered servers.

---

### Question #31
**Question:** Configure Azure Backup reports for Vault1. Which storage accounts and Log Analytics workspaces?

**Answer:** storage1, storage2, storage3 for storage. Analytics3 for workspace.

**Explanation:** Storage accounts and workspaces must be in the same region as the vault.

---

### Question #32
**Question:** Storage accounts with different types and tiers. Which support file shares and blob tiering?

**Answer:** contoso104 for file shares (FileStorage). contoso101, 102, 103 for blob tiering.

**Explanation:** FileStorage accounts are for premium file shares. GPv2 and BlobStorage support tiering.

---

### Question #33
**Question:** SAS token with IP restrictions. Access from 193.77.134.1 on Sept 2 and 193.77.134.50 on Sept 10.

**Answer:** No access on Sept 2. Read, write, and list access on Sept 10.

**Explanation:** IP restrictions apply. File shares can use SAS for authentication.

---

### Question #34
**Question:** VM2 backed up to RSV1. Need to back up to RSV2. What should you do first?

**Answer:** C. From the VM2 blade, click Disaster recovery, click Replication settings, select RSV2.

**Explanation:** Disaster recovery settings control the vault used for backup.

---

### Question #35
**Question:** General-purpose v1 storage account with LRS. Protect data if zone fails. Minimize cost and effort.

**Answer:** C. Upgrade the account to general-purpose v2.

**Explanation:** Only GPv2 accounts support zone-redundant storage.

---

### Question #36
**Question:** Storage accounts and lifecycle management rules. Which accounts can apply lifecycle management?

**Answer:** D. storage1, storage2, and storage3 only.

**Explanation:** Lifecycle management is supported on GPv2, BlobStorage, and BlockBlobStorage accounts.

---

### Question #37
**Question:** Map drive to Azure file share from Windows 10. Which outbound port should be open?

**Answer:** C. 445

**Explanation:** SMB protocol requires TCP port 445 for file share access.

---

### Question #38
**Question:** Azure Import/Export destination for 5 TB of data. What can you use?

**Answer:** A. Azure File Storage

**Explanation:** Import/Export can import to Azure Blob Storage and Azure Files.

---

### Question #39
**Question:** ARM template for storage account. Can server with IP 131.107.103.10 access? Can blobs use archive tier? Can global admins access file share with Azure AD?

**Answer:** No, Yes, No (based on template settings)

**Explanation:** defaultAction is Allow, so any IP can access. Archive tier is supported. Azure AD auth not enabled.

---

### Question #40
**Question:** Which devices can use AzCopy to copy data to storage1?

**Answer:** B. Device1, Device2, and Device3

**Explanation:** AzCopy is available for Windows, Linux, and macOS.

---

### Question #41
**Question:** Prevent new content in container1 from being modified for one year. What should you configure?

**Answer:** B. an access policy

**Explanation:** Immutable storage policies prevent modification for specified retention periods.

---

### Question #42
**Question:** Lifecycle management rules for container1. File1.docx status on specific dates.

**Answer:** Based on the specific rule configuration, files move to archive and are deleted.

**Explanation:** Lifecycle rules move blobs through tiers based on last modification time.

---

### Question #43
**Question:** Configure Azure AD authentication for storage1. Group1 needs to upload files with least privilege.

**Answer:** BC. Storage Blob Data Contributor and Reader.

**Explanation:** Data contributor grants write access. Reader is needed for Azure portal navigation.

---

### Question #44
**Question:** Create new storage account for object replication. How to configure?

**Answer:** General Purpose v2 with same region as source.

**Explanation:** Object replication requires source and destination accounts to be GPv2 in the same region.

---

### Question #45
**Question:** Copy contents of D:\Folder1 to public container. Which command?

**Answer:** C. azcopy copy D:\folder1 https://contosodata.blob.core.windows.net/public -recursive

**Explanation:** The azcopy copy command with -recursive copies directories.

---

### Question #46
**Question:** Create storage1 with BlockBlobStorage account kind. Which setting to modify first?

**Answer:** A. Performance

**Explanation:** BlockBlobStorage requires Premium performance tier.

---

### Question #47
**Question:** AzCopy to copy blob from container1 to share1. Which authentication methods?

**Answer:** SAS token for both.

**Explanation:** Azure AD auth is supported for blob but not file shares with AzCopy.

---

### Question #48
**Question:** Use different key to encrypt data at rest for one container. What should you do?

**Answer:** D. Create an encryption scope.

**Explanation:** Encryption scopes allow different encryption keys per container.

---

### Question #49
**Question:** Lifecycle management rules for File1 and File2. On June 6 and June 16, where are files?

**Answer:** File1 in Archive on June 6 (moved after 3 days). File2 deleted on June 16 (deleted after 10 days).

**Explanation:** Lifecycle rules apply based on last modification time.

---

### Question #50
**Question:** ARM template for storage1. Can changes be rolled back? Only East US users connect? Three copies maintained?

**Answer:** No, No, Yes.

**Explanation:** Versioning is enabled (7 days). NetworkACLs allows all networks. LRS maintains 3 copies.

---

### Question #51
**Question:** Copy contents of D:\Folder1 to public container. Which command?

**Answer:** C. azcopy copy D:\folder1 https://contosodata.blob.core.windows.net/public -recursive

**Explanation:** The azcopy copy command with -recursive copies directories.

---

### Question #52
**Question:** Lifecycle management rule to move blobs to lowest-cost tier after 90 days.

**Answer:** Archive tier after 90 days.

**Explanation:** Archive tier has the lowest storage cost for infrequently accessed data.

---

### Question #53
**Question:** Back up VM1 with backups stored across three availability zones. Three actions in sequence?

**Answer:** 1. Create Recovery Services vault, 2. Set Replication to Zone-redundant storage (ZRS), 3. Create backup policy and configure backup.

**Explanation:** ZRS replicates backups across availability zones.

---

### Question #54
**Question:** Azure Import/Export destination for 5 TB of data. What can you use?

**Answer:** B. Azure File Storage

**Explanation:** Import/Export can import to Azure Blob Storage and Azure Files.

---

### Question #55
**Question:** Tasks with Azure Storage Explorer. Which tasks can you perform?

**Answer:** D. Task2, Task3, and Task4 only.

**Explanation:** Storage Explorer can manage containers, file shares, and tables but cannot create storage accounts.

---

### Question #56
**Question:** RA-GRS account contoso2023. Need User1 to write blob data and account to fail over to secondary.

**Answer:** Assign Storage Blob Data Contributor role and enable account failover.

**Explanation:** Data contributor allows writing. Account failover switches to secondary region.

---

### Question #57
**Question:** Customer-managed key encryption for container1. Which key should you use?

**Answer:** E. RSA key type with key size of 2048, 3072, or 4096.

**Explanation:** Azure Storage supports RSA keys with sizes 2048, 3072, or 4096 for customer-managed encryption.

---

### Question #58
**Question:** User1 roles and SAS permissions. Which resources can User1 write to?

**Answer:** Based on roles and SAS permissions, specific resources are accessible.

**Explanation:** RBAC roles and SAS permissions combine to determine access.

---

### Question #59
**Question:** Storage account exhibit. Statements about the account.

**Answer:** Based on the account configuration shown.

**Explanation:** Account settings determine capabilities and access.

---

### Question #60
**Question:** Azure Import/Export destination for 5 TB of data. What can you use?

**Answer:** A. Azure Blob Storage

**Explanation:** Import/Export can import to Azure Blob Storage and Azure Files.

---

### Question #61
**Question:** Lifecycle management rules for File1. State on June 7.

**Answer:** D. deleted

**Explanation:** Multiple rules apply. The delete rule takes effect after 5 days.

---

### Question #62
**Question:** Storage accounts with different types and redundancy. Which support lifecycle management and Archive tier?

**Answer:** storage1 and storage3 for lifecycle management. storage1 and storage3 for Archive tier.

**Explanation:** GPv2 and BlockBlobStorage support lifecycle management and Archive tier.

---

### Question #63
**Question:** Azure Import/Export destination for 5 TB of data. What can you use?

**Answer:** C. Azure Blob storage

**Explanation:** Import/Export can import to Azure Blob Storage and Azure Files.

---

### Question #64
**Question:** Lifecycle rule to move blobs not updated for 45 days to Cool tier.

**Answer:** Rule applies to base blobs, last modified > 45 days, move to cool storage.

**Explanation:** Lifecycle rules can move blobs to lower-cost tiers based on age.

---

### Question #65
**Question:** Azure Import/Export destination for 5 TB of data. What can you use?

**Answer:** B. Azure Blob Storage

**Explanation:** Import/Export can import to Azure Blob Storage and Azure Files.

---

### Question #66
**Question:** Storage account for file share supporting SMB Multichannel. Minimize costs.

**Answer:** A. Premium performance with locally-redundant storage (LRS)

**Explanation:** SMB Multichannel is supported on premium file shares.

---

### Question #67
**Question:** Azure Import/Export destination for 5 TB of data. What can you use?

**Answer:** B. Azure File Storage

**Explanation:** Import/Export can import to Azure Blob Storage and Azure Files.

---

### Question #68
**Question:** RBAC role conditions for storage1. Which storage services support conditions?

**Answer:** E. containers and queues only

**Explanation:** Conditions for RBAC assignments are supported for blobs and queues.

---

### Question #69
**Question:** AKS clusters with different network configurations. Statements about deployments.

**Answer:** Based on specific CNI and network configurations.

**Explanation:** AKS network configuration affects pod IP assignment and connectivity.

---

### Question #70
**Question:** Ensure NGINX is available on VMs deployed in scale set. What should you use?

**Answer:** C. a Desired State Configuration (DSC) extension

**Explanation:** DSC extension configures VMs during deployment.

---

### Question #71
**Question:** Storage account creation with settings. Statements about the account.

**Answer:** Based on the specific settings configured.

**Explanation:** Storage account settings determine capabilities, redundancy, and access.

---

### Question #72
**Question:** Use customer-managed key with maximum supported bit length.

**Answer:** RSA key with 4096-bit length.

**Explanation:** RSA 4096 is the maximum supported key size for Azure Storage encryption.

---

## TOPIC 4 - QUESTION SET 4 (COMPUTE)

---

### Question #1
**Question:** Deploy YAML file to AKS. Solution: run az aks.

**Answer:** B. No

**Explanation:** kubectl is used to deploy YAML files, not az aks.

---

### Question #2
**Question:** Deploy YAML file to AKS. Solution: run kubectl client.

**Answer:** A. Yes

**Explanation:** kubectl apply is used to deploy YAML files to AKS.

---

### Question #3
**Question:** Deploy YAML file to AKS. Solution: run azcopy.

**Answer:** B. No

**Explanation:** azcopy is for storage operations, not Kubernetes deployment.

---

### Question #4
**Question:** Create alert when more than two error events logged in System event log within hour. Solution: storage account with SAS.

**Answer:** B. No

**Explanation:** Log Analytics workspace is needed, not storage account.

---

### Question #5
**Question:** Move custom application from VM1 to VNET2. Minimize administrative effort.

**Answer:** Delete VM1, recreate in VNET2 with same disk.

**Explanation:** VMs cannot be moved directly between VNets.

---

### Question #6
**Question:** ARM template referencing administrative password. Prevent plain text password.

**Answer:** A. an Azure Key Vault and an access policy

**Explanation:** Key Vault stores passwords securely. ARM template references the Key Vault.

---

### Question #7
**Question:** App Service plans and web apps. Which plans can be used for WebApp1 and WebApp2?

**Answer:** WebApp1: ASP1, ASP3 (.NET Core on Windows or Linux). WebApp2: ASP1 only (ASP.NET on Windows).

**Explanation:** ASP.NET requires Windows. .NET Core runs on both Windows and Linux.

---

### Question #8
**Question:** Scale set Scale1 with autoscale settings. Number of VMs at 85% CPU for 6 minutes and 25% then 50% CPU.

**Answer:** 6 VMs at 85% (scale out adds 2). 2 VMs at 25% (scale in reduces to minimum 2).

**Explanation:** Autoscale rules determine VM count changes based on CPU thresholds.

---

### Question #9
**Question:** Automate deployment of scale set with web server components installed.

**Answer:** AD. Upload configuration script, Modify extensionProfile section of ARM template.

**Explanation:** Custom Script Extension or DSC extension installs components during deployment.

---

### Question #10
**Question:** Install kubectl client on Windows 10. Which command?

**Answer:** az aks install-cli

**Explanation:** az aks install-cli installs kubectl on the local machine.

---

### Question #11
**Question:** Use Azure Automation State Configuration to manage VM configurations. Three actions in sequence?

**Answer:** 1. Upload configuration, 2. Compile into node configuration, 3. Assign node configuration.

**Explanation:** Azure Automation DSC requires configuration import, compilation, and assignment.

---

### Question #12
**Question:** Deploy VM to West US location using Template1. What should you do?

**Answer:** A. Modify the location in the resources section to westus

**Explanation:** The resources section location overrides variables and parameters.

---

### Question #13
**Question:** Staging slot unavailable for webapp1. What should you do first?

**Answer:** A. From Plan1, scale up the App Service plan

**Explanation:** Staging slots require Standard, Premium, or Isolated tiers.

---

### Question #14
**Question:** App1 always runs on at least eight VMs during planned maintenance.

**Answer:** C. one Availability Set that has 10 update domains and one fault domain

**Explanation:** Update domains distribute VMs across maintenance windows.

---

### Question #15
**Question:** Create alert for error events. Solution: event subscription on VM1.

**Answer:** B. No

**Explanation:** Log Analytics workspace and Microsoft Monitoring Agent are needed.

---

### Question #16
**Question:** Move VM1 to different host during maintenance. Solution: move to different subscription.

**Answer:** B. No

**Explanation:** Redeploy the VM to move to different host.

---

### Question #17
**Question:** Move VM1 to different host during maintenance. Solution: click Redeploy.

**Answer:** A. Yes

**Explanation:** Redeploy moves VM to a new node in Azure infrastructure.

---

### Question #18
**Question:** Move VM1 to different host during maintenance. Solution: Enable Update management.

**Answer:** B. No

**Explanation:** Redeploy is needed to move to different host.

---

### Question #19
**Question:** Add custom domain to webapp1. What should you do first?

**Answer:** A. Create a DNS record

**Explanation:** DNS record (CNAME or A) must be created before adding custom domain.

---

### Question #20
**Question:** Connect VM1 to VNET2. Solution: move VM1 to RG2, add new network interface.

**Answer:** B. No

**Explanation:** VM must be deleted and recreated to change VNet.

---

### Question #21
**Question:** Connect VM1 to VNET2. Solution: delete VM1, recreate with new network interface.

**Answer:** A. Yes

**Explanation:** Deleting and recreating is the correct solution.

---

### Question #22
**Question:** Connect VM1 to VNET2. Solution: turn off VM1, add new network interface.

**Answer:** B. No

**Explanation:** VM must be deleted and recreated to change VNet.

---

### Question #23
**Question:** Quota for vCPUs. Can deploy VM3, VM4, VM5?

**Answer:** Based on quota usage and available vCPUs.

**Explanation:** Quota limits apply to total vCPUs across all VM sizes.

---

### Question #24
**Question:** Availability Set with 2 fault domains and 10 update domains. 14 VMs. Maximum unavailable VMs during maintenance and power failure?

**Answer:** 2 VMs (maintenance - update domains), 7 VMs (power failure - fault domains)

**Explanation:** Update domains = 10, so 14 VMs distributed across 10 domains. Fault domains = 2, so 7 VMs per domain.

---

### Question #25
**Question:** AKS cluster with various IP addresses. Which IP for DNS record?

**Answer:** A. 131.107.2.1

**Explanation:** This is the load balancer frontend IP for external access.

---

### Question #26
**Question:** Deploy 10 web apps. Minimize costs. What to deploy before template?

**Answer:** B. one App Service plan

**Explanation:** Multiple web apps can run in one App Service plan.

---

### Question #27
**Question:** ARM template for container instance. Internet users can connect? IIS failure handling?

**Answer:** Internet users can connect. Container restarts automatically on failure.

**Explanation:** Container instance has public IP. Restart policy handles failures.

---

### Question #28
**Question:** Changes to VM1. Which change causes downtime?

**Answer:** C. Change the size to D8s v3

**Explanation:** VM resize requires VM to be in stopped state.

---

### Question #29
**Question:** Test App1 update before making available to users.

**Answer:** AD. Deploy to webapp1-test, test, then swap slots.

**Explanation:** Deployment slots allow testing before production deployment.

---

### Question #30
**Question:** Record successful and failed connection attempts to VM1.

**Answer:** AEF. Enable Network Watcher, Register Insights provider, Enable NSG flow logs.

**Explanation:** NSG flow logging requires Network Watcher and Insights provider.

---

### Question #31
**Question:** Deploy scale set with five instances as quickly as possible.

**Answer:** D. one virtual machine scale set that is set to ScaleSetVM orchestration mode.

**Explanation:** ScaleSetVM orchestration mode creates and manages instances.

---

### Question #32
**Question:** Web apps with different runtime stacks. Minimum number of App Service plans?

**Answer:** B. 2 (one for Windows apps, one for Linux apps)

**Explanation:** .NET Core and ASP.NET run on Windows. PHP and Ruby run on Linux.

---

### Question #33
**Question:** Budget for RG1 with VM1 (20 euros/day) and VM2 (30 euros/day). Alerts and VM status when budget reached.

**Answer:** VMs continue to run (budget only sends notifications). One email notification (50% threshold reached).

**Explanation:** Budgets don't stop resources. Only 50% threshold is reached within month.

---

### Question #34
**Question:** View date/time resources created in RG1. Solution: Subscriptions blade, Programmatic deployment.

**Answer:** B. No

**Explanation:** Deployments are viewed from RG1 blade, not Subscriptions blade.

---

### Question #35
**Question:** Connect VM1 to VNET2. Solution: create new network interface, add to VM1.

**Answer:** B. No

**Explanation:** VM must be deleted and recreated to change VNet.

---

### Question #36
**Question:** Local Administrator group membership on Computer1 joined by User1.

**Answer:** C. User1 and User2 only

**Explanation:** Device owner (User1) and global administrators (User2) are local admins.

---

### Question #37
**Question:** Move App1 from RG1 to RG3. Can App1 be moved? Can storage account be moved?

**Answer:** No (RG2 has Read Only lock), Yes (App1 can be moved)

**Explanation:** Read-only lock prevents movement. App Service resources can be moved to different region.

---

### Question #38
**Question:** Policy1 appends tag2:value2 to resources. Tags on RG1 and storage1?

**Answer:** RG1: tag1:value1 only. Storage1: tag2:value2 and tag3:value3.

**Explanation:** Tags applied to resource groups aren't inherited by resources.

---

### Question #39
**Question:** Alert rule with action group. Emails and SMS per hour?

**Answer:** 60 emails (one per minute), 12 SMS (rate limited to 1 per 5 minutes).

**Explanation:** Rate limiting applies to SMS (1 per 5 minutes) and email (100 per hour).

---

### Question #40
**Question:** Backup VMs to Vault1. Which VMs can be backed up?

**Answer:** D. VM1, VM3, VMA, and VMC only

**Explanation:** Vault must be in same region as VMs being backed up.

---

### Question #41
**Question:** Configure cluster autoscaler for AKS. Which two tools?

**Answer:** AB. kubectl command and az aks command

**Explanation:** kubectl autoscale configures pod autoscaling. az aks update configures cluster autoscaler.

---

### Question #42
**Question:** Deploy container image App1 to AKS cluster. What should you do first?

**Answer:** C. Run the az acr build command

**Explanation:** Container image must be built and pushed to Container Registry first.

---

### Question #43
**Question:** Configure proximity placement group for VMSS1. Which proximity placement group?

**Answer:** A. Proximity2 only

**Explanation:** Proximity placement group must be in same region as VMSS.

---

### Question #44
**Question:** View date/time resources created in RG1. Solution: Subscriptions blade, Resource providers.

**Answer:** B. No

**Explanation:** Deployments are viewed from RG1 blade, not Subscriptions blade.

---

### Question #45
**Question:** View date/time resources created in RG1. Solution: RG1 blade, Automation script.

**Answer:** B. No

**Explanation:** Automation script shows template, not deployment history. Use Deployments.

---

### Question #46
**Question:** View date/time resources created in RG1. Solution: RG1 blade, Deployments.

**Answer:** A. Yes

**Explanation:** Deployments blade shows deployment history.

---

### Question #47
**Question:** Monitor metrics and logs of Linux VM1. What should you use?

**Answer:** B. Linux Diagnostic Extension (LAD) 3.0

**Explanation:** LAD collects metrics and logs from Linux VMs.

---

### Question #48
**Question:** Effective network security rules for VM1. Internet users can reach web server? DNS server?

**Answer:** Yes to web server (port 80 allowed). No to DNS server (port 53 blocked by Rule2).

**Explanation:** Rules are processed in priority order. Rule2 blocks ports 50-60.

---

### Question #49
**Question:** At least two VMs available if single Azure datacenter becomes unavailable.

**Answer:** C. each virtual machine in a separate Availability Zone

**Explanation:** Availability zones protect against datacenter failures.

---

### Question #50
**Question:** Deploy VM2 from Template1. What can you configure during deployment?

**Answer:** B. administrator username

**Explanation:** Administrator credentials can be specified during deployment.

---

### Question #51
**Question:** Scheduled runbook to increase processor performance at month end.

**Answer:** B. Modify the VM size property of VM1

**Explanation:** Changing VM size increases processor performance.

---

### Question #52
**Question:** Ensure NGINX available on VMs in scale set deployed from ARM template.

**Answer:** B. A Desired State Configuration (DSC) extension

**Explanation:** DSC extension configures VMs during deployment.

---

### Question #53
**Question:** AKS network profile. Pod CIDR and Service CIDR?

**Answer:** Pod CIDR: 10.244.0.0/16, Service CIDR: 10.0.0.0/16

**Explanation:** These are the default ranges for AKS networking.

---

### Question #54
**Question:** App Service plan autoscale. Number of instances with CPU >= 30% for 45 minutes, then < 30% for 60 minutes?

**Answer:** 5 instances (scale out to max), then 3 instances (scale in after cooldown)

**Explanation:** Scale out occurs at >= 30% CPU. Scale in occurs at < 30% CPU.

---

### Question #55
**Question:** VM1 redeploy. Which changes will be lost?

**Answer:** C. the new files on drive D

**Explanation:** Redeploy preserves OS disk (C:) but data disks (D:) are lost.

---

### Question #56
**Question:** Use disks attached to VM1 as template for Azure VMs. What should you modify?

**Answer:** C. the hard drive

**Explanation:** VHDX must be converted to VHD format for Azure.

---

### Question #57
**Question:** Scale set with 4 instances. Get-AzVmss cmdlet. Automatic updates and upgrade settings.

**Answer:** 0 (automatic updates disabled), 4 (manual upgrade required for all instances)

**Explanation:** enableAutomaticUpdates is false. Manual upgrade needed.

---

### Question #58
**Question:** View ARM template used for VM and storage account deployment. From which blade?

**Answer:** B. RG1

**Explanation:** Resource Group blade shows deployment history with templates.

---

### Question #59
**Question:** Revert to previous version of App1 after swap caused performance issues.

**Answer:** B. Swap the slots

**Explanation:** Swapping back reverts to the previous version.

---

### Question #60
**Question:** Restore latest backup of VM1. Where can you restore?

**Answer:** New VM in same region.

**Explanation:** Azure Backup can restore to new VM in same region.

---

### Question #61
**Question:** Backup Pre-Check Warning status. What is possible cause?

**Answer:** B. VM1 does not have the latest version of the Azure VM Agent installed.

**Explanation:** Outdated VM Agent can cause backup warnings.

---

### Question #62
**Question:** Move VM1 to different host during maintenance. Solution: move to different resource group.

**Answer:** B. No

**Explanation:** Redeploy is needed to move to different host.

---

### Question #63
**Question:** ARM template for 50 VMs in availability set. Fault domains and update domains.

**Answer:** 2 fault domains, 20 update domains.

**Explanation:** 2-3 fault domains per region. 20 is max update domains.

---

### Question #64
**Question:** Create alert for error events. Solution: Log Analytics workspace with agent.

**Answer:** A. Yes

**Explanation:** Log Analytics workspace with Microsoft Monitoring Agent collects events for alerts.

---

### Question #65
**Question:** Scale set autoscale settings. Number of VMs at specific times.

**Answer:** Based on autoscale rules and thresholds.

**Explanation:** Autoscale rules determine VM count based on metrics.

---

### Question #66
**Question:** Additional App Service plan ASP5 with Linux OS. Which locations can deploy?

**Answer:** A. West US, Central US, or East US

**Explanation:** Linux App Service plans are available in all locations.

---

### Question #67
**Question:** Ensure NGINX available on VMs in scale set deployed from ARM template.

**Answer:** B. a Desired State Configuration (DSC) extension

**Explanation:** DSC extension configures VMs during deployment.

---

### Question #68
**Question:** Create VM using ARM template from Cloud Shell. Complete the command.

**Answer:** New-AzResourceGroupDeployment

**Explanation:** This cmdlet deploys ARM templates to resource groups.

---

### Question #69
**Question:** Deploy YAML file to AKS. Solution: az aks from Cloud Shell.

**Answer:** B. No

**Explanation:** kubectl is used to deploy YAML files.

---

### Question #70
**Question:** Create alert for error events. Solution: Log Analytics workspace with Microsoft Monitoring Agent VM extension.

**Answer:** B. No

**Explanation:** Microsoft Monitoring Agent must be installed, not the VM extension.

---

### Question #71
**Question:** Create alert for error events. Solution: Log Analytics workspace with Microsoft Monitoring Agent.

**Answer:** A. Yes

**Explanation:** Log Analytics workspace with agent collects events for alerts.

---

### Question #72
**Question:** Restore backup to VM2. What should you do first?

**Answer:** B. From VM2, install the Microsoft Azure Recovery Services Agent.

**Explanation:** Recovery Services Agent is needed to restore backup to a different VM.

---

### Question #73
**Question:** ARM template for VM with multiple data disks. Complete the template.

**Answer:** dataDisks array in storageProfile.

**Explanation:** Multiple data disks are defined in the dataDisks section.

---

### Question #74
**Question:** Create NIC2 for VM1. Solution: create in RG1 and West US.

**Answer:** A. Yes

**Explanation:** NIC must be in same region as VM (West US).

---

### Question #75
**Question:** Create NIC2 for VM1. Solution: create in RG2 and Central US.

**Answer:** B. No

**Explanation:** NIC must be in same region as VM (West US).

---

### Question #76
**Question:** Create NIC2 for VM1. Solution: create in RG2 and West US.

**Answer:** A. Yes

**Explanation:** NIC must be in same region as VM (West US).

---

### Question #77
**Question:** Deploy ARM template to create resource group and storage account. Which cmdlet?

**Answer:** B. New-AzResourceGroupDeployment

**Explanation:** This cmdlet deploys to a resource group.

---

### Question #78
**Question:** Daily backup of WebApp1 excluding Folder2. What to create first and what to use for exclusion?

**Answer:** Azure Storage account, _backup.filter file.

**Explanation:** Backups require storage account. _backup.filter excludes files/folders.

---

### Question #79
**Question:** Ensure NGINX available on VMs in scale set deployed from ARM template.

**Answer:** C. Azure Custom Script Extension

**Explanation:** Custom Script Extension installs software during deployment.

---

### Question #80
**Question:** Join VM to Active Directory domain using ARM template. Complete the template.

**Answer:** Microsoft.Compute/VirtualMachines/extensions with protectedSettings for password.

**Explanation:** Domain join extension configures AD join during deployment.

---

### Question #82
**Question:** AKS cluster creation settings. Statements about the cluster.

**Answer:** Based on specific AKS configuration.

**Explanation:** AKS settings determine node size, node count, and networking.

---

### Question #83
**Question:** Coordinated upgrade of AKS cluster with two new nodes. Minimize costs.

**Answer:** Use az aks upgrade with max surge parameter.

**Explanation:** max surge controls how many nodes are added during upgrade.

---

### Question #84
**Question:** Deploy.json file and Azure CLI commands. Statements about the deployment.

**Answer:** Based on the specific template and command parameters.

**Explanation:** Template deployment behavior depends on parameters and mode.

---

### Question #85
**Question:** Ensure NGINX available on VMs in scale set deployed from ARM template.

**Answer:** A. Azure Custom Script Extension

**Explanation:** Custom Script Extension installs software during deployment.

---

### Question #86
**Question:** ARM template deployment to RG1 removing existing resources. Complete the command.

**Answer:** New-AzResourceGroupDeployment -Mode Complete

**Explanation:** Complete mode deletes resources not in the template.

---

### Question #87
**Question:** App Service autoscale rules. CPU usage and instance count.

**Answer:** Based on specific autoscale rule settings.

**Explanation:** Autoscale rules determine when to scale out or in.

---

### Question #88
**Question:** Deploy container instances to container group. Which instances?

**Answer:** C. Instance1 and Instance2 only

**Explanation:** Container groups require instances to share lifecycle.

---

### Question #89
**Question:** Ensure NGINX available on VMs in scale set deployed from ARM template.

**Answer:** A. Azure Custom Script Extension

**Explanation:** Custom Script Extension installs software during deployment.

---

### Question #90
**Question:** Azure Firewall Premium FW1. Which IP addresses can you use?

**Answer:** D. IP1, IP2, IP4, and IP5 only

**Explanation:** Firewall requires specific SKU and region compatible IPs.

---

### Question #91
**Question:** Deploy VM using ARM template. Complete the template.

**Answer:** The template requires VM size, image, and network configuration.

**Explanation:** VM deployment template must specify these properties.

---

## TOPIC 5 - QUESTION SET 5 (NETWORKING)

---

### Question #1
**Question:** Multi-tiered application with web, business logic, and data tiers. Load balance web to business logic, protect from SQL injection.

**Answer:** Internal load balancer, Application Gateway with WAF tier.

**Explanation:** Internal load balancer distributes traffic. WAF protects from SQL injection.

---

### Question #2
**Question:** Connect three datacenters to Azure subscription, minimize latency.

**Answer:** C. three virtual WANs and one virtual hub

**Explanation:** Virtual WAN provides hub-spoke connectivity for multiple locations.

---

### Question #3
**Question:** Five VMs with public and private IPs. Same security rules. Minimum interfaces and NSGs?

**Answer:** 5 network interfaces, 1 network security group.

**Explanation:** Each VM needs one NIC. One NSG applies to all.

---

### Question #4
**Question:** Create inbound NAT rules for RDP to VM1 and VM2 on port 3389.

**Answer:** A. a frontend IP address

**Explanation:** Frontend IP is needed before creating NAT rules.

---

### Question #5
**Question:** Private DNS zone adatum.com with auto registration from VNET1. Which A records added?

**Answer:** A records for VMs in VNET1 only.

**Explanation:** Auto registration creates A records for VMs in the linked VNet.

---

### Question #6
**Question:** Collect data about IP addresses connecting to ILB1. Run interactive queries.

**Answer:** Log Analytics workspace, ILB1.

**Explanation:** Log Analytics collects and queries load balancer logs.

---

### Question #7
**Question:** Peer VNet1 with other VNets. Which VNets can be peered?

**Answer:** C. VNet3 and VNet4 only

**Explanation:** Address spaces must not overlap. VNet2 overlaps with VNet1.

---

### Question #8
**Question:** Load balancer for NVAs in active-active configuration with automatic failover.

**Answer:** BCF. Standard load balancer, two backend pools, frontend IP, backend pool, health probe.

**Explanation:** Standard LB supports HA ports. Two backend pools for different services.

---

### Question #9
**Question:** Connect Client1 to VNet2. What should you do?

**Answer:** A. Download and re-install VPN client configuration package.

**Explanation:** VPN client package must be updated with new routes.

---

### Question #10
**Question:** Public and private DNS zones. Statements about name resolution.

**Answer:** Based on specific DNS configuration.

**Explanation:** DNS resolution depends on zone type and virtual network links.

---

### Question #11
**Question:** Apply NSG1 to subnets. Which subnets?

**Answer:** D. the subnets on VNet3 only

**Explanation:** NSG must be in same region as VNet.

---

### Question #12
**Question:** Add address space to VNet1 while maintaining communication with VNet2.

**Answer:** 1. Remove peering, 2. Add address space, 3. Recreate peering.

**Explanation:** Peering must be removed before adding address ranges.

---

### Question #13
**Question:** Move resources between resource groups. Can Disk1, NIC1, IP2 be moved?

**Answer:** Yes for Disk1, No for NIC1 (attached to VM), No for IP2 (different region).

**Explanation:** Attached resources can't be moved. Resources are region-specific.

---

### Question #14
**Question:** webapp1 access MySQL database on VM1 in VNET1.

**Answer:** D. Deploy an Azure Application Gateway

**Explanation:** Application Gateway provides access to VM1 from webapp1.

---

### Question #15
**Question:** Enable Desired State Configuration for VM1. What should you do first?

**Answer:** B. Start VM1

**Explanation:** VM must be running to install DSC extension.

---

### Question #16
**Question:** Visitors serviced by same web server for each request. What to configure?

**Answer:** D. Session persistence to Client IP

**Explanation:** Session persistence ensures requests go to same server.

---

### Question #17
**Question:** Remote Desktop connections to VM1. Solution: Add rule to NSG-Subnet1, remove NSG-VM1.

**Answer:** B. No

**Explanation:** RDP uses TCP port 3389, not UDP. NSG on subnet alone not sufficient.

---

### Question #18
**Question:** Remote Desktop connections to VM1. Solution: Add rule to NSG-Subnet1 with UDP.

**Answer:** B. No

**Explanation:** RDP uses TCP port 3389, not UDP.

---

### Question #19
**Question:** Remote Desktop connections to VM1. Solution: Add TCP rule to NSG-Subnet1 and NSG-VM1.

**Answer:** A. Yes

**Explanation:** TCP port 3389 rules on both NSGs allow RDP connections.

---

### Question #20
**Question:** VNet1 configuration. Need to add IP addresses. What to do?

**Answer:** Add address space, add network interface.

**Explanation:** Address space must include required ranges.

---

### Question #21
**Question:** NSGs to meet requirements for VM1-VM6. Minimum NSGs?

**Answer:** C. 4

**Explanation:** Different subnets require different rules.

---

### Question #22
**Question:** Create VM2 and connect to VNET1. Policy blocks VMs and VNets.

**Answer:** A. Remove Microsoft.Compute/virtualMachines from the policy.

**Explanation:** Policy blocks VM creation. Must remove the restriction.

---

### Question #23
**Question:** Move adatum.com zone to Azure DNS. Minimize administrative effort.

**Answer:** B. Azure PowerShell

**Explanation:** PowerShell script automates DNS zone migration.

---

### Question #24
**Question:** Direct RDP connections to VM3 only. What to configure?

**Answer:** A. an inbound NAT rule

**Explanation:** NAT rule directs traffic to specific VM.

---

### Question #25
**Question:** Basic internal load balancer LB1. Statements about backend VM connectivity.

**Answer:** Based on LB configuration and VM connectivity.

**Explanation:** Basic internal LB has specific connectivity requirements.

---

### Question #26
**Question:** Link DNS zones to VNET1 and auto registration.

**Answer:** Private DNS zone contoso.com can be linked.

**Explanation:** Private DNS zones can be linked to VNets for resolution and registration.

---

### Question #27
**Question:** Create site-to-site VPN to Azure. Four actions in sequence.

**Answer:** 1. Create gateway subnet, 2. Create virtual network gateway, 3. Create local network gateway, 4. Create connection.

**Explanation:** VPN setup requires gateway subnet, virtual gateway, local gateway, and connection.

---

### Question #28
**Question:** Prevent users of VM1 and VM2 from accessing websites on TCP port 80.

**Answer:** C. Associate the NSG to Subnet1.

**Explanation:** NSG with deny rule must be associated to the subnet.

---

### Question #29
**Question:** Connect VNet1 to VNet2 in different subscriptions. What should you do first?

**Answer:** D. Provision virtual network gateways.

**Explanation:** VPN gateways are needed for VNet-to-VNet connections.

---

### Question #30
**Question:** Ensure VM1 can be created in Availability Zone. Which settings to modify?

**Answer:** AC. Use managed disks, Availability options.

**Explanation:** Managed disks and availability zone selection are required.

---

### Question #31
**Question:** Add VM1 to VMSS1 (VM orchestration mode). Which resource group and location?

**Answer:** RG1, RG2, or RG3 for resource group. West US only for location.

**Explanation:** Resource group can be any. Location must match VMSS.

---

### Question #32
**Question:** VNet peering configurations. How can packets be routed?

**Answer:** Based on gateway transit and peering settings.

**Explanation:** Peering settings determine routing between VNets.

---

### Question #33
**Question:** Point-to-site VPN from Computer2. Solution: modify Azure AD authentication policies.

**Answer:** B. No

**Explanation:** Client certificate must be installed on Computer2.

---

### Question #34
**Question:** Point-to-site VPN from Computer2. Solution: join Computer2 to Azure AD.

**Answer:** B. No

**Explanation:** Client certificate is required, not Azure AD join.

---

### Question #35
**Question:** NSGs automatically block TCP port 8080. Solution: create resource lock.

**Answer:** B. No

**Explanation:** Azure Policy should be used, not resource lock.

---

### Question #36
**Question:** Remote Desktop connection to VM1 fails. What should you do first?

**Answer:** D. Start VM1

**Explanation:** VM must be running for RDP connection.

---

### Question #37
**Question:** Ensure VMs can resolve DNS names using DNS service on VM1.

**Answer:** D. Configure peering between VNET1, VNET2, and VNET3.

**Explanation:** Peering allows VMs to access DNS service across VNets.

---

### Question #38
**Question:** Network Watcher with NSG rules. Statements about VM traffic.

**Answer:** Based on specific NSG rules and Network Watcher results.

**Explanation:** NSG rules determine allowed/denied traffic.

---

### Question #39
**Question:** Prevent RDP access from internet. Allow from on-premises network.

**Answer:** B. Create a deny rule in NSG linked to Subnet1.

**Explanation:** NSG deny rule blocks RDP from internet.

---

### Question #40
**Question:** Apply ASG1 to VM1. What should you do?

**Answer:** A. Associate NIC1 to ASG1

**Explanation:** Application Security Groups are associated with NICs.

---

### Question #41
**Question:** Connect VNet1 to on-premises using site-to-site VPN. Minimize cost.

**Answer:** ADE. Create connection, Create gateway subnet, Create VPN gateway with Basic SKU.

**Explanation:** Basic SKU is lowest cost for VPN gateway.

---

### Question #42
**Question:** Peering configurations. Packets can reach which VNets?

**Answer:** Based on peering status and gateway transit settings.

**Explanation:** Peering status determines connectivity.

---

### Question #43
**Question:** Basic Load Balancer LB1 with VM1 and VM2. Statements about load balancing.

**Answer:** Based on LB configuration and health probe.

**Explanation:** Health probes determine backend availability.

---

### Question #44
**Question:** Configure slb1 to allow connectivity to VM1. Which changes to VM1?

**Answer:** Remove public IP, Create and configure NSG.

**Explanation:** Public load balancer manages internet traffic. NSG allows traffic.

---

### Question #45
**Question:** Create network interface NIC1. Which location can you create it?

**Answer:** B. East US only

**Explanation:** NIC must be in same region as VNet (East US).

---

### Question #46
**Question:** Ensure VM1 resolves host names in adatum.com.

**Answer:** A. Update the DNS suffix on VM1 to be adatum.com

**Explanation:** DNS suffix must match the zone for resolution.

---

### Question #47
**Question:** Network Watcher features for identifying security rules and validating outbound connectivity.

**Answer:** IP flow verify, Connection troubleshoot.

**Explanation:** IP flow verify tests security rules. Connection troubleshoot tests connectivity.

---

### Question #48
**Question:** DNS settings for VNET1 and VM network interfaces. Which DNS servers used?

**Answer:** Based on VNet DNS settings and per-VM overrides.

**Explanation:** VNet DNS settings apply by default. VM settings can override.

---

### Question #49
**Question:** Move resources from RG1 to RG2. Which resources can be moved?

**Answer:** IP1, Storage1 can be moved. No resources from RG2 (delete lock).

**Explanation:** IP addresses and storage accounts can be moved. Locks prevent movement.

---

### Question #50
**Question:** Add VM1 and VM2 to LB1 backend pool. Solution: create Basic SKU public IP.

**Answer:** B. No

**Explanation:** Standard load balancer requires Standard SKU resources.

---

### Question #51
**Question:** Add VM1 and VM2 to LB1 backend pool. Solution: create Standard SKU public IP, stop VM2.

**Answer:** B. No

**Explanation:** Both VMs need Standard SKU resources.

---

### Question #52
**Question:** Add VM1 and VM2 to LB1 backend pool. Solution: create Standard SKU public IPs.

**Answer:** A. Yes

**Explanation:** Standard SKU IPs are required for Standard load balancer.

---

### Question #53
**Question:** Point-to-site VPN from Computer2. Solution: export client certificate from Computer1.

**Answer:** A. Yes

**Explanation:** Client certificate must be installed on each client.

---

### Question #54
**Question:** Allow HTTPS connections to website on VM1. What should you do?

**Answer:** C. For Rule5, change Action to Allow and priority to 401.

**Explanation:** HTTPS uses port 443. Rule must allow traffic with appropriate priority.

---

### Question #55
**Question:** NSGs automatically block TCP port 8080. Solution: unregister Microsoft.ClassicNetwork provider.

**Answer:** B. No

**Explanation:** Azure Policy should be used, not resource provider changes.

---

### Question #56
**Question:** VNet peering statements. Can connect VNets across regions? Can peer overlapping address spaces?

**Answer:** Yes (global peering), No (cannot overlap).

**Explanation:** Global peering connects different regions. Address spaces must not overlap.

---

### Question #57
**Question:** Connections to App1 from 131.107.100.50 over TCP port 443 fail. Solution: create deny rule.

**Answer:** B. No

**Explanation:** Denying traffic would make it worse. Allow rule is needed.

---

### Question #58
**Question:** Same scenario. Solution: delete BlockAllOther443 rule.

**Answer:** B. No

**Explanation:** BlockAllOther443 has lower priority. The specific allow rule has higher priority.

---

### Question #59
**Question:** Same scenario. Solution: modify priority of allow rule.

**Answer:** B. No

**Explanation:** The allow rule already has highest priority (100).

---

### Question #60
**Question:** NSGs automatically block TCP port 8080. Solution: assign built-in policy.

**Answer:** B. No

**Explanation:** Built-in policy doesn't exist for this. Custom policy needed.

---

### Question #61
**Question:** AKS network type for App1 where on-premises clients connect by pod IP.

**Answer:** B. Azure Container Networking Interface (CNI)

**Explanation:** CNI gives pods direct IP addresses from VNet.

---

### Question #62
**Question:** Add VM1 and VM2 to LB1 backend pool. Solution: disassociate public IP from VM2.

**Answer:** B. No

**Explanation:** Public IP association doesn't affect load balancer backend.

---

### Question #63
**Question:** NSGs automatically block TCP port 8080. Solution: configure custom policy.

**Answer:** A. Yes

**Explanation:** Custom Azure Policy can enforce NSG rules.

---

### Question #64
**Question:** View average round-trip time from VM1 to VM2.

**Answer:** C. Connection monitor

**Explanation:** Connection monitor measures latency and reachability over time.

---

### Question #65
**Question:** Basic and Standard load balancers with VMs. How should VMs be created?

**Answer:** Basic LB VMs: same availability set or scale set. Standard LB VMs: same VNet.

**Explanation:** Basic LB is restricted to availability set/scale set. Standard LB can span any VMs in VNet.

---

### Question #66
**Question:** Site-to-site VPN with failover. Minimum public IPs, virtual network gateways, local network gateways?

**Answer:** 4 public IPs, 2 virtual network gateways, 2 local network gateways.

**Explanation:** Active-active configuration requires redundant resources.

---

### Question #67
**Question:** Reverse DNS lookup for 10.0.0.4 from VM2. Which FQDN returned?

**Answer:** D. vm1.internal.cloudapp.net

**Explanation:** Azure internal DNS returns internal.cloudapp.net.

---

### Question #68
**Question:** App1 connections fail. Solution: create inbound rule allowing AzureLoadBalancer source.

**Answer:** A. Yes

**Explanation:** AzureLoadBalancer source allows traffic from load balancer.

---

### Question #69
**Question:** Configure point-to-site connection from policy-based gateway.

**Answer:** CE. Delete GW1, Create route-based virtual network gateway.

**Explanation:** Point-to-site requires route-based VPN gateway.

---

### Question #70
**Question:** Private DNS zone with registration virtual network. Statements about records.

**Answer:** Based on registration and resolution VNet links.

**Explanation:** Auto-registration occurs only in registration VNet.

---

### Question #71
**Question:** Private DNS zones and VNet links. Statements about DNS resolution.

**Answer:** Based on VNet links and auto-registration settings.

**Explanation:** Resolution depends on linked VNets. Registration creates records.

---

### Question #72
**Question:** ARM template for VNET1 with Azure Bastion. Complete the template.

**Answer:** Bastion requires AzureBastionSubnet and Bastion host resource.

**Explanation:** Bastion deployment requires specific subnet and host configuration.

---

### Question #73
**Question:** Inspect network traffic from VM1 to VM2 for 3 hours. Solution: create packet capture.

**Answer:** A. Yes

**Explanation:** Packet capture collects network traffic for analysis.

---

### Question #74
**Question:** Same scenario. Solution: create connection monitor.

**Answer:** A. Yes

**Explanation:** Connection monitor inspects network traffic.

---

### Question #75
**Question:** Same scenario. Solution: create Data Collector Set.

**Answer:** B. No

**Explanation:** Connection Monitor is Azure Network Watcher feature.

---

### Question #76
**Question:** Load balance HTTPS connections to vm1 and vm2 using lb1. Three actions.

**Answer:** 1. Create backend pool, 2. Create health probe, 3. Create load balancing rule.

**Explanation:** Load balancer requires backend pool, health probe, and rule.

---

### Question #77
**Question:** Inspect network traffic. Solution: create metric on Network In/Out.

**Answer:** B. No

**Explanation:** Connection Monitor or packet capture is needed.

---

### Question #78
**Question:** App1 connections fail. Solution: create deny rule for 131.107.100.50.

**Answer:** B. No

**Explanation:** Deny rule would block the traffic.

---

### Question #79
**Question:** Connect site1 and site2 using Azure Virtual WAN. Four actions.

**Answer:** 1. Create virtual WAN, 2. Create virtual hub, 3. Create VPN site, 4. Connect site to hub.

**Explanation:** Virtual WAN requires hub and site connections.

---

### Question #80
**Question:** Private DNS zone contoso.com. Statements about name resolution.

**Answer:** Based on DNS records and VNet links.

**Explanation:** DNS resolution depends on zones and linked VNets.

---

### Question #81
**Question:** Peer VNet1 to VNet2. What should you do first?

**Answer:** A. Modify the address space of VNet1.

**Explanation:** Address spaces must not overlap for peering.

---

### Question #82
**Question:** Ping VM2 from VM1. Which DNS names can you use?

**Answer:** B. comp1.contoso.com, comp2.contoso.com, comp3.contoso.com, comp4.contoso.com

**Explanation:** All records in the private DNS zone are resolvable.

---

### Question #83
**Question:** Add rule to NSG1 to allow VM1 to ping VM2. Least privilege.

**Answer:** Source: VM1 IP, Destination: VM2 IP, Protocol: ICMP, Action: Allow.

**Explanation:** ICMP is used for ping. Specific IPs limit scope.

---

### Question #84
**Question:** Point-to-site VPN from Computer2. Solution: set IPSec Policy Agent to Automatic.

**Answer:** B. No

**Explanation:** Client certificate must be installed on Computer2.

---

### Question #85
**Question:** Visitors serviced by same web server for each request.

**Answer:** A. Session persistence to Client IP and protocol

**Explanation:** Session persistence ensures consistent server assignment.

---

### Question #86
**Question:** Public Azure Standard Load Balancer. Which public IP addresses can you use?

**Answer:** C. IP3 only

**Explanation:** Standard LB requires Standard SKU public IP.

---

### Question #87
**Question:** Restrict network traffic between pods in AKS with kubenet networking.

**Answer:** B. the Calico network policy

**Explanation:** Calico provides network policy for AKS.

---

### Question #88
**Question:** Route inbound traffic from VPN gateway through VM1.

**Answer:** Configure route table with next hop as VM1 IP.

**Explanation:** User-defined routes can force traffic through NVA.

---

### Question #89
**Question:** Visitors serviced by same web server for each request.

**Answer:** D. Session persistence to Client IP and Protocol

**Explanation:** Session persistence ensures consistent server assignment.

---

### Question #90
**Question:** NSG1 and NSG2 configurations. Can VM1 and VM2 be accessed?

**Answer:** Based on specific NSG rules and associations.

**Explanation:** NSG rules determine VM accessibility.

---

### Question #91
**Question:** Load balancing HTTPS traffic between VM1 and VM2. Additional resources needed?

**Answer:** DE. a backend pool and a health probe

**Explanation:** Load balancing rule requires backend pool and health probe.

---

### Question #92
**Question:** VPN gateway for site-to-site VPN. IP address SKU and assignment?

**Answer:** C. a basic SKU and a dynamic IP address assignment

**Explanation:** VPN gateway uses Basic SKU with dynamic IP.

---

### Question #93
**Question:** Private DNS zone contoso.com. Statements about resolution.

**Answer:** Based on DNS server configuration and VNet links.

**Explanation:** DNS resolution depends on configured DNS servers.

---

### Question #94
**Question:** DNS zones with VNet link and auto-registration. Statements about records.

**Answer:** Based on zone configuration and RBAC assignments.

**Explanation:** Auto-registration creates A records. Owner role allows access.

---

### Question #95
**Question:** ExpressRoute gateway supporting 10 Gbps, availability zones, FastPath.

**Answer:** D. ErGw3AZ

**Explanation:** ErGw3AZ supports FastPath and availability zones.

---

### Question #96
**Question:** NSG1 and NSG2 inbound rules. Statements about VM communication.

**Answer:** Based on specific rules and priorities.

**Explanation:** NSG rules determine allowed/denied traffic between VMs.

---

### Question #97
**Question:** Route table with IP forwarding. Statements about VM connectivity.

**Answer:** Based on route table and IP forwarding configuration.

**Explanation:** User-defined routes and IP forwarding control traffic flow.

---

### Question #98
**Question:** webapp1 connect to on-premises SMB share Share1.

**Answer:** C. an Azure Virtual Network Gateway

**Explanation:** VPN gateway connects Azure to on-premises network.

---

### Question #99
**Question:** Ensure NGINX available on VMs in scale set.

**Answer:** C. Azure Custom Script Extension

**Explanation:** Custom Script Extension installs software during deployment.

---

### Question #100
**Question:** Ensure traffic from VM1 to storage1 travels across Microsoft backbone.

**Answer:** B. service endpoints

**Explanation:** Service endpoints secure traffic to storage over Microsoft backbone.

---

### Question #101
**Question:** Route-based Site-to-Site VPN. Which tunneling protocol?

**Answer:** C. IKEv2

**Explanation:** IKEv2 supports multiple S2S connections.

---

### Question #102
**Question:** Test failover of VM1 to VNET2. Which subnet will VM connect to?

**Answer:** A. TestSubnet1

**Explanation:** The test failover uses the specified subnet in the target VNet.

---

### Question #103
**Question:** Visitors serviced by same web server for each request.

**Answer:** D. Session persistence to Client IP

**Explanation:** Session persistence ensures consistent server assignment.

---

### Question #104
**Question:** Ensure NGINX available on VMs in scale set.

**Answer:** D. a Desired State Configuration (DSC) extension

**Explanation:** DSC extension configures VMs during deployment.

---

### Question #105
**Question:** Visitors serviced by same web server for each request.

**Answer:** B. Session persistence to Client IP

**Explanation:** Session persistence ensures consistent server assignment.

---

### Question #106
**Question:** Azure Bastion Basic SKU inbound access. Which port?

**Answer:** B. 443

**Explanation:** Azure Bastion uses port 443 for HTTPS access.

---

### Question #107
**Question:** Move DC1 to VNET1. How to configure DC1?

**Answer:** Configure DC1 as DNS server, set VNET1 DNS to DC1 IP.

**Explanation:** Domain controller must provide DNS resolution.

---

### Question #108
**Question:** Visitors serviced by same web server for each request.

**Answer:** C. Session persistence to Client IP

**Explanation:** Session persistence ensures consistent server assignment.

---

### Question #109
**Question:** Deploy Azure Firewall AF1 to RG1 in West US. Which VNets?

**Answer:** C. VNET1 only

**Explanation:** Firewall must be in same region (West US) as RG1.

---

### Question #110
**Question:** Monitor connectivity between VMs and on-premises network. Minimum connection monitors?

**Answer:** B. 2

**Explanation:** One connection monitor for each endpoint pair.

---

### Question #111
**Question:** ARM template for network resources. Statements about deployment.

**Answer:** Based on specific template configuration.

**Explanation:** Template deployment creates specified resources.

---

### Question #112
**Question:** Inbound traffic uses Microsoft POP closest to user's location.

**Answer:** C. Routing preference

**Explanation:** Routing preference controls how traffic is routed to Azure.

---

### Question #113
**Question:** Prevent VM1 from accessing VM2 on port 3389.

**Answer:** A. Create NSG with outbound deny rule for destination port 3389, apply to VM1 NIC.

**Explanation:** Outbound rule on VM1 blocks traffic to port 3389.

---

### Question #114
**Question:** Manage outbound traffic from VNET1 using Firewall1. What should you do first?

**Answer:** C. Create a route table

**Explanation:** Route table directs traffic to the firewall.

---

### Question #115
**Question:** Azure Bastion protects which resources?

**Answer:** A. VM1 only

**Explanation:** Azure Bastion provides RDP/SSH access to VMs in the same VNet.

---

### Question #116
**Question:** Visitors serviced by same web server for each request.

**Answer:** C. Session persistence to Client IP and protocol

**Explanation:** Session persistence ensures consistent server assignment.

---

### Question #117
**Question:** Visitors serviced by same web server for each request.

**Answer:** C. Session persistence to Client IP and protocol

**Explanation:** Session persistence ensures consistent server assignment.

---

### Question #118
**Question:** Bastion1 support 100 concurrent SSH users. Minimize administrative effort.

**Answer:** D. Upgrade Bastion1 to the Standard SKU

**Explanation:** Standard SKU supports higher concurrent connections.

---

### Question #119
**Question:** Visitors serviced by same web server for each request.

**Answer:** A. Session persistence to Client IP and protocol

**Explanation:** Session persistence ensures consistent server assignment.

---

### Question #120
**Question:** Remote Desktop connection to VM1 from Device1. Three actions.

**Answer:** 1. Get public IP of VM1, 2. Configure NSG to allow RDP, 3. Connect using RDP.

**Explanation:** RDP requires public IP, NSG rule, and client connection.

---

### Question #121
**Question:** Visitors serviced by same web server for each request.

**Answer:** B. Session persistence to Client IP

**Explanation:** Session persistence ensures consistent server assignment.

---

### Question #122
**Question:** Azure Bastion Basic SKU. Which IP addresses can you use?

**Answer:** B. IP1 and IP2 only

**Explanation:** Bastion Basic SKU supports Basic and Standard public IPs.

---

### Question #123
**Question:** Visitors serviced by same web server for each request.

**Answer:** D. Session persistence to Client IP

**Explanation:** Session persistence ensures consistent server assignment.

---

### Question #124
**Question:** Visitors serviced by same web server for each request.

**Answer:** D. Session persistence to Client IP

**Explanation:** Session persistence ensures consistent server assignment.

---

### Question #125
**Question:** Move VM1 to Sub2. Which resources should you move?

**Answer:** D. VM1, Disk1, NetInt1, and VNet1

**Explanation:** All associated resources must be moved together.

---

## TOPIC 6 - QUESTION SET 6 (MONITORING & BACKUP)

---

### Question #1
**Question:** Schedule nightly backups for VMs. Which VMs can be backed up?

**Answer:** B. VM1, VM2, VM3 and VM4

**Explanation:** Azure Backup supports Windows Server, Windows 10, and Ubuntu Server.

---

### Question #2
**Question:** Backup policy Policy1 with retention settings. Retention periods?

**Answer:** 10 years for yearly backup, 36 months for monthly backup.

**Explanation:** Policy settings determine retention periods.

---

### Question #3
**Question:** Protect VM3 and VM4 with Recovery Services. What should you do first?

**Answer:** A. Create a new Recovery Services vault

**Explanation:** Vaults must be in same region as protected resources.

---

### Question #4
**Question:** Monitor storage1 with email notifications. Minimum alert rules and action groups?

**Answer:** Based on number of signals and notification requirements.

**Explanation:** Each signal may require separate alert rule.

---

### Question #5
**Question:** Alert rule AG1 with Email Azure Resource Manager Role notification. Who receives email?

**Answer:** C. User1 only

**Explanation:** Email only sent to Azure AD user members, not groups or service principals.

---

### Question #6
**Question:** Backup policy Policy1 for VM1 starting Jan 1. Recovery points on Jan 8 and Jan 15?

**Answer:** 6 on Jan 8, 8 on Jan 15.

**Explanation:** Daily, weekly, and monthly recovery points accumulate.

---

### Question #7
**Question:** Monitor web apps with Application Insights. Minimize code modifications.

**Answer:** Enable Application Insights from the Azure portal.

**Explanation:** Azure portal configuration requires minimal code changes.

---

### Question #8
**Question:** Changes made after Backup1. Which change must be performed again after restore?

**Answer:** D. Copy Budget.xls to Data

**Explanation:** Files added after backup are not restored.

---

### Question #9
**Question:** Self-service password reset settings. Statements about users and permissions.

**Answer:** Based on SSPR configuration and user roles.

**Explanation:** SSPR settings determine who can reset passwords.

---

### Question #10
**Question:** User1 unable to join personal device to Azure AD. What should you do?

**Answer:** B. From the Device settings blade, modify the Maximum number of devices per user setting.

**Explanation:** User may have reached device limit.

---

### Question #11
**Question:** App Service backup configuration. Statements about backups.

**Answer:** Based on specific backup settings.

**Explanation:** Backup configuration determines what is backed up.

---

### Question #12
**Question:** SSPR with security questions. Statements about password reset.

**Answer:** Based on SSPR configuration and user types.

**Explanation:** Administrative accounts have SSPR restrictions.

---

### Question #13
**Question:** User1 creates external tenant. Need to create user accounts.

**Answer:** A. Yes (User1 is Global Administrator)

**Explanation:** Global Administrators can create users in any tenant.

---

### Question #14
**Question:** Monitor latency between on-premises network and virtual machines.

**Answer:** C. Network Performance Monitor

**Explanation:** Network Performance Monitor measures latency between locations.

---

### Question #15
**Question:** CPU usage for ASP1. Times CPU exceeded threshold? Scale up or out?

**Answer:** four times, scaled up.

**Explanation:** CPU spikes indicate need for larger instance (scale up).

---

### Question #16
**Question:** Restore deleted files from Linux VM to on-premises Windows server. Four actions.

**Answer:** 1. File Recovery from vault, 2. Select restore point, 3. Download and run script, 4. Copy files.

**Explanation:** File Recovery mounts disks for file access.

---

### Question #17
**Question:** Protect VM1 with Azure Backup at 01:00 for 30 days.

**Answer:** Create Recovery Services vault, Create backup policy.

**Explanation:** Vault and policy are required for VM backup.

---

### Question #18
**Question:** Alert rule for System event log errors. Target resource?

**Answer:** D. Azure Log Analytics workspace

**Explanation:** Log Analytics workspace contains event logs for alerts.

---

### Question #19
**Question:** Identify unattached disks that can be deleted.

**Answer:** D. From Azure Cost Management, view Advisor Recommendations

**Explanation:** Advisor identifies unused resources for deletion.

---

### Question #20
**Question:** Provide developers with real-time HTTP 500 error access.

**Answer:** A. From webapp1, enable Web server logging

**Explanation:** Web server logging captures HTTP error details.

---

### Question #21
**Question:** Monitor availability with multi-step web test. What to use?

**Answer:** B. Azure Application Insights

**Explanation:** Application Insights supports multi-step web tests.

---

### Question #22
**Question:** View event time, event name, affected resources for service outage.

**Answer:** AzureActivity table with project operator.

**Explanation:** Activity log contains subscription-level events.

---

### Question #23
**Question:** Recover VM1 to point eight days ago. Minimize downtime.

**Answer:** B. Restore VM1 using Replace existing restore configuration.

**Explanation:** Replace existing restores in-place with minimal downtime.

---

### Question #24
**Question:** Create data collection rule DCR1. Data sources and destinations?

**Answer:** VM1 as data source, Workspace1 as destination.

**Explanation:** DCRs collect from VMs and send to workspaces.

---

### Question #25
**Question:** Role assignment file. Statements about permissions.

**Answer:** Based on specific role assignments.

**Explanation:** RBAC roles determine permissions.

---

### Question #26
**Question:** Custom RBAC role. Statements about permissions.

**Answer:** Based on specific role definition.

**Explanation:** Custom roles define specific permissions.

---

### Question #27
**Question:** NSG1 configuration. Statements about traffic.

**Answer:** Based on specific NSG rules.

**Explanation:** NSG rules determine allowed/denied traffic.

---

### Question #28
**Question:** Connect Client1 to VNet2. What should you do?

**Answer:** C. Download and re-install VPN client configuration package.

**Explanation:** VPN client package must be updated with new routes.

---

### Question #29
**Question:** Role assignments in management groups. Statements about permissions.

**Answer:** Based on specific role assignments.

**Explanation:** Management group roles apply to all subscriptions.

---

### Question #30
**Question:** Monitor user activity across all subscriptions.

**Answer:** D. a Log Analytics workspace

**Explanation:** Log Analytics aggregates activity logs from multiple subscriptions.

---

### Question #31
**Question:** Back up Disk2 using Azure Backup. Three actions.

**Answer:** 1. Create Recovery Services vault, 2. Configure backup for Disk2, 3. Run backup.

**Explanation:** Backup requires vault, configuration, and execution.

---

### Question #32
**Question:** Prevent hosts on Subnet1 from connecting to Azure portal.

**Answer:** C. Service Tag

**Explanation:** Service Tag for Azure Portal blocks access to portal IPs.

---

### Question #33
**Question:** View error events from Event table. Which query?

**Answer:** A. search in (Event) "error"

**Explanation:** Search operator finds error events.

---

### Question #34
**Question:** Collect performance traces for App1.

**Answer:** A. Azure Application Insights Profiler

**Explanation:** Profiler collects performance traces for web apps.

---

### Question #35
**Question:** Back up App1. Minimize costs. Which storage account?

**Answer:** D. storage4 (BlobStorage with LRS)

**Explanation:** LRS is lowest cost for backup storage.

---

### Question #36
**Question:** Alert rules triggered by User1 and User2 actions.

**Answer:** Based on specific alert rules configuration.

**Explanation:** Activity log alerts trigger on resource operations.

---

### Question #37
**Question:** Ensure NGINX available on VMs in scale set.

**Answer:** A. a Desired State Configuration (DSC) extension

**Explanation:** DSC extension configures VMs during deployment.

---

### Question #38
**Question:** Minimum service endpoints for VNET1 to communicate with VNET2 and access storage.

**Answer:** D. 5

**Explanation:** Service endpoint needed for each service (storage1, storage2, Azure AD).

---

### Question #39
**Question:** Configure contoso.azurewebsites.net to host www.contoso.com.

**Answer:** C. Create a CNAME record named asuid that contains the domain verification ID.

**Explanation:** Domain verification requires asuid record.

---

### Question #40
**Question:** Azure Monitor Network Insights alert for suspicious network traffic.

**Answer:** D. Configure NSG flow logs.

**Explanation:** NSG flow logs provide network traffic data.

---

### Question #41
**Question:** Alert rule and alert processing rule. Statements about notifications.

**Answer:** Based on specific rule configuration.

**Explanation:** Processing rules can suppress notifications.

---

### Question #42
**Question:** Secondary copy of blob data in East US region. Minimize administrative effort.

**Answer:** C. geo-redundant storage (GRS)

**Explanation:** GRS automatically replicates to secondary region.

---

### Question #43
**Question:** Collect performance data and events from VMs to two workspaces.

**Answer:** A. the Azure Monitor agent

**Explanation:** Azure Monitor agent supports multi-homing to multiple workspaces.

---

### Question #44
**Question:** Alert rule to run App1 if VM1 stops.

**Answer:** C. an action group

**Explanation:** Action groups define actions for alerts.

---

### Question #45
**Question:** Dashboard with metrics and network topology for ExpressRoute.

**Answer:** A. Azure Monitor Network Insights

**Explanation:** Network Insights provides topology and metrics.

---

### Question #46
**Question:** Diagnose connectivity issue on port 33000. Which options?

**Answer:** BC. IP flow verify and Azure Monitor Network Insights

**Explanation:** Both can diagnose network connectivity issues.

---

### Question #47
**Question:** Email alert when resource lock removed.

**Answer:** A. a resource, a condition, and an action group

**Explanation:** Activity log alert requires resource, condition, and action group.

---

### Question #48
**Question:** Alerts exhibit. Statements about alert status.

**Answer:** Based on specific alert configurations.

**Explanation:** Alert status indicates triggered/acknowledged state.

---

## TOPIC 7 - TESTLET 1 (CONTOSO MANUFACTURING)

---

### Question #1
**Question:** Device settings to meet technical requirements - only Pilot group can join devices, users verify with mobile phone.

**Answer:** Selected for users joining devices, Yes for requiring MFA.

**Explanation:** Device settings control who can join devices and MFA requirements.

---

### Question #2
**Question:** Meet requirement for Admin1 as service admin and receiving email alerts.

**Answer:** D. From Subscriptions blade, select subscription, modify Properties.

**Explanation:** Service admin is set in subscription properties.

---

## TOPIC 8 - TESTLET 10 (CONTOSO CONSULTING)

---

### Question #1
**Question:** Azure Backup for file shares and VMs. Minimum Recovery Services vaults and backup policies?

**Answer:** 3 vaults (one per region), 6 policies (one per service per vault).

**Explanation:** Vaults are per region. Each vault needs separate policies for files and VMs.

---

### Question #2
**Question:** Configure alerts for VM1 and VM2 free space. Three actions.

**Answer:** 1. Enable guest OS monitoring, 2. Create metric alert, 3. Configure action group.

**Explanation:** Guest OS monitoring required for disk metrics.

---

## TOPIC 9 - TESTLET 2 (CONTOSO CONSULTING)

---

### Question #1
**Question:** User1 create initiative definitions, User4 assign initiatives to RG2.

**Answer:** User1: Contributor or Policy Contributor. User4: Contributor or Policy Contributor.

**Explanation:** Policy creation and assignment require specific roles.

---

### Question #2
**Question:** Grant Group4 read-only permissions to Azure file shares.

**Answer:** A. On storage2, enable identity-based access for the file shares.

**Explanation:** Identity-based access enables Azure AD permissions for file shares.

---

## TOPIC 10 - TESTLET 3 (CONTOSO MANUFACTURING)

---

### Question #1
**Question:** Implement backup solution for App1. What should you create first?

**Answer:** D. a Recovery Services vault

**Explanation:** Vault is the container for backups.

---

### Question #2
**Question:** Move blueprint files to Azure.

**Answer:** B. Use Azure Storage Explorer to copy the files.

**Explanation:** Storage Explorer copies files over internet.

---

### Question #3
**Question:** Storage requirements statements.

**Answer:** Based on specific requirements for VMs and blobs.

**Explanation:** Unmanaged disks use page blobs. Blueprint files use blob storage.

---

## TOPIC 11 - TESTLET 4 (CONTOSO CONSULTING)

---

### Question #1
**Question:** Create container1 and share1. Which storage accounts?

**Answer:** container1 in storage2 (BlobStorage). share1 in storage2 (General Purpose v2).

**Explanation:** Blob containers in BlobStorage or GPv2. File shares in GPv2.

---

### Question #2
**Question:** Create storage5. Which type and destination?

**Answer:** General Purpose v2, destination storage account.

**Explanation:** Object replication requires GPv2 accounts.

---

### Question #3
**Question:** Storage account for flow logging with 8-month retention.

**Answer:** C. storage3 (BlobStorage)

**Explanation:** Lifecycle management in BlobStorage handles retention.

---

## TOPIC 12 - TESTLET 5 (LITWARE CONSULTING)

---

### Question #1
**Question:** Verify VM3 outbound TCP port 8080 connectivity issue. What to use?

**Answer:** E. IP flow verify in Azure Network Watcher

**Explanation:** IP flow verify tests if packet is allowed/denied by security rules.

---

## TOPIC 13 - TESTLET 6 (LITWARE CONSULTING)

---

### Question #1
**Question:** Ensure VM1 can communicate with VM4. Minimize administrative effort.

**Answer:** C. Assign VM4 an IP address of 10.0.1.5/24.

**Explanation:** Correct IP configuration enables communication.

---

### Question #2
**Question:** Connect New York office to VNet1 over internet with encrypted connection.

**Answer:** Create virtual network gateway and local network gateway, configure site-to-site VPN.

**Explanation:** Site-to-site VPN provides encrypted internet connection.

---

## TOPIC 14 - TESTLET 7 (CONTOSO MANUFACTURING)

---

### Question #1
**Question:** App1 solution with N-tier architecture and SQL Server.

**Answer:** Deploy VMs in separate subnets for each tier. Use NSGs to minimize open ports.

**Explanation:** N-tier architecture separates tiers by subnet. NSGs control traffic between tiers.

---

### Question #2
**Question:** Provide users access to App1.

**Answer:** A. Create incoming security rule for port 443 from Internet. Associate NSG to web server subnet.

**Explanation:** Users access web front end over HTTPS. NSG on web server subnet allows access.

---

## TOPIC 15 - TESTLET 8 (CONTOSO CONSULTING)

---

### Question #1
**Question:** NSG1 and NSG2 implementations. Statements about VM access.

**Answer:** Based on specific NSG rules and associations.

**Explanation:** NSG rules determine allowed/denied traffic.

---

### Question #3
**Question:** Add VM1 and VM2 to LB1 backend pool. What should you do first?

**Answer:** A. Connect VM2 to VNET1/Subnet1.

**Explanation:** Both VMs must be in same subnet for internal load balancer.

---

### Question #4
**Question:** Ensure VM1 can communicate with VM4. Minimize administrative effort.

**Answer:** D. Establish peering between VNET1 and VNET3.

**Explanation:** Peering connects VNets with minimal effort.

---

## TOPIC 16 - TESTLET 9 (LITWARE CONSULTING)

---

### Question #1
**Question:** Implement custom role Role1. Which command to run first?

**Answer:** Get-AzRoleDefinition to export Reader role definition.

**Explanation:** Custom role based on Reader requires exporting the Reader role definition.

---

### Question #2
**Question:** Automate MFA configuration for finance department users.

**Answer:** B. dynamic groups and conditional access policies

**Explanation:** Dynamic groups include finance users. Conditional access enforces MFA.

---

# END OF DOCUMENT

---

**Instructions to create your downloadable document:**

1. Copy all the content above
2. Paste into Microsoft Word, Google Docs, or any text editor
3. Save as .docx, .pdf, or .txt file

**Good luck with your AZ-104 exam!**
