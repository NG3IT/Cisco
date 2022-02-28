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

### ACL

#### Configuration

```bash
# Create named ACL
$ access-list extended <name>
# Examples
$ permit <transport_protocol> host 192.168.1.10 gt 1023 192.168.2.0 0.0.0.255 eq 22
$ deny <transport_protocol> host 192.168.1.10 gt 1023 192.168.2.0 0.0.0.255 eq 443
$ deny ip any any log
```

#### Application

```bash
$ int <interface>
$ ip access-group <name> <in or out>

$ int fa0/1
$ ip access-group <name> int
```

#### Show configuration

```bash
$ show acces-lists <name>
```

#### Delete ACL

```bash
$ no ip access-list extended <name>
$ end
```

#### Delete ACL/Interface association

```bash
$ int <interface>
$ no ip access-group <name> <in or out>
```
