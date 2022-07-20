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
