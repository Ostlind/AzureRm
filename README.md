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
##How to install [Powershell 1.0.1 Preview]

First you must check that the current logged in user is allowed to executecute scripts

```PowerShell
Get-ExecutionPolicy -
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

![Concept](http://trevorsullivan.net/wp-content/uploads/2015/08/2015-09-06-16_59_10-New-notification-1024x707.png)
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
[Powershell 1.0.1 Preview]: https://www.powershellgallery.com/packages/AzureRM/










[To the top](#azure-resource-manager-quickstart)

