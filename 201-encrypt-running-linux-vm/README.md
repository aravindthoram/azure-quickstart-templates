# Enable encryption on a running Linux VM. 

<a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fazure%2Fazure-quickstart-templates%2Fmaster%2F201-encrypt-running-linux-vm%2Fazuredeploy.json" target="_blank">
    <img src="http://azuredeploy.net/deploybutton.png"/>
</a>

This template enables encryption on a running linux vm using AAD client secret. This template assumes that the VM is located in the same region as the resource group. If not, please edit the template to pass appropriate location for the VM sub-resources.

<br>
Prerequisites:
<br>
1. Azure Disk Encryption securely stores the encryption secrets in a specified Azure Key Vault. 
Use the below PS cmdlet for getting the "keyVaultSecretUrl" and "keyVaultResourceId"
Get-AzureRmKeyVault -VaultName $KeyVaultName -ResourceGroupName $rgname

References:
<br>
White paper - https://azure.microsoft.com/en-us/documentation/articles/azure-security-disk-encryption/
<br>
Powershell - http://blogs.msdn.com/b/azuresecurity/archive/2015/11/16/explore-azure-disk-encryption-with-azure-powershell.aspx
<br>
http://blogs.msdn.com/b/azuresecurity/archive/2015/11/21/explore-azure-disk-encryption-with-azure-powershell-part-2.aspx