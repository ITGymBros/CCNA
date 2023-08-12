Showing the status of each interface

```
Switch#show ip int brief
Interface          IP-Address OK? Method Status   Protocol
Vlan1              unassigned YES unset  up       up
FastEthernet1/0/1  unassigned YES unset  up       up
FastEthernet1/0/2  unassigned YES unset  down     down
FastEthernet1/0/3  unassigned YES unset  down     up
```

If `Status` and `Protocol` say `up` that:
1) The interface is receiving signal
2) The port is receiving data

### Interface Speed Mismatch
```
Switch1#show int g0/0
GigabitEthernet0/0 is down, line protocol is down
...
  Full Duplex, 1Gbps, media type is RJ45
  ...
    0 runts, 0 giants, 0 throttles
    0 input errors, 0 CRC, 0 frame, 0 overrun, 0 ignored
```

```
Switch2#show int fa1/0/1
FastEthernet1/0/1 is down, line protocol is down (not connected)
...
  Full Duplex, 10Mb/s, media type is 10/100BaseTX
  ...
    0 runts, 4 giants, 0 throttles
    4288 input errors, 4284 CRC, 0 frame, 0 overrun, 0 ignored
```

### Interface Duplex Mismatch
```
Switch1#show int g0/1
GigabitEthernet0/0 is up, line protocol is up
...
  Half Duplex, 100Mbps, media type is RJ45
```

```
Switch2#show int fa1/0/1
FastEthernet1/0/1 is up, line protocol is up (connected)
...
  Full-Duplex, 100Mb/s, media type is RJ45
```

### Collisions
```
Switch1#show int g0/1
GigabitEthernet0/0 is up, line protocol is up
...
  Half Duplex, 100Mbps, media type is RJ45
  ...
    0 output errors, 153 collisions, 2 interface resets
```

```
Switch2#show int fa1/0/1
FastEthernet1/0/1 is up, line protocol is up (connected)
...
  Full-Duplex, 100Mb/s, media type is RJ45
  ...
    0 runts, 4 giants, 0 throttles
    4288 input errors, 4284 CRC, 0 frame, 0 overrun, 0 ignored
```