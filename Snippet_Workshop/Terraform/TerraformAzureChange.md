## Add in main.tf
```
resource "azurerm_virtual_network" "vnet" {
  name                = "myTFVnet"
  address_space       = ["10.0.0.0/16"]
  location            = "westus2"
  resource_group_name = azurerm_resource_group.rg.name
}
```
## Apply the changes
```
terraform apply
```
## Modify an existing resource
```
tags = {
    Environment = "Terraform Getting Started"
    Team = "DevOps"
}
```
## Review updates to state
```
terraform show
```
## Get the updated state list of resources
```
terraform state list
```
