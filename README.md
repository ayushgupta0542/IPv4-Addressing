# IPv4-Addressing
An IPv4 (Internet Protocol version 4) address is a 32-bit number label assigned to each device connected to a computer network that uses the Internet Protocol for communication.

Key Characteristics : 32-Bit Structure : An IPv4 address is made up of 32 bits (4 bytes) separated by periods into 4 octets (8 bits each).

# Network Topology

The packet tracer lab is consist of a central router (R1) which connects three different local area networks to three different switches with three different classes of IPv4 addresses:

Class A Network: 15.0.0.0/8 connected via interface GigabitEthernet0/0 to SW1 and PC1.

Class B Network: 182.98.0.0/16 connected via interface GigabitEthernet0/1 to SW2 and PC2.

Class C Network: 201.191.20.0/24 connected via interface GigabitEthernet0/2 to SW3 and PC3.


![alt image](https://github.com/ayushgupta0542/IPv4-Addressing/blob/d595b68fe2e5b19a963d7269218daebaeec2ee0a/Network%20Topology.png)

# Physical Network Layout
![alt image](https://github.com/ayushgupta0542/IPv4-Addressing/blob/a13b636fe13dfba8d0703ce0703de2af8332eb21/Physical%20Network%20Layout.png)

# Router Interface Configuration
The router has three gigabit Ethernet interfaces.

Each is the default gateway for a different LAN.

All interfaces are up/up which means that the physical and data link layers are up and running.

| Interface          | IP Address     | Subnet Mask         | Connected Network |
| ------------------ | -------------- | ------------------- | ----------------- |
| GigabitEthernet0/0 | 15.255.255.254 | 255.0.0.0 (/8)      | 15.0.0.0/8        |
| GigabitEthernet0/1 | 182.98.255.254 | 255.255.0.0 (/16)   | 182.98.0.0/16     |
| GigabitEthernet0/2 | 201.191.20.254 | 255.255.255.0 (/24) | 201.191.20.0/24   |

The show ip interface brief command confirms that all configured interfaces are operational.
```plaintext
Command : R1#show ip interface brief
```

| Interface          | IP Address     | OK? | Method | Status | Protocol |
| ------------------ | -------------- | --- | ------ | ------ | -------- |
| GigabitEthernet0/0 | 15.255.255.254 | YES | manual | up     | up       |
| GigabitEthernet0/1 | 182.98.255.254 | YES | manual | up     | up       |
| GigabitEthernet0/2 | 201.191.20.254 | YES | manual | up     | up       |


Purpose:

Provide Layer 3 connectivity between the three networks.
Serve as the default gateway for hosts in each subnet.
Enable inter-network communication through routing.

**Running Configuration**
```plaintext
Command : R1#show running-config
```
![alt image](https://github.com/ayushgupta0542/IPv4-Addressing/blob/0494d402dc0724567a9d1923468f7dbe5c40acc2/Running%20Configuration.png)



