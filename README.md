---

```markdown
# pfSense Home Lab Firewall

## Overview
This project documents a hands-on pfSense firewall home lab deployed in a virtualized environment. The lab demonstrates how pfSense operates as a perimeter firewall by separating WAN and internal networks, enforcing firewall rules, and logging traffic.

The objective of this project is to build practical familiarity with pfSense, firewall rule behavior, and traffic filtering in a realistic lab setup.

---

## Lab Environment

- pfSense Community Edition
- VirtualBox
- Internal client virtual machine for testing

pfSense is positioned as the central gateway between the external network (WAN) and one or more internal networks, mirroring a common enterprise firewall deployment.

---

## Network Architecture

```

Internet (NAT)
|
pfSense Firewall
|
Internal Network(s)
|
Client VM(s)

```

---

## Firewall Functionality Demonstrated

- WAN and LAN interface separation
- Stateful firewall behavior
- Inbound traffic restriction
- Outbound traffic control
- Firewall logging and visibility

---

## Firewall Rules Summary

| Purpose                            | Interface | Action             |
| ---------------------------------- | --------- | ------------------ |
| Allow internal traffic to internet | LAN       | Allow              |
| Block unsolicited inbound traffic  | WAN       | Block              |
| Restrict management access         | LAN       | Allow (restricted) |
| Default deny policy                | WAN       | Block              |

pfSense enforces an implicit deny rule to ensure a secure default configuration.

---

## Validation & Observations

- Internal systems successfully access external networks
- Unsolicited inbound connections are blocked
- Firewall logs record denied and allowed traffic
- Rule order directly impacts traffic flow

---

## Key Learnings

- Practical understanding of pfSense firewall operations
- Importance of interface-based rule placement
- Difference between inbound and outbound filtering
- How firewall logs support security monitoring and analysis

---

## Screenshots

All screenshots included in this repository were captured during the lab execution and demonstrate the firewall configuration and behavior.

The screenshots directory contains:

- Virtual machine configuration
- pfSense console output
- pfSense web dashboard
- LAN and WAN firewall rules

---

## Project Summary

This lab provided hands-on experience with deploying and operating a pfSense firewall in a controlled environment. The project reinforces foundational network security concepts and firewall administration skills relevant to entry-level SOC and security analyst roles.
