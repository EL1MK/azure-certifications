# AZ‑500 LAB07: Implementing Secure Data with Always Encrypted & Azure Key Vault

🎯 **Objective**

This lab focuses on securing sensitive data in Azure SQL Database using **Always Encrypted** with **Azure Key Vault**. It demonstrates how to protect data in use, enforce client‑side encryption, and manage encryption keys securely—aligned with the **Implement data and application protection** module of the AZ‑500 certification.

## 📚 Context

This lab is based on the official Microsoft Learning exercise **LAB_07_KeyVaultImplementingSecureDatabysettingupAlwaysEncrypted**.

It highlights:

- Deploying Azure SQL Database and Azure Key Vault  
- Creating and managing encryption keys in Key Vault  
- Configuring Always Encrypted columns  
- Using SQL Server Management Studio (SSMS) to encrypt data  
- Testing encrypted column behavior from client applications  

## 🧪 Planned Steps

1. **Deploy Azure Resources**
   - Azure SQL Database  
   - Azure Key Vault  
   - Access policies and permissions
   - App Registration  

2. **Create Encryption Keys and Secrets**
   - Key stored in Azure Key Vault  
   - Secret stored in Azure Key Vault

3. **Configure Always Encrypted**
   - Select sensitive columns  
   - Apply deterministic encryption  
   - Encrypt data using SSMS wizard  

4. **Validate Encryption Behavior**
   - Test access using SSMS and .NET client  
   - Observe ciphertext vs plaintext behavior  

## 🧠 Personal Notes

All walkthrough steps, command outputs, and observations will be documented in the `notes/` folder.

## 📸 Screenshots

Screenshots will be added to the `screenshots/` folder.

## 🧩 Deployment Files & Scripts

- ARM templates for deploying resources
- C# file (application code)

## 📎 References

- Microsoft Learn: Azure Key Vault  
- Microsoft Learn: Always Encrypted  
- Microsoft Learn: SQL Client Encryption  
- AZ‑500 Learning Path: Implement data and application protection  
