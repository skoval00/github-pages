Title: Linux networking
Date: 2016-11-30 11:26

Q: Enable IPv6 routing

    ip -6 route add {network}/{netmask} dev {interface}
    sysctl net.ipv6.conf.default.forwarding=1
    sysctl net.ipv6.conf.all.forwarding=1

Q: List network interfaces information

    ip addr show
    ip -6 addr show dev lo

Q: Show routing table
    
    ip route show
    ip -6 route show
