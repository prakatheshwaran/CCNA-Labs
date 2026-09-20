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

## Screenshots

### 1. Network Topology

![Network Topology](Screenshots/01-topology.png)

### 2. MAC Address Table

![MAC Address Table](Screenshots/02-mac-address-table.png)

### 3. PDU Analysis

![PDU Analysis](Screenshots/03-pdu-analysis.png)

### 4. Ping Verification

![Ping Verification](Screenshots/04-ping-verification.png)

### 5. Inbound PDU

![Inbound PDU](Screenshots/05-inbound-pdu.png)

### 6. Outbound PDU

![Outbound PDU](Screenshots/06-outbound-pdu.png)

### 7. MAC Simulation

![MAC Simulation](Screenshots/07-mac-simulation.png)


### Simulation Recording

[▶️ View Simulation Recording](./Lab-Simulation/mac-simulation.mp4)

## Simulation Observations

| Step | Observation |
|---|---|
| 1 | PC generates an ICMP Echo Request |
| 2 | Ethernet frame is created with source and destination MAC addresses |
| 3 | Switch learns the source MAC address |
| 4 | Unknown destination MAC causes flooding |
| 5 | Destination device receives the frame |
| 6 | Reply frame is forwarded using the learned MAC address |
