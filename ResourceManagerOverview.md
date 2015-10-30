# Azure Resource Manager


![Consitent Managment Layer](http://image.slidesharecdn.com/architectingworldclassazureresourcemanagertemplates-150921152729-lva1-app6892/95/architecting-world-class-azure-resource-manager-templates-3-1024.jpg?cb=1442851386)
## Resource Group

	1. Container for multiple resources
	2. Resources exist in one resource group
	3. Resource groups can span regions
	4. Resource groups can span services 
	
## Imperativ or Declarative

```PowerShell
  New-AzureVM - VM $myVm
```

```Json
{
  "$schema": "https://..//deploymentTemplate.json#",
  "contentVersion": "1.0.0.0",
  "parameters",
  
}
```
## Deployment with Azure Resource Manager

  * template-driven
  * declarative
  * idempotent
  * multi-service
  * multi-region
  * extensible


    1. Tracks template execution
	2. Created within a resource group
	3. Allows nested deployments 
	
	
 