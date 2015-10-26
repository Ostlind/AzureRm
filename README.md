# Azure Resource Manager Quickstart

In this tutorial we will learn how to setup and provision a Virtual Machine on _Azure_ with little
or no knowledge about _Powershell_ or _Azure_ using Azure Resource Manager (ARM). I will only touch the surface of the topics and instead provide the reader with useful links 
that describes the topics in depth.  

## Prerequisites

* Basic knowledge about **[Powershell][Powershell link]**
* Basic knowledge about **[Microsoft Azure][Azure link]**

---

###In this tutorial we will learn how to; 
1. Install _Azure Powershell 1.0 Preview_ module  
  * Import and install
2. Login to _Azure Account_
3. How to create a _Azure Subscription Profile_
4. Create new _Resource Group_
5. Use _Azure Quick Templates_ **Json** files 
6. Deploy Resources to Azure Preview Portal  

---
##How to install [Powershell 1.0 Preview]

First you must check that the current logged in user is allowed to execute cute scripts

```PowerShell
Set-ExecutionPolicy RemoteSigned
Install-Module AzureRM
Install-AzureRM

```


```PowerShell
Login-AzureRmAccount
```

## Subscription
---

To get started with Azure Resource Manager (referred form here on as ARM) you must have valid Azure subscription.


=======

## Useful Links 

[Powershell link]  
[Azure link]  
[PowershellGallery link]  
[PowershellGallery2 link]  
[Powershell 1.0 Preview]  



[Powershell link]: http://powershell.com/cs/
[Azure link]: https://azure.microsoft.com/en-us/
[PowershellGallery link]: https://www.powershellgallery.com/
[PowershellGallery2 link]: https://github.com/Azure/azure-powershell/releases/tag/v1.0.0-preview-gallery-October2015
[Powershell 1.0 Preview]: https://azure.microsoft.com/en-us/blog/azps-1-0-pre/










[To the top](#azure-resource-manager-quickstart)

