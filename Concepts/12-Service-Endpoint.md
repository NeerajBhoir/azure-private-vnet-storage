# Service Endpoint

## Definition

A Service Endpoint allows Azure resources in a VNet to securely access Azure services through Microsoft's backbone network.

---

## Architecture

```text
VNet
 |
 |
Service Endpoint
 |
 |
Storage Account
```

---

## Benefits

- Traffic stays within Microsoft's network
- Improved security
- Storage firewall can restrict access to specific VNets

---

## Limitation

The Storage Account still has a Public Endpoint.

```text
storage01finance.blob.core.windows.net
```

still exists.

---

## Service Endpoint vs Private Endpoint

### Service Endpoint

```text
Traffic stays private

BUT

Public Endpoint still exists
```

### Private Endpoint

```text
Traffic stays private

AND

Storage gets a Private IP
```

---

## Key Learning

Service Endpoints improve connectivity but do not remove the public endpoint.