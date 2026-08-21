# Azure Private VNet Storage Architecture

## Objective

Build a secure Azure Storage solution where Blob Storage is accessible only through a Private Endpoint inside an Azure Virtual Network (VNet).

---

## Business Requirement

- Secure Blob Storage access
- Eliminate public internet exposure
- Enable private connectivity through Azure Private Link
- Use network segmentation
- Leverage RBAC for access control
- Support future enterprise scalability

---

## Resources Created

### Resource Group

```text
RG-neeraj-Storage01
```

### Virtual Network

```text
vnet-neeraj-storage01
```

Address Space:

```text
10.10.0.0/16
```

### Subnets

#### Application Subnet

```text
snet-app
10.10.1.0/24
```

#### Private Endpoint Subnet

```text
snet-privateendpoint
10.10.2.0/24
```

### Storage Account

```text
storage01finance
```

### Blob Containers

```text
backups
logs
documents
```

### Private Endpoint

```text
pe-neeraj-storage01
```

Private IP:

```text
10.10.2.4
```

---

## Architecture Diagram

```text
+--------------------------------------------------+
| VNet                                              |
| vnet-neeraj-storage01                             |
| Address Space: 10.10.0.0/16                       |
|                                                    |
| +---------------------------------------------+    |
| | App Subnet                                  |    |
| | snet-app                                    |    |
| | 10.10.1.0/24                                |    |
| |                                              |    |
| | Application / VM                             |    |
| +-------------------+-------------------------+    |
|                     | HTTPS 443                    |
|                     |                              |
|                     v                              |
| +---------------------------------------------+    |
| | Private Endpoint Subnet                     |    |
| | snet-privateendpoint                        |    |
| | 10.10.2.0/24                                |    |
| |                                              |    |
| | Private Endpoint                             |    |
| | pe-neeraj-storage01                          |    |
| | 10.10.2.4                                    |    |
| +-------------------+-------------------------+    |
+---------------------|------------------------------+
                      |
                      |
                Azure Private Link
                      |
                      v

            +----------------------+
            |  Storage Account     |
            |  storage01finance    |
            +----------+-----------+
                       |
                       |
                 Blob Storage
                       |
      +----------------+----------------+
      |                |                |
      v                v                v

   backups          logs          documents
```

---

## Packet Flow

```text
Application / VM
       |
       |
       v
snet-app
10.10.1.0/24
       |
       |
HTTPS 443
       |
       v
Private Endpoint
10.10.2.4
       |
       |
Azure Private Link
       |
       v
Storage Account
storage01finance
       |
       v
Blob Container
       |
       v
Blob File
```

---

## Security Controls

### Network Security

- VNet Isolation
- Subnet Segmentation
- Dedicated Private Endpoint Subnet
- Private Connectivity

### Storage Security

- Public Network Access Disabled
- Blob Storage Private Access
- HTTPS Only
- Encryption at Rest

### Identity Security

- Azure RBAC
- Least Privilege Principle

---

## Key Design Decisions

### Why Separate Subnets?

To isolate application workloads from private service connectivity.

### Why Private Endpoint?

To provide a private IP address for Azure Storage inside the VNet.

### Why Private Link?

To securely connect Azure resources without using the public internet.

### Why Private DNS?

To resolve the Storage Account FQDN to the Private Endpoint IP address.

### Why Disable Public Access?

To eliminate internet exposure and reduce the attack surface.

---

## Learning Outcomes

- Azure Virtual Network (VNet)
- Azure Subnets
- Azure Blob Storage
- Azure Storage Account
- Service Endpoint
- Private Endpoint
- Azure Private Link
- Private DNS
- RBAC
- Network Segmentation
- Secure Storage Architecture