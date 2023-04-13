// Access-Switch Configuration

system-view 

vlan10
quit
vlan20
quit

interface e0/0/1
port link-type access
port default vlan 10

interface e0/0/2
port link-type access
port default vlan 20

interface e0/0/3
port link-type trunk
port trunk allow-pass vlan all

// Core-Switch Configuration

system-view 

vlan10
quit
vlan20
quit

interface g0/0/1
port link-type trunk
port trunk allow-pass vlan all

interface Vlanif 10
ip address 192.168.1.1 255.255.255.0

interface Vlanif 20
ip address 192.168.2.1 255.255.255.0

