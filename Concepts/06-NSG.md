# Network Security Group (NSG)

## Definition

A Network Security Group (NSG) is an Azure Layer 3 and Layer 4 firewall used to control inbound and outbound traffic.

---

## Filters Traffic Based On

- Source IP
- Destination IP
- Port
- Protocol

---

## Example

```text
Allow TCP 443

Deny Everything Else
```

---

## Inbound Traffic

Traffic entering a resource.

Example:

```text
Internet

↓

VM
```

---

## Outbound Traffic

Traffic leaving a resource.

Example:

```text
VM

↓

Storage Account
```

---

## Stateful Firewall

NSG is Stateful.

If a request is allowed:

```text
Client

↓

Server
```

The return traffic is automatically allowed.

---

## Associations

NSG can be attached to:

- Subnet
- Network Interface (NIC)

---

## Key Learning

NSG provides network-level traffic filtering inside Azure.