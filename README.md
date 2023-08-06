# Azure-Key-Vault-Service

# What can a Security Engineer use the Azure Key Vault Service for?
- Security Engineers can use an Azure Key Vault to secure store and programatically access secrets and certificates.

# What is the Azure Key Vault Service?
- Service used to store your secrets - encryption keys, certificates, and passwords
- Applications will use encryption keys, certificates, or passwords to connect to a SQL database or storage account
- Key vault stores them securely

# Azure Key Vault Diagram
<p align="center">
  
<img src="https://user-images.githubusercontent.com/104326475/180062528-bafc9ae6-2ba6-43bf-9e1b-f7a0604a70ba.png" height="100%" width="100%" alt="key vault"/>

<p/>

#  Create an Azure Key Vault
- Store a database password
- This secret will be used by your applications to access a database.
- An app can go ahead and take the value from the key vault but it must be authorized to. 


# Create an application object so that the application can link to it and access the key vault
- Go to Azure AD > App registrations > New registration > 
- The application object will represent the application and it will authorize itself.

# Add an access policy to allow the application object to access the key vault
- Select the object 
- Assign permissions




# What is the Soft Delete Feature of Azure Key Vault?
- Soft-delete feature will allow users to recover the key vault if it's been accidentaly deleted.
- If a secret is deleted, it's not permanently deleted. Commands can be performed in PowerShell to recover.
- If a user tries to create a secret with the same new as the deleted secret, there will be an error since it's a soft delete.
- Commands are on #226 of Udemy
- Purge commands are not given to an account admin. They have to be assigned. 




# Azure Key Vault offers two Authorization Systems - Access Policies (Legacy) vs Azure RBAC(Recommended)

# Access Policies - operate on the data plane only. It is used to give permissions when it comes to operations on the secrets/encryption keys
- List permissions is where users can view the key
- Get permissions is where users can get the value of the key
- The access policy model, on the other hand, is an legacy authorization system built in Key Vault to provide access to keys, secrets, and certificates. You can control access by assigning individual permissions to security principals (user, group, service principal, managed identity) at Key Vault scope.
<img src="https://github.com/earkevin11/Azure-Key-Vault-Service/assets/104326475/c3ee333a-6a92-423d-9ecc-5a610f24fb21" height="100%" width="100%" alt="key vault"/>

# Azure RBAC - Permission Model
- Azure RBAC - operates on the data plane and the management plane. It is used assigned to users or applications to manage the key vault itself, not the keys or secrets
- In order to work with data within the resources such as the Key Vault, special roles need to be assigned.


