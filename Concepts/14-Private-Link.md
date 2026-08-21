# Azure Private Link

## Definition

Azure Private Link is the underlying technology that enables private connectivity between Azure services and a Virtual Network.

---

## Relationship

```text
Private Link

↓

Technology
```

```text
Private Endpoint

↓

Private IP in VNet
```

---

## Architecture

```text
Storage Account
 |
Private Link
 |
Private Endpoint
 |
VNet
```

---

## Purpose

- Secure Connectivity
- Private Data Path
- No Public Internet Dependency

---

## Real World Analogy

```text
Private Link

=

Private Tunnel
```

```text
Private Endpoint

=

Private Door
```

---

## Key Learning

Private Link provides the secure connection used by the Private Endpoint.