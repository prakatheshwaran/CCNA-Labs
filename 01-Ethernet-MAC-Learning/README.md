# Experiment 1 - Ethernet Frame & MAC Learning

## Objective

To understand Ethernet frame transmission, MAC address learning,
flooding, forwarding, and the operation of a Layer 2 switch.

## Topology

PC0 → Switch0 → PC1

## IP Addressing

| Device | IP Address | Subnet Mask |
|---|---|---|
| PC0 | 192.168.1.10 | 255.255.255.0 |
| PC1 | 192.168.1.20 | 255.255.255.0 |

## Concepts Observed

- Ethernet frames
- Source MAC address
- Destination MAC address
- MAC address learning
- MAC address table
- Flooding
- Forwarding
- Layer 2 switching
- ICMP ping
- Ethernet II frame structure

## Verification

The switch dynamically learned the MAC addresses of PC0 and PC1.

Ping connectivity between PC0 and PC1 was successful.

## Key Learning

A Layer 2 switch learns the source MAC address of an incoming frame
and associates it with the incoming switch port.

If the destination MAC address is unknown, the switch floods the frame
out the appropriate ports. Once the destination MAC is learned, the
switch forwards the frame only through the corresponding port.

## Tool

Cisco Packet Tracer
