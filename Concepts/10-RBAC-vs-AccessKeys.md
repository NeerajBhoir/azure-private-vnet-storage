# RBAC vs Access Keys

## Access Keys

Access Keys provide account-wide access to a Storage Account.

### Characteristics

- Shared Secret
- Full Access
- Harder to Audit

---

## RBAC

Role Based Access Control uses Azure identities and roles to control permissions.

### Characteristics

- Identity Based
- Granular Permissions
- Easy Auditing
- Least Privilege

---

## Example Roles

### Storage Blob Reader

Can:

```text
Read
```

Cannot:

```text
Write
Delete
```

---

### Storage Blob Contributor

Can:

```text
Read
Write
Delete
```

---

## Which Is More Secure?

RBAC

Because permissions are assigned to identities rather than shared secrets.

---

## Key Learning

RBAC is the preferred authorization mechanism in enterprise environments.