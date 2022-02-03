# Cisco

---

## Vlan

```bash
$ configure terminal
$ vlan <vlan_number>
$ name <vlan_name>
```

## Trunk

```bash
$ configure terminal
$ interface <intarface_name>
$ switchport trunk encapsulation dot1q
$ switchport mode trunk
```

### VTP

```bash
$ vtp domain <domain_name>
$ vtp version 2
```

### SVI

```bash
$ configure terminal
$ interface <vlan_number>
$ ip address <ip> <mask>
$ no shutdown
```
