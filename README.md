[![Deploy to Azure](http://azuredeploy.net/deploybutton.png)](https://azuredeploy.net/)

# Azure Resource Manager Quickstart

In this tutorial we will learn how to setup and provision a Virtual Machine on _Azure_ with little
or no knowledge about _Powershell_ or _Azure_ using the Azure Resource Manager (ARM). I will only touch the surface of the topics and instead provide the reader with useful links 
that describes the topics in depth.  

## Prerequisites

* Basic knowledge about **[Powershell][Powershell link]**
* Basic knowledge about **[Microsoft Azure][Azure link]**

---

###In this tutorial we will learn how to 
1. Install _Azure Powershell 1.0 Preview_ module  
  * Enable Script Execution
  * Import and install
  * Uninstall the AzureRM component modules
Uninstall-AzureRM

# Uninstall AzureRM module
Uninstall-Module AzureRM

# Uninstall the Azure module
Uninstall-Module Azure
2. Login to _Azure Account_
3. How to create a _Azure Subscription Profile_
4. Create new _Resource Group_
5. Use _Azure Quick Templates_ **Json** files 
6. Deploy Resources to Azure Preview Portal    
 * Using inline parameters  
 * Using parameter object  
 * Using parameter file  

---
##How to install [Powershell 1.0.1 Preview]

**Enable script execution**  

To begin with you have to make sure that you have permission to run scripts on you local computer. This can be
made by executing the following [Cmdlet][Cmdlet Overview]
```PowerShell
Get-ExecutionPolicy
```
If the result is _Restricted_ you must enable it by executing   

```PowerShell
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned
```
There are several different execution policies that can be used but we will not cover them here. If you want to know more you can read [here][Execution Policy]

**Import, Install and Uninstall**

If you haven't downloaded the AzureRm module you can do it by using [Cmdlets][Cmdlet Overview] from [PowershellGet]. PowershellGet is built on top of the [OneGet] component and it enables simplified package management of [PowerShell modules] 

#### Install
```PowerShell
### To Install AzureRM module 
Install-Module AzureRM  

### To Install ARM cmdlet modules
Update-AzureRM
```
#### Import
After the modules are installed you can import AzureRM modules into your session. AzureRm is splitted into component modules for example cmdlets that relates to storage can be found in the AzureRm.storage module. 
This is how you import the AzureRm storage module
```PowerShell
### Only import the storage module
Import-Module AzureRM.Storage
```

If you want to import all of the modules 
```PowerShell
### Import all AzureRm modules
Import-AzureRM
```

#### Uninstall 

```PowerShell
# Uninstall the AzureRM component modules
Uninstall-AzureRM

# Uninstall AzureRM module
Uninstall-Module AzureRM
```

# Login to _Azure Account_

Before we start to work with ARM we have to login. After excuting this command you will be prompted to enter your username and password of your _Azure_ subscription
```PowerShell
### To login to ARM
Login-AzureRmAccount
```

## Subscription
---


To get started with Azure Resource Manager (referred form here on as ARM) you must have valid Azure subscription.

![Concept](http://trevorsullivan.net/wp-content/uploads/2015/08/2015-09-06-16_59_10-New-notification-1024x707.png)
## Useful Links 

[Powershell link]  
[Azure link]  
[PowershellGallery link]  
[PowershellGallery2 link]  
[Powershell 1.0.1 Preview]  

Fabbe
<script src="https://gist.github.com/Ostlind/f57dfd9f066b743e5e77.js"></script>
<script src="https://gist.github.com/Ostlind/f57dfd9f066b743e5e77.js"></script>

[Powershell link]: http://powershell.com/cs/
[Azure link]: https://azure.microsoft.com/en-us/
[PowershellGallery]: https://www.powershellgallery.com/
[PowershellGallery2 link]: https://github.com/Azure/azure-powershell/releases/tag/v1.0.0-preview-gallery-October2015
[Powershell 1.0.1 Preview]: https://www.powershellgallery.com/packages/AzureRM/
[Azure Quickstart Templates]: https://azure.microsoft.com/en-us/documentation/templates/
[Azure Quickstart Templates Github]: https://github.com/Azure/azure-quickstart-templates
[Cmdlet Overview]: https://technet.microsoft.com/en-us/library/ms714395(v=vs.85).aspx
[Execution Policy]: https://blog.netspi.com/15-ways-to-bypass-the-powershell-execution-policy/
[PowershellGet]: http://blogs.msdn.com/b/mvpawardprogram/archive/2014/10/06/package-management-for-powershell-modules-with-powershellget.aspx 
[PowershellGet Tutorial 1]: http://blogs.msdn.com/b/mvpawardprogram/archive/2014/10/06/package-management-for-powershell-modules-with-powershellget.aspx 
[OneGet]: https://github.com/oneget/oneget
[Powershell modules]: https://technet.microsoft.com/en-us/library/dd878324(v=vs.85).aspx
[To the top](#azure-resource-manager-quickstart)

