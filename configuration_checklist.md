# Azure ML Private Networking Worksheet

## Network Information

### VNET Information

| Name        |        Address Space |
|:------------|---------------------:|
| *Vnet Name* | *VNet Address Space* |

[ ] - Verify custom DNS is configured on the Azure VNet to allow for private link resolution.

### Subnet Information

| Subnet Name    |           Address Space |
|:---------------|------------------------:|
| *Subnet1 Name* | *Subnet1 Address Space* |
| *Subnet2 Name* | *Subnet2 Address Space* |

## Storage

### Storage Configuration

| Item                 |                 Configuration |
|:---------------------|------------------------------:|
| Storage Account Name |                               |
| Blob FQDNS           |  (Name).blob.core.windows.net |
| PE Created for Blob  |                               |
| File FQDNS           |  (Name).file.core.windows.net |
| PE Created for File  |                               |
| Queue FQDNS*         | (Name).queue.core.windows.net |
| PE Created for Queue |                               |
| Table FQDNS *        | (Name).table.core.windows.net |
| PE Created for Table |                               |

### Validate Storage Private Connectivity

| Task                                   | (Y/N) |
|:---------------------------------------|------:|
| All zones linked to DNS Forwarder VNet |       |
| Conditional Forwards created for…      |       |
| -	blob.core.windows.net                |       |
| -	file.core.windows.net                |       |
| -	queue.core.windows.net               |       |
| -	table.core.windows.net               |       |
| Can resolve private IPs for…           |       |
| -	blob                                 |       |
| -	file                                 |       |
| -	table                                |       |
| -	queue                                |       |

## KeyVault

| Item                                  |                        |
|---------------------------------------|-----------------------:|
| KeyVault Name                         |                        |
| PE Created                            |                        |
| Vault FQDNS                           | (Name).vault.azure.net |
| DNS Zone linked to DNS forwarder VNet |                        |
| Conditional forward created for       |                        |
| - vault.azure.net                     |                        |
| - vaultcore.azure.net                 |                        |
| Can resolve private IPs for Vault     |                        |

## Azure Container Registry

| Item                                       |                   |
|--------------------------------------------|-------------------|
| ACR Name                                   |                   |
| PE Created                                 |                   |
| ACR FQDNS                                  | (Name).azurecr.io |
| DNS Zone linked to DNS forwarder VNet      |                   |
| Conditional forward created for azurecr.io |                   |
| Can resolve private IPs for                |                   |
| - Login                                    |                   |
| - Data Endpoint                            |                   |
| Admin User enabled                         |                   |

## Azure ML Workspace

| Item                                                                     |   |
|--------------------------------------------------------------------------|---|
| Azure ML Workspace Name                                                  |   |
| PE Created                                                               |   |
| DNS Zones Linked to DNS forwarder VNet                                   |   |
| Conditional forwards created for                                         |   |
| - notebooks.azure.net                                                    |   |
| - api.azureml.ms                                                         |   |
| - notebooks.azure.net                                                    |   |
| - instances.azureml.ms                                                   |   |
| - aznbcontent.net                                                        |   |
| Workspace Identity granted Reader access to all of the private endpoints |   |
