# Azure ML Private Netowrking Worksheet

## Network Information

### VNET Information

| Name        |        Address Space |
|:------------|---------------------:|
| *Vnet Name* | *VNet Address Space* |

### Subnet Information

| Subnet Name    |           Address Space |
|:---------------|------------------------:|
| *Subnet1 Name* | *Subnet1 Address Space* |
| *Subnet2 Name* | *Subnet2 Address Space* |

## Storage

### Storage Configuration

| Item                         | Configuration |
|:-----------------------------|--------------:|
| Storage Account Name         |               |
| Blob Private Endpoint Name   |               |
| Blob FQDNS                   |               |
| File Private Endpoint Name   |               |
| File FQDNS                   |               |
| Queue Private Endpoint Name* |               |
| Queue FQDNS*                 |               |
| Table Private Endpoint Name* |               |
| Table FQDNS *                |               |

### Validate Storage Private Connectivity

| Task                                   | (Y/N) |
|:---------------------------------------|------:|
| All zones linked to DNS Forwarder VNet |       |
| All zones linked to ML VNet            |       |
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









