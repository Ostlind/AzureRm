# Azure Resource Manager Quickstart

## Prerequisites

* Basic knowledge about **[Powershell][Powershell link]**
* Basic knowledge about **[Microsoft Azure][Azure link]**

---

####This tutorial will go through 
1. How to install Powershell Azure Preview
2. 

- [x] a bigger project
  - [ ] first subtask #1234
  - [ ] follow up subtask #4321
  - [ ] final subtask cc @mention
- [ ] a separate task



## Subscription
---

To get started with Azure Resource Manager (referred form here on as ARM) you must have valid Azure subscription.

```PowerShell
#AzureRm Getting Started Script

Set-StrictMode -Version Latest

#Login

#Login-AzureRmAccount


# Initialize variables
$subscriptionName = "Visual Studio Premium with MSDN"

$location = "North Europe"

$resourceGroupName = "FabioFirstResourceGroup"

$storageAccountName = "fabiostorageacccount"

$scriptRootParent = Split-Path -Path $PSScriptRoot -Parent

$scriptRootParent = "D:\Azure"

$templateUriVM = "$scriptRootParent\azure-quickstart-templates\101-simple-windows-vm\azuredeploy.json"

$templateParemterFile = "$scriptRootParent\azure-quickstart-templates\101-simple-windows-vm\azuredeploy.parameters.json"

# Create new resource group

New-AzureRmResourceGroup -Name $resourceGroupName -Location $location

$deploymentParrameter =  @{ Name = "VmDeployment"; ResourceGroupName = $resourceGroupName; TemplateUri = $templateUriVM; TemplateParameterFile = $templateParemterFile  }

New-AzureRmResourceGroupDeployment @deploymentParrameter 

# Get subscriptions

Get-AzureRmSubscription –SubscriptionName $subscriptionName| Select-AzureRmSubscription 

Set-AzureRmCurrentStorageAccount –ResourceGroupName $resourceGroupName –StorageAccountName $storageAccountName | Out-Null


Get-AzureRmResourceGroup -Name $resourceGroupName


Get-AzureRmStorageAccount -ResourceGroupName  $resourceGroupName -Name $storageAccountName | Set-AzureRmCurrentStorageAccount | Out-Null

#Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob

Remove-AzureRmResourceGroup -Name $resourceGroupName -Force





```
=======
Azure Resource Manager related tutorials and content

![Concept](http://trevorsullivan.net/wp-content/uploads/2015/08/2015-09-06-16_59_10-New-notification-1024x707.png)


## Useful Links 
```PowerShell
 Login-AzureRm
 ```



[Powershell link]: http://powershell.com/cs/
[Azure link]: https://azure.microsoft.com/en-us/
[PowershellGallery link]: https://www.powershellgallery.com/
[PowershellGallery2 link]: https://github.com/Azure/azure-powershell/releases/tag/v1.0.0-preview-gallery-October2015
[Powershell 1.0 preview Blog]: https://azure.microsoft.com/en-us/blog/azps-1-0-pre/













































































[Link to Header](#azure-resource-manager-quickstart)