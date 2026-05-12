# Basics #1: localhost and hosts file

Small project about **name resolution** on Linux using **`/etc/hosts`**: how static entries override DNS for specific names, and why changing **`localhost`** can break software if you leave it wrong.

## What you do here

- Script **`0-change_your_home_IP`** (run with **`sudo`**) updates **`/etc/hosts`** so that:
  - **`localhost`** resolves to **`127.0.0.2`** instead of **`127.0.0.1`**
  - **`facebook.com`** resolves to **`8.8.8.8`**
- **`ping`** then shows those IPs because the resolver consults **`/etc/hosts`** first.

## Files

| File | Description |
|------|-------------|
| `0-change_your_home_IP` | Bash script that rewrites **`/etc/hosts`** for the two mappings above |

## Safety

On a machine you keep using, **revert** **`localhost`** to **`127.0.0.1`** and remove the **`facebook.com`** override when you are finished experimenting; many tools assume the usual loopback mapping.

