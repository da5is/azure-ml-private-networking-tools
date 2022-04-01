# Azure ML Private Networking Worksheet

## Network Information

### VNET Information

| Name                 | Address Space |
|:---------------------|--------------:|
| vnet-azureml-east-01 |   10.0.0.0/16 |

[X] - Verify custom DNS is configured on the Azure VNet to allow for private link resolution.

### Subnet Information

| Subnet Name    | Address Space |
|:---------------|--------------:|
| TrainingSubnet |   10.0.0.0/24 |
| ScoringSubnet  |   10.0.1.0/24 |

## Storage

### Storage Configuration

| Item                 |                         Configuration |
|:---------------------|--------------------------------------:|
| Storage Account Name |                        saprivmleast01 |
| Blob FQDNS           |  saprivmleast01.blob.core.windows.net |
| PE Created for Blob  |                                     Y |
| File FQDNS           |  saprivmleast01.file.core.windows.net |
| PE Created for File  |                                     Y |
| Queue FQDNS*         | saprivmleast01.queue.core.windows.net |
| PE Created for Queue |                                     Y |
| Table FQDNS *        | saprivmleast01.table.core.windows.net |
| PE Created for Table |                                     Y |

### Validate Storage Private Connectivity

| Task                                   | (Y/N) |
|:---------------------------------------|------:|
| All zones linked to DNS Forwarder VNet |     Y |
| Conditional Forwards created for…      |       |
| -	blob.core.windows.net                |     Y |
| -	file.core.windows.net                |     Y |
| -	queue.core.windows.net               |     Y |
| -	table.core.windows.net               |     Y |
| Can resolve private IPs for…           |       |
| -	blob                                 |     Y |
| -	file                                 |     Y |
| -	table                                |     Y |
| -	queue                                |     Y |

## KeyVault

| Item                                  |                                        |
|---------------------------------------|---------------------------------------:|
| KeyVault Name                         |                 kv-ow-secureml-east-01 |
| PE Created                            |                                      Y |
| Vault FQDNS                           | kv-ow-secureml-east-01.vault.azure.net |
| DNS Zone linked to DNS forwarder VNet |                                      Y |
| Conditional forward created for       |                                        |
| - vault.azure.net                     |                                      Y |
| - vaultcore.azure.net                 |                                      Y |
| Can resolve private IPs for Vault     |                                      Y |

## Azure Container Registry

| Item                                       |                                |
|--------------------------------------------|-------------------------------:|
| ACR Name                                   |            acrowsecuremleast01 |
| PE Created                                 |                              Y |
| ACR FQDNS                                  | acrowsecuremleast01.azurecr.io |
| DNS Zone linked to DNS forwarder VNet      |                              Y |
| Conditional forward created for azurecr.io |                              Y |
| Can resolve private IPs for                |                                |
| - Login                                    |                              Y |
| - Data Endpoint                            |                              Y |
| Admin User enabled                         |                              Y |

## Azure ML Workspace

| Item                                                                     |                       |
|--------------------------------------------------------------------------|----------------------:|
| Azure ML Workspace Name                                                  | ml-orangewasp-east-01 |
| PE Created                                                               |                     Y |
| DNS Zones Linked to DNS forwarder VNet                                   |                     Y |
| Conditional forwards created for                                         |                       |
| - notebooks.azure.net                                                    |                     Y |
| - api.azureml.ms                                                         |                     Y |
| - notebooks.azure.net                                                    |                     Y |
| - instances.azureml.ms                                                   |                     Y |
| - aznbcontent.net                                                        |                     Y |
| Workspace Identity granted Reader access to all of the private endpoints |                     Y |
