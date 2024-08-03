# PostgreSQL Database on Azure and Excel Data Upload

This guide provides a step-by-step process to create a PostgreSQL database in Azure and upload data from an Excel file to it.

## Step 1: Create an Azure PostgreSQL Database

### 1.1 Sign in to Azure Portal

1. Go to the [Azure Portal](https://portal.azure.com).
2. Sign in with your Azure account credentials.

### 1.2 Create a PostgreSQL Database

1. In the left-hand menu, select **Create a resource**.
2. Search for **Azure Database for PostgreSQL** and select it.
3. Click on **Create**.
4. Choose **Single Server** for the deployment option.
5. Fill in the required fields:
   - **Subscription**: Choose your Azure subscription.
   - **Resource Group**: Create a new resource group or use an existing one.
   - **Server Name**: Provide a unique name for your PostgreSQL server.
   - **Data Source**: Choose **None** (start with a blank database).
   - **Location**: Choose a region close to you or with lower costs.
   - **Version**: Select the PostgreSQL version you want to use.
   - **Compute + Storage**: Choose the Basic pricing tier for lower costs.
   - **Administrator Account**: Create an admin username and password.
6. Review the configuration and click **Create**.
7. Wait for the deployment to complete.

## Step 2: Upload the Excel File to the PostgreSQL Database

### 2.1 Prepare Your Local Environment

Ensure you have the following Python libraries installed:
- **pandas**: For handling Excel files and data manipulation.
- **psycopg2**: PostgreSQL adapter for Python.
- **sqlalchemy**: SQL toolkit and Object-Relational Mapping (ORM) library.
- **openpyxl**: Library to read/write Excel files.

You can install these libraries using pip:

```bash
pip install pandas psycopg2-binary sqlalchemy openpyxl
