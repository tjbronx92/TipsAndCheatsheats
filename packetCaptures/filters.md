# Useful Packet Sniffing Filters

![image](/img/ghost_in_the_shell.png)

### Protocol Field Filters:

ICMP Destination/Host Unreachable
```
icmp[0:2] == 0x0301
```

Local Host src & dst Traffic:
- Useful for NICs with multiple IPs or rouge DHCP servers
```
ether host 00:00:00:00:00:00
```

#### TCP Protocol Filters:
```
tcp[13] & 1 == 1  #TCP FIN flag set

tcp[13] & 2 == 2  #TCP SYN flag set

tcp[13] & 4 == 4  #TCP RST flag set

tcp[13] & 8 == 8  #TCP PSH flag set

tcp[13] & 16 == 16  #TCP ACK flag set

tcp[13] & 32 == 32  #TCP URG flag set

tcp[13] == 18  #TCP SYN-ACK flag set
```