# SWRE (Switching, Routing, and Wireless Essentials)

Cerinte proiect AR (an 3, AC, UPT)

1.	(0.45p)	Faceti configuratia de VLAN in Customer Office (definiti VLAN-urile pe SW-uri, porturi de tip acces, porturi de tip trunk)
2.	(0.45p)	Faceti configuratia de VLAN in Data Center (definiti VLAN-urile pe SW-uri, porturi de tip acces, porturi de tip trunk)
3.	(0.45p)	Configurati IPv4 echipamentele din VLAN-urile din Customer Office conform topologiei si dupa urmatoarele cerinte: 
a.	Pe end-devices la alegere din VLAN-ul din care fac parte
b.	Pe SW-uri la alegere din VLAN-ul de Management
c.	Pe fiecare router pe subinterfete cate o adresa IPv4 din VLAN-ul din care fac parte). 
4.	(0.45p)	Configurati IPv4 echipamentele din VLAN-urile din Data Center conform topologiei si dupa urmatoarele cerinte: 
a.	Pe end-devices la alegere din VLAN-ul din care fac parte
b.	Pe SW-uri la alegere din VLAN-ul de Management
c.	Pe fiecare MSW pe interfetele de VLAN cate o adresa IPv4 din VLAN-ul din care fac parte). 
5.	(0.45p)	Verificati ping de la oricine la oricine in Customer Office. 
6.	(0.45p)	Verificati ping de la oricine la oricine in Data Center. 
7.	(0.45p)	Configurati IPv4 WAN-urile (WAN1, WAN2, cluster Internet) respectand subnet-urile mentionate in topologie (atentie la Cluster Internet). 
8.	(0.45p)	In site "Customer Office" configurati port-channel folosind PAGP. 
9.	(0.45p)	Setati RSTP si HSRP-ul, astfel incat sa folositi optim reteaua. Atentie la alegerea Root Bridge-ului Primary si Secondary per VLAN sa fie corelat cu HSRP pentru a avea load-balancing. (ex: Daca SW4 este Root Bridge pentru VLANa, atunci R4 va fi HSRP Active pentru VLANa)
10.	(0.45p)	In site "DataCenter" configurati port-channel folosind LACP. 
11.	(0.45p)	Setati RSTP si HSRP-ul, astfel incat sa folositi optim reteaua. Atentie la alegerea Root Bridge-ului Primary si Secondary per VLAN sa fie corelat cu HSRP pentru a avea load-balancing. (ex: Daca CoreSW1 este Root Bridge pentru VLANb, atunci CoreSW1 va fi HSRP Active pentru VLANb)
12.	(0.45p)	Verificati ping de la oricine la oricine in Customer Office. Atentie: DGW pe echipamente va fi adresa IPv4 a routerului virtual.
13.	(0.45p)	Verificati ping de la oricine la oricine in Data Center. Atentie: DGW pe echipamente va fi adresa IPv4 a routerului virtual.
14.	(0.45p)	Configurati RIPv2 pentru routerele din "Internet" (ISP1 + Cluster + ISP2). Asigurati-va ca update-urile de RIPv2 nu se trimit in “Customer Office” si “Data Center”. 
15.	(0.45p)	Configurati rute statice default catre ISP in IPv4 astfel: 
a. R4 si R5, ruta default catre ISP1 
b. Core_SW1 si Core_SW2, ruta default catre ISP2 
16.	(0.45p)	Configurati HSRP in IPv4 in partea de WAN1 si WAN2 astfel: 
a.	R4 si R5 vor imparti un IP virtual din subnet 10.10.10.0/24 
b.	b. Core_SW1 si Core_SW2 vor imparti un IP virtual din subnet 20.20.20.0/24 
17.	(0.45p)	Configurati rute statice de la ISP-uri catre VLAN-uri astfel: 
a.	Pe ISP1: catre subnet-urile 192.x.10.0/24, 192.x.20.0/24 , 192.x.30.0/24 , 192.x.40.0/24 , 192.x.99.0/24  se va folosi ca next hop IP virtual configurat la pct 16a
b.	Pe ISP2: catre subnet-urile 172.z.10.0/24, 172.z.20.0/24, 172.z.30.0/24, 172.z.40.0/24, 172.z.98.0/24 se va folosi ca next hop IP virtual configurat la pct 16b

18.	(0.45p)	Configurati SSH pe SW2 si Core_Switch1 pentru access remote si testati SSH functional de la  PC1 pe cele doua echipamente (UN: admin, PW: savnet)
Exemplu de stiva de comenzi pentru SSH: 
SW2(config)# ip domain-name cisco.com
SW2(config)# Username admin1 secret uptac
SW2(config)# Line vty 0 15
SW2(config)# Transport input ssh
SW2(config)# Login local
SW2(config)# Exit
SW2(config)# Crypto key generate rsa // se pune 1024
19.	(0.45p)	Configurati Telnet pe SW-urile din Customer Office  pentru access remote si testati Telnet functional de la  PC1 pe echipamentele cu Telnet configurat  (PW ales la alegere)
20.	(0.45p)	Salvati config din Customer Office pe serverul de TFTP.