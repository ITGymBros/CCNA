## Reviewing IPv4 Addressing

Dotted decimal notation = 32 bit Binary number

```
192.168.0.1 - IP Address (2 parts - Network ID & Host ID)
255.255.255.0 - Subnet Mask

192.168.0.1/24 - CIDR notation 

-----
IP address:    192      168      0         2
            11000000 10101000 00000000 00000010
Netmask:    11111111 11111111 11111111 00000000
               255      255     255        0
           +--------------------------+--------+
                    Network              Host

```

IPv4 Address Classes
Class A 1.0.0.1 - 127.255.255.254
Default Subnet Mask: 255.0.0.0
Number of Networks: 127
Number of Hosts per Network: 16,777,254
Binary: 00000001

Class B 128.0.0.1 - 191.255.255.254
Default Subnet Mask: 255.255.0.0
Number of Networks: 65, 636 
Number of Hosts per Network: 65, 535 
Binary: 10000000

Class C 192.0.0.1 - 223.255.255.254
Default Subnet Mask: 255.255.255.0
Number of Networks: 16, 777, 216
Number of Hosts per Network: 254
Binary: 11000000

Class D 224.0.0.1 - 255.255.255.254
Default Subnet Mask: N/A
Binary: 11100000

Class E Experimental
Default Subnet Mask: N/A

## References
[^1]: Understanding network terminology [[https://wiki.gentoo.org/wiki/Handbook:AMD64/Installation/Networking#Understanding_network_terminology]]
