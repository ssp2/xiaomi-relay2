# xiaomi-relay2
Control script for 2 channel  aqara relay. This script improves miiocli functioning.

Prerequisite:
- Library python-miio https://github.com/rytilahti/python-miio/ is installed and functions well
- You have aqara relay (LLKZMK11LM, lumi.relay.c2acn01), which is controlled by xiaomi gateway 2 (DGNWG02LM, lumi.gateway.v3), with opened development mode

Istallation:
- put relay2 to /usr/local/bin
- chmod 755 relay2

Usage:

relay2 ip token sid channel cmd
 
- 4 parameters (order is important) to get status of a channel
- 5 (+ cmd) parameters for channging a channel status
- (1) ip - local ip of gateway (find in your router)
- (2) token - gateway token (google, how to find)
- (3) sid - id of subdevice (relay), get it from 
    miiocli gateway --ip 192.168.1.xx --token tokentoken discover_devices
- (4) channel - channel of relay can be 0 or 1
- (5) cmd - command to change relay status (on, off, toggle)
