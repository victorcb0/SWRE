# SWRE (Switching, Routing, and Wireless Essentials)

## Project Description
The SWRE project (Switching, Routing, and Wireless Essentials) implements a complex network using the Cisco Packet Tracer platform, focusing on essential concepts such as switching, routing, and wireless technologies. The project architecture involves using a mix of Cisco networking equipment, including switches, routers and wireless access points, to create a robust and scalable infrastructure. By configuring and managing these devices, the project aims to provide a deep understanding of the basic concepts of computer networks, as well as hands-on experience in their implementation and administration.

![picture alt](https://github.com/victorcb0/SWRE/blob/main/Arhitectura%20re%C8%9Belei.png)

## Project Requirements - Network Administration (Year 3, AC, UPT)
1.	(0.45p) Configure VLANs in the Customer Office (define VLANs on SWs, access ports, trunk ports)
2.	(0.45p) Configure VLANs in the Data Center (define VLANs on SWs, access ports, trunk ports)
3.	(0.45p) Configure IPv4 equipment in the Customer Office VLANs according to the topology and according to the following requirements:
- a. On end-devices of your choice from the VLAN they belong to
- b. On SWs of your choice from the Management VLAN
- c. On each router on subinterfaces one IPv4 address from the VLAN they are part of.
4.	(0.45p)	Configure IPv4 equipment in the VLANs in the Data Center according to the topology and according to the following requirements:
- a. On end-devices of your choice from the VLAN they belong to
- b. On SWs of your choice from the Management VLAN
- c. On each MSW on the VLAN interfaces one IPv4 address from the VLAN they belong to.
5.	(0.45p)	Check the ping from anyone to anyone in the Customer Office.
6.	(0.45p)	Check the ping from anyone to anyone in the Data Center.
7.	(0.45p)	Configure the IPv4 WANs (WAN1, WAN2, Internet cluster) respecting the subnets mentioned in the topology (pay attention to Internet Cluster). 
8.	(0.45p)	In the "Customer Office" site, configure the port-channel using PAGP.
9.	(0.45p)	Set RSTP and HSRP, so as to use the network optimally. Pay attention to the choice of the Primary and Secondary Root Bridge per VLAN to be correlated with HSRP to have load-balancing. (eg: If SW4 is the Root Bridge for VLANa, then R4 will be HSRP Active for VLANa)
10.	(0.45p)	In the "DataCenter" site, configure the port-channel using LACP.
11.	(0.45p)	Set RSTP and HSRP, so as to use the network optimally. Pay attention to the choice of the Primary and Secondary Root Bridge per VLAN to be correlated with HSRP to have load-balancing. (eg: If CoreSW1 is the Root Bridge for VLANb, then CoreSW1 will be HSRP Active for VLANb)
12.	(0.45p)	Check the ping from anyone to anyone in the Customer Office. Attention: DGW on the equipment will be the IPv4 address of the virtual router.
13.	(0.45p)	Check the ping from anyone to anyone in the Data Center. Attention: DGW on the equipment will be the IPv4 address of the virtual router.
14.	(0.45p)	Configure RIPv2 for the routers in the "Internet" (ISP1 + Cluster + ISP2). Make sure that RIPv2 updates are not sent to "Customer Office" and "Data Center".
15.	(0.45p)	Configure default static routes to the ISP in IPv4 as follows:
- a. R4 and R5, default route to ISP1
- b. Core_SW1 and Core_SW2, default route to ISP2
16.	(0.45p)	Configure HSRP in IPv4 on the side of WAN1 and WAN2 as follows:
- a.	R4 and R5 will share a virtual IP from the 10.10.10.0/24 subnet
- b.	Core_SW1 and Core_SW2 will share a virtual IP from the 20.20.20.0/24 subnet
17.	(0.45p)	Configure static routes from ISPs to VLANs as follows: 
- a.	On ISP1: to subnets 192.x.10.0/24, 192.x.20.0/24, 192.x.30.0/24, 192.x.40.0/24, 192.x.99.0/24 will be used as next hop virtual IP configured at point 16a
- b.	On ISP2: to subnets 172.z.10.0/24, 172.z.20.0/24, 172.z.30.0/24, 172.z.40.0/24, 172.z.98.0/24 will be used as next hop virtual IP configured at point 16b
18.	(0.45p)	Configure SSH on SW2 and Core_Switch1 for remote access and test functional SSH from PC1 on the two devices (UN: admin, PW: savnet). Example command stack for SSH:
```
SW2(config)# ip domain-name cisco.com
SW2(config)# Username admin1 secret uptac
SW2(config)# Line vty 0 15
SW2(config)# Transport input ssh
SW2(config)# Login local
SW2(config)# Exit
SW2(config)# Crypto key generate rsa // se pune 1024
```
19.	(0.45p)	Configure Telnet on the SWs in the Customer Office for remote access and test functional Telnet from PC1 on the equipment with Telnet configured (PW chosen by choice)
20.	(0.45p)	Save the config from the Customer Office on the TFTP server.
