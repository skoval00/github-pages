Title: Linux networking
Date: 2016-11-30 11:26

Q: How to enable IPv6 routing?

    ip -6 route add {network}/{netmask} dev {interface}
    sysctl net.ipv6.conf.default.forwarding=1
    sysctl net.ipv6.conf.all.forwarding=1
