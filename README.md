# Домашнее задание к занятию 10.1 «Keepalived/vrrp» Умаров Азиз
## 1-Node nano /etc/keepalived/keepalived.conf
```bash
vrrp_instance test {
state MASTER
interface enp0s8
virtual_router_id 10
priority 110
advert_int 4
authentication {
auth_type AH
auth_pass 1111
}
unicast_peer {
192.168.2.2
}
virtual_ipaddress {
192.168.2.250 dev enp0s8 label enp0s8
}
}

vrrp_instance MAST{
state BACKUP
interface enp0s3
virtual_router_id 11
priority 100
advert_int 4
authentication {
auth_type AH
auth_pass 1111
}
unicast_peer {
192.168.31.133
}
virtual_ipaddress {
192.168.31.200 dev enp0s3 label TEST
}
}
```
## 2-Node nano /etc/keepalived/keepalived.conf
```bash
vrrp_instance test {
state BACKUP
interface enp0s8
virtual_router_id 10
priority 100
advert_int 4
authentication {
auth_type AH
auth_pass 1111
}
unicast_peer {
192.168.2.1
}
virtual_ipaddress {
192.168.2.250 dev enp0s8 label enp0s8
}
}
vrrp_instance MAST{
state MASTER
interface enp0s3
virtual_router_id 11
priority 110
advert_int 4
authentication {
auth_type AH
auth_pass 1111
}
unicast_peer {
192.168.31.15
}
virtual_ipaddress {
192.168.31.200 dev enp0s3 label TEST
}
}

```
