# Useful Packet Sniffing Filters

![image](/img/ghost_in_the_shell.png)

#### Protocol Field Filters:

ICMP Destination/Host Unreachable
```
icmp[0:2] == 0x0301
```

ToS/QoS Filters
- [DSCP Codes](https://www.tucny.com/Home/dscp-tos)
```
tcpdump -ni eth0 ip[1] == 184 #0xB8
```

#### Local Host src & dst Traffic:
- Useful for NICs with multiple IPs or network with rouge DHCP servers
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

#### TCPdump Protocol Qualifiers:
```
- ether (Ethernet)
- wlan (Wireless Lan)
- ip (Internet Protocol v4)
- ip6 (Internet Protocol v6)
- arp (Address Resolution Protocol)
- rarp (Reverse - ARP)
- tcp (Transmission Control Protocol)
- udp (User Datagram Protocol)
- icmp (Internet Control Message Protocol)
```

#### Filters To TSHOOT Slow Internet:
```
tcp.analysis.retransmission #RTO packets
tcp.analysis.fast_retransmission
```

---
Reference:  
<sup>1</sup> [Using tcpdump: Options, Filters and Examples](https://upskilld.com/learn/using-tcpdump-options-filters-and-examples/)
