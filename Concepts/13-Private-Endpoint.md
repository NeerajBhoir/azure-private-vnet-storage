# Private Endpoint

## Definition

A Private Endpoint is a network interface that provides a private IP from a VNet to an Azure service.

---

## Project Example

```text
Private Endpoint

pe-neeraj-storage01

IP Address:

10.10.2.4
```

---

## Architecture

```text
Storage Account
 |
Azure Private Link
 |
Private Endpoint
 |
10.10.2.4
```

---

## Purpose

- Private Connectivity
- Better Security
- Reduced Attack Surface
- Compliance Requirements

---

## Why Not Service Endpoint?

Service Endpoint:

```text
Public Endpoint Still Exists
```

Private Endpoint:

```text
Storage Receives Private IP
```

and public access can be disabled.

---

## Key Learning

The Private Endpoint is the heart of the Azure Private Storage architecture.