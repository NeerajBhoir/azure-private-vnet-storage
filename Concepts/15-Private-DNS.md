# Azure Private DNS

## Definition

Private DNS enables Azure resources to resolve service names to private IP addresses.

---

## Project Example

Storage Account:

```text
storage01finance.blob.core.windows.net
```

Private Endpoint:

```text
10.10.2.4
```

---

## Without Private DNS

```text
storage01finance.blob.core.windows.net

↓

Public IP
```

---

## With Private DNS

```text
storage01finance.blob.core.windows.net

↓

10.10.2.4
```

---

## DNS Zone

```text
privatelink.blob.core.windows.net
```

---

## Why Is It Needed?

Without Private DNS:

```text
Applications continue using
the public endpoint
```

With Private DNS:

```text
Applications automatically
use the private endpoint
```

---

## Key Learning

Private DNS ensures Azure Storage resolves to the Private Endpoint IP instead of a public address.