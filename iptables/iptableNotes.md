# IPTABLES

![image](/img/roxbury.gif)

DENY all traffic to/from local host:
```
iptables -t filter -A FORWARD -d 0.0.0.0.0/0 -s 0.0.0.0/0 -J DROP
```

Configure DHCP Server:
```
iptables -t nat -A POSTROUTING -s 0.0.0.0/0 -o <WAN_interface or Interface_IP> -J MASQURADE
```