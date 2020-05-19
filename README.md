# DP-200 Azure Data Solution - Implementation
Couple of remarks about course and training of Azure Data Solutions

Free training materials (courseware) on FutureProof [website](https://future-proof.net/track/implementing-an-azure-data-solution)

You need trial account, azure pass or other access to Microsoft Azure. The best practice is to use separate purpose build account for this task. For example, create new gmail account, then create new Microsoft account for this new email, redeem code for new account (or use credit card for trial account verification). Credit card for trial account cannot be connected to Azure ever before. Electronic credit card can be used. For trial account, the card is used only for verification and is never charged.

Install Azure CLI. Azure CLI is preferred command line tool to work with Azure. It is multiplatform tool (you can run Azure CLI on MacOS, Linux, Windows and if you try little bit harder even on BSD like UNIX).

For convenient PowerShell experience install latest version of PowerShell and install Az module. There was big change in Azure modules on the beginning of the year 2019. You can still find two different command sets (AzureRmSomething, AzSomething). Try to use Az version whenever it is possible, it is newer with bright future. Even reworking older syntax (AzureRm) to new one will pay off in the future.

## Setup training environment
1. Get dummy mail account (like Yahoo) eg. myname01@yahoo.com. 
2. Create Microsoft account for this email
3. Open Azure pass page, Sign in with MS Account
4. Redeem the code

## Azure account links
* [Yahoo](https://www.yahoo.com/?guccounter=1)
* [MS Account](https://account.microsoft.com/account?lang=en-us)
* [Redeem pass](https://www.microsoftazurepass.com/)

## Exam
- Not the easiest one, but not so difficult if you compare it to AZ-300 even to AZ-103
- Broad range of technologies is covered in some depth
- No virtual labs :-(  
- Databricks - spin up cluster, working with notebook, connecting to data, basic libraries, Spark, Python
- Storage - focus on Data Lake Gen 2 (but Gen 1 as well), loading blobs, using polybase, mounting to Databricks, security
- CosmosDB - scalability, avaliability, partitioning, RU
- Azure SQL RDBMS - more DW than SQL, Polybase, ADF load, partitioning (indexes, distributing tables to node), vCPU, DTU, DWU
- Stream Analytics - SU, IoT hub, Event hub/ Event grid, storage, azure functions
- ADF - basic concepts, transformations, SSIS
- Monitoring - Azure Log analytics, Alerts, Actions
- Security - how to secure data TDE, RLS, CLS, RBAC, AAD, keys, credentials

## Recommended preparation for exam
- Practice, practice, practice
- This exam does have a lab. Circa ten tasks about setting something in Azure portal / no code writing
- There is Measure Up practice test for this exam [MeasureUp](https://www.measureup.com/dp-200-microsoft-implementing-an-azure-data-solution.html)

## Usuall schedule
1. [Azure for the Data Engineer](mod01/Intro.md)
2. [Working with Data Storage](mod02/Storage.md)
3. [Enabling Team Based Data Science with Azure Databricks](mod03/DataBrick.md)
4. [Building Globally Distributed Databases with Cosmos DB](mod04/CosmosDB.md)
5. [Working with Relational Data Stores in the Cloud](mod05/AzureRDBMS.md)
6. [Performing Real-Time Analytics with Stream Analytics](mod06/AzureStream.md)
7. [Orchestrating Data Movement with Azure Data Factory](mod07/ADF.md)
8. [Securing Azure Data Platforms](mod08/AzureDataSecurity.md)
9. [Monitoring and Troubleshooting Data Storage and Processing](mod09/Monitoring.md)




## Software links
Not all the software is essential, but it is recomended software for working with Azure.

* [Visual Studio Community Edition](https://visualstudio.microsoft.com/vs/community/)
* [Visual Studio Code Azure Account Extension](https://marketplace.visualstudio.com/items?itemName=msvscode.azure-account)
* [Visual Studio Code Azure Resource Manager Tools Extension](https://marketplace.visualstudio.com/items?itemName=msazurermtools.azurerm-vscode-tools)
* [Visual Studio Code Azure CLI Tools Extension](https://marketplace.visualstudio.com/items?itemName=msvscode.azurecli)
* [Visual Studio Code PowerShell Extension](https://marketplace.visualstudio.com/items?itemName=msvscode.PowerShell)
* [Visual Studio Code C# Extension](https://marketplace.visualstudio.com/items?itemName=msvscode.csharp)
* [Visual Studio Code Docker Extension](https://marketplace.visualstudio.com/items?itemName=msazuretools.vscode-docker)
* [PowerShell 6](https://github.com/PowerShell/PowerShell/releases/latest/)
* [Azure PowerShell](https://docs.microsoft.com/powershell/azure/install-az-ps)
* [Azure CLI](https://docs.microsoft.com/cli/azure/install-azure-cli)
* [Azure Storage Explorer](https://azure.microsoft.com/features/storage-explorer/)
* [Azure Data Studio](https://docs.microsoft.com/en-us/sql/azure-data-studio/)
* [Git for Windows](https://git-scm.com/download/win)
* [.NET Core 3.1.1 SDK](https://dotnet.microsoft.com/download)
* [.NET Tool - HttpRepl](https://github.com/dotnet/HttpRepl)
* [.NET Tool - Entity Framework Core Tools](https://docs.microsoft.com/ef/core/miscellaneous/cli/dotnetosoft.com/p/windows-terminalpreview/9n0dx20hk701)
* [Edge (Chromium)](https://www.microsoft.com/edge)
* [Docker](https://docs.docker.com/docker-for-windows/install/)
* [Windows Terminal](https://www.microsoft.com/p/windows-terminalpreview/9n0dx20hk701)


## Training sessions specific schedule

### 17.09.2019 - Warszawa

1. [Azure for the Data Engineer](mod01/Intro.md)
2. [Working with Data Storage](mod02/Storage.md)
3. [Building Globally Distributed Databases with Cosmos DB](mod04/CosmosDB.md)
4. [Working with Relational Data Stores in the Cloud](mod05/AzureRDBMS.md)
5. [Securing Azure Data Platforms](mod08/AzureDataSecurity.md)


6. [Orchestrating Data Movement with Azure Data Factory](mod07/ADF.md)
7. [Enabling Team Based Data Science with Azure Databricks](mod03/DataBrick.md)
8. [Performing Real-Time Analytics with Stream Analytics](mod06/AzureStream.md)
9. [Monitoring and Troubleshooting Data Storage and Processing](mod09/Monitoring.md)
