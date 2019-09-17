# Azure Storage

Focus on Azure Data Lake, where it can be mounted, how to ingest data (to ADLS, from ADLS) ADF, Polybase, ACLs, integrating security with Databrick, etc.

## Labs
### DP-200 Courseware labs
It is not enough, you need to know the difference between ADL Gen1 & Gen2 and use Data factory to move data around
- [Case study](https://github.com/MicrosoftLearning/DP-200-Implementing-an-Azure-Data-Solution/blob/master/instructions/course-case-study.md)
- Create storage account, upload files, Create ADLSv2 [link](https://github.com/MicrosoftLearning/DP-200-Implementing-an-Azure-Data-Solution/blob/master/instructions/dp-200-02_instructions.md)

### Other Labs
- In depth lab from AZ-103, working with signatures, redundancy, etc. [link](https://github.com/MicrosoftLearning/AZ-103-MicrosoftAzureAdministrator/blob/master/Instructions/Labs/03%20-%20Implement%20and%20Manage%20Storage%20(az-100-02).md)
- Another basic HOL [link](https://github.com/MSRConnections/Azure-training-course/blob/master/Content/Storage/Azure%20Storage%20HOL.md)
- ADL Gen1 [link](https://github.com/MSRConnections/Azure-training-course/blob/master/Content/Data%20Lake/Azure%20Data%20Lake%20HOL.md)

## Demo

```bash
export loc="northeurope"
export rg="storage-ec-rg01"
az login
az group create -n $rg -l $loc
az extension add -n storage-preview
az storage account create -n ec-train-adls01 -l $loc -g $rg --sku Standard_LRS --kind StorageV2 --hierarchical-namespace true
az group delete $rg
```
