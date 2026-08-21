# Project Notes

## Use Case

Build Azure Storage reachable through a private IP inside a Virtual Network.

---

## Why VNet?

Provides:

- Network Isolation
- Private Communication
- IP Address Management

---

## Why Subnets?

Used to separate workloads.

### App Subnet

```text
10.10.1.0/24
```

### Private Endpoint Subnet

```text
10.10.2.0/24
```

---

## Why Separate Private Endpoint Subnet?

To isolate application workloads from private service connectivity.

---

## Why Private Endpoint?

Provides:

- Private IP Address
- Better Security
- Reduced Attack Surface
- No Public Exposure

---

## Why Private DNS?

Ensures:

```text
storage01finance.blob.core.windows.net
```

resolves to:

```text
10.10.2.4
```

instead of a public IP.

---

## Why Public Access Disabled?

Prevents storage access from the internet.

---

## Why RBAC?

Provides:

- Identity-Based Access
- Least Privilege
- Auditing

Preferred over Access Keys.

---

## Project Outcome

Storage Account successfully accessed through Azure Private Endpoint using private network connectivity.