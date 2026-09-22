# Two-Subnet Routed Network

## Project overview

This Cisco Packet Tracer project demonstrates communication between two IPv4 subnets connected through a router.

Each subnet contains a switch and multiple PCs. The router has an interface in each subnet and acts as the default gateway, allowing devices on different subnets to communicate.

## Network topology

* Subnet 1: three PCs connected to Switch 1
* Subnet 2: two PCs connected to Switch 2
* One router connecting both switches
* Static IPv4 addressing used on all PCs

## IPv4 addressing

### Subnet 1 — 192.168.1.0/24

| Device | IPv4 address | Subnet mask   | Default gateway |
| ------ | ------------ | ------------- | --------------- |
| PC0    | 192.168.1.10 | 255.255.255.0 | 192.168.1.1     |
| PC1    | 192.168.1.11 | 255.255.255.0 | 192.168.1.1     |
| PC2    | 192.168.1.12 | 255.255.255.0 | 192.168.1.1     |

Router interface: `192.168.1.1`

### Subnet 2 — 192.168.2.0/24

| Device | IPv4 address | Subnet mask   | Default gateway |
| ------ | ------------ | ------------- | --------------- |
| PC3    | 192.168.2.10 | 255.255.255.0 | 192.168.2.1     |
| PC4    | 192.168.2.11 | 255.255.255.0 | 192.168.2.1     |

Router interface: `192.168.2.1`

## How the network works

Devices within the same subnet communicate through their local switch.

When a PC needs to communicate with a device on the other subnet, it recognises that the destination is outside its local network. It sends the data to its default gateway, which is the router interface on its subnet.

The router examines the destination IPv4 address and forwards the packet through its interface connected to the destination subnet.

## Testing

I tested communication between the two subnets by sending a ping from:

* Source: `192.168.1.10`
* Destination: `192.168.2.10`

The ping was successful, confirming that the addressing, default gateways and router interfaces were configured correctly.

## Skills demonstrated

* Building a network in Cisco Packet Tracer
* Connecting PCs, switches and a router
* Configuring static IPv4 addresses
* Using `/24` subnet masks
* Configuring default gateways
* Connecting and routing between two subnets
* Testing connectivity with ICMP ping
* Understanding the different roles of switches and routers

## Project file

Open `two-subnet-routed-network.pkt` using Cisco Packet Tracer to view and test the network.
