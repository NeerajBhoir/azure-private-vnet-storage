# Azure Firewall

## Definition

Azure Firewall is a managed, centralized network security service.

---

## NSG vs Azure Firewall

### NSG

Works at:

```text
Layer 3
Layer 4
```

Filters:

```text
IP
Port
Protocol
```

---

### Azure Firewall

Works at:

```text
Layer 3
Layer 4
Layer 7
```

Can inspect:

```text
Applications
URLs
Domains
FQDNs
```

---

## Features

- Application Filtering
- DNS Filtering
- Threat Intelligence
- Centralized Security

---

## Architecture

```text
Internet
    |
Azure Firewall
    |
Applications
```

---

## Key Learning

NSG provides traffic filtering, while Azure Firewall provides enterprise-grade centralized security.