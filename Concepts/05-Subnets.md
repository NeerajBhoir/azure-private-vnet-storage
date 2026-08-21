# Azure Subnets

## Definition

A subnet is a smaller network segment created from a VNet address space.

---

## Purpose

- Network Segmentation
- Security Isolation
- Better Organization
- Easier Management

---

## Project Example

### App Subnet

```text
snet-app

10.10.1.0/24
```

Used for:

```text
Applications
Virtual Machines
```

### Private Endpoint Subnet

```text
snet-privateendpoint

10.10.2.0/24
```

Used for:

```text
Private Endpoints
```

---

## Architecture

```text
VNet
|
|-- snet-app
|
|-- snet-privateendpoint
```

---

## Why Separate Subnets?

To isolate application workloads from private service connectivity and improve network management.

---

## Key Learning

Subnets help organize resources and apply different security policies within a VNet.