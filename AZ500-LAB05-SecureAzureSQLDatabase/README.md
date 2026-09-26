# AZ‑500 LAB05: Securing Azure SQL Database

🎯 **Objective**

This lab focuses on securing Azure SQL Database using native Azure security capabilities. It demonstrates how to protect data, classify sensitive information, detect threats, and audit database activity—aligned with the **Plan and implement security for Azure SQL Database** module of the AZ‑500 certification.


## 📚 Context

This lab is based on the official Microsoft Learning exercise **LAB_05_SecuringAzureSQLDatabase**.

It highlights:

- Deploying an Azure SQL Database using an ARM template  
- Enabling **Microsoft Defender for SQL**  
- Classifying sensitive data with **SQL Information Protection**  
- Configuring **SQL Auditing** at server and database level  
- Reviewing security recommendations and audit logs  


## 🧪 Planned Steps

1. **Deploy an Azure SQL Database**
   - Use the provided ARM template (`azuredeploy.json`)
   - Validate deployment (SQL server + SQL database)

2. **Enable Advanced Data Security**
   - Activate Microsoft Defender for SQL
   - Explore vulnerability assessment and threat detection

3. **Configure Data Classification**
   - Discover sensitive fields
   - Apply classification labels and review recommendations

4. **Enable SQL Auditing**
   - Configure server‑level auditing
   - Configure database‑level auditing
   - Inspect audit logs in the associated storage account


## 🧠 Personal Notes

All walkthrough steps, command outputs, and observations will be documented in the `notes/` folder.

## 📸 Screenshots

Screenshots will be added to the `screenshots/` folder to illustrate:

- SQL Database deployment  
- Microsoft Defender for SQL configuration  
- Data classification dashboard  
- Auditing setup  
- Audit logs in the storage account  

## 🧩 Deployment Files & Scripts

- ARM template:  
  - `azuredeploy.json` (from `Allfiles/Labs/11/`)


## 📎 References

- Microsoft Learn: Azure SQL Database security  
- Microsoft Learn: Microsoft Defender for SQL  
- Microsoft Learn: SQL Auditing  
- AZ‑500 Learning Path: Plan and implement security for Azure SQL Database  

