# Public Endpoint

## Definition

A Public Endpoint is the default access method for Azure Storage Accounts.

---

## Architecture

```text
Internet
    |
    |
Storage Account
```

---

## Example

```text
storage01finance.blob.core.windows.net
```

This endpoint is reachable from the internet.

---

## Is It Secure?

Public Endpoints can still be secured using:

- RBAC
- Access Keys
- SAS Tokens
- Storage Firewalls

However, the endpoint remains internet-facing.

---

## Limitation

- Publicly reachable
- Larger attack surface
- May not satisfy compliance requirements

---

## Key Learning

Public Endpoint means the service is accessible through the internet even if authentication is still required.