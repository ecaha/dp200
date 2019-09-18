# Data Bricks


```bash
export loc="northeurope"
export rg="ectraindatabricks01"
export sqlserver="ectrainsqldb01"
export user="erycek"
export pwd="JatrovaPastika321"
export myip="1.2.3.4"

az group create -g $rg -l $loc

###TODO### 
#Create SQLDW with sample data
# az sql server create -l $loc -g $rg -n $sqlserver -u $user -p $pwd
#### Create sqldw with sample data from portal

az sql server firewall-rule create -g $rg -s $sqlserver -n myip --start-ip-address $myip --end-ip-address $myip
```

## Labs
Courseware lab [link](https://github.com/MicrosoftLearning/DP-200-Implementing-an-Azure-Data-Solution/blob/master/instructions/dp-200-03_instructions.md)

[Demo](https://github.com/midomsft/DatabricksHOL#targetText=Intro%20To%20Azure%20Databricks%20Hands,engineering%20and%20data%20science%20platform.md)
