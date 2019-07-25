# Allowed resource types (Microsoft Services only)

This policy allows only resources of type "Microsoft.*" to be deployed

## Try on Portal

[![Deploy to Azure](http://azuredeploy.net/deploybutton.png)](https://portal.azure.com/#blade/Microsoft_Azure_Policy/CreatePolicyDefinitionBlade/uri/https%3A%2F%2Fraw.githubusercontent.com%2seb2k%2Azure%2Policy%2Policy%2AllowedResourceTypesMicrosoftOnly%2azurepolicy.json)

## Try with PowerShell

````powershell
$definition = New-AzPolicyDefinition -Name "AllowedResourceTypesMicrosoftOnly" -DisplayName "Allowed resource types (Microsoft Services only)" -description "This policy allows only resources of type "Microsoft.*" to be deployed" -Policy 'https://raw.githubusercontent.com/seb2k/Azure/Policy/Policy/AllowedResourceTypesMicrosoftOnly/azurepolicy.rules.json' -Mode All
$definition
$assignment = New-AzPolicyAssignment -Name <assignmentname> -Scope <scope> -PolicyDefinition $definition
$assignment 
````

## Try with CLI

````cli

az policy definition create --name 'AllowedResourceTypesMicrosoftOnly' --display-name 'Allowed resource types (Microsoft Services only)' --description 'This policy allows only resources of type "Microsoft.*" to be deployed' --rules 'https://raw.githubusercontent.com/seb2k/Azure/Policy/Policy/AllowedResourceTypesMicrosoftOnly/azurepolicy.rules.json' --mode All

az policy assignment create --name <assignmentname> --scope <scope> --policy 'audit-keyvault-vnet-rules' 

````
