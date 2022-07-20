# Azure-Key-Vault-Service

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
