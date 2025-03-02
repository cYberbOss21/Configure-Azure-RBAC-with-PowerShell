# Configure-Azure-RBAC-with-PowerShell
This guide provides step-by-step instructions on configuring Azure Role-Based Access Control (RBAC) using PowerShell. It covers:

✅ Assigning built-in roles (Network Contributor, Storage Account Contributor)

✅ Creating and managing Azure Virtual Networks (VNets)

✅ Troubleshooting role assignment failures

✅ Creating custom roles using Azure Cloud Shell and JSON

✅ Resolving "Forbidden" permission errors

Perfect for cloud administrators, security professionals, and DevOps engineers who need to manage access control in Azure environments efficiently.

📌 Includes PowerShell commands & examples for easy implementation!


## 🔹 Assigning an Azure Built-In Role  

### **Step 1: Sign into the Admin Account**  
Ensure you have **sufficient privileges** to assign roles in Azure.  

### **Step 2: Assign the Network Contributor Role**  
- This role allows a user to **manage** network resources but **not access them**.  

#### 🔹 **Command to Assign the Role:**  
```powershell
New-AzRoleAssignment -ObjectId <User_Object_ID> -RoleDefinitionName "Network Contributor" -Scope "/subscriptions/<Subscription_ID>"
