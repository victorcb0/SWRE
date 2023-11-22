# SWRE (Switching, Routing, and Wireless Essentials)

## Cerințe proiect AR (an 3, AC, UPT):

1.	(0.45p)	Faceți configurația de VLAN în Customer Office (definiți VLAN-urile pe SW-uri, porturi de tip acces, porturi de tip trunk)
2.	(0.45p)	Faceți configurația de VLAN în Data Center (definiți VLAN-urile pe SW-uri, porturi de tip acces, porturi de tip trunk)
3.	(0.45p)	Configurați IPv4 echipamentele din VLAN-urile din Customer Office conform topologiei și după următoarele cerințe:
a.	Pe end-devices la alegere din VLAN-ul din care fac parte
b.	Pe SW-uri la alegere din VLAN-ul de Management
  * c.	Pe fiecare router pe subinterfețe câte o adresa IPv4 din VLAN-ul din care fac parte).
4.	(0.45p)	Configurați IPv4 echipamentele din VLAN-urile din Data Center conform topologiei și după urmatoarele cerințe: 
  a.	Pe end-devices la alegere din VLAN-ul din care fac parte
  b.	Pe SW-uri la alegere din VLAN-ul de Management
  c.	Pe fiecare MSW pe interfețele de VLAN câte o adresă IPv4 din VLAN-ul din care fac parte). 
5.	(0.45p)	Verificați ping de la oricine la oricine în Customer Office. 
6.	(0.45p)	Verificați ping de la oricine la oricine în Data Center. 
7.	(0.45p)	Configurați IPv4 WAN-urile (WAN1, WAN2, cluster Internet) respectând subnet-urile menționate în topologie (atenție la Cluster Internet). 
8.	(0.45p)	În site "Customer Office" configurați port-channel folosind PAGP. 
9.	(0.45p)	Setați RSTP și HSRP-ul, astfel încât să folosiți optim rețeaua. Atenție la alegerea Root Bridge-ului Primary și Secondary per VLAN să fie corelat cu HSRP pentru a avea load-balancing. (ex: Daca SW4 este Root Bridge pentru VLANa, atunci R4 va fi HSRP Active pentru VLANa)
10.	(0.45p)	În site "DataCenter" configurați port-channel folosind LACP. 
11.	(0.45p)	Setați RSTP și HSRP-ul, astfel încat să folosiți optim rețeaua. Atenție la alegerea Root Bridge-ului Primary și Secondary per VLAN să fie corelat cu HSRP pentru a avea load-balancing. (ex: Dacă CoreSW1 este Root Bridge pentru VLANb, atunci CoreSW1 va fi HSRP Active pentru VLANb)
12.	(0.45p)	Verificați ping de la oricine la oricine în Customer Office. Atenție: DGW pe echipamente va fi adresa IPv4 a routerului virtual.
13.	(0.45p)	Verificați ping de la oricine la oricine în Data Center. Atenție: DGW pe echipamente va fi adresa IPv4 a routerului virtual.
14.	(0.45p)	Configurați RIPv2 pentru routerele din "Internet" (ISP1 + Cluster + ISP2). Asigurați-vă că update-urile de RIPv2 nu se trimit în “Customer Office” și “Data Center”. 
15.	(0.45p)	Configurați rute statice default către ISP în IPv4 astfel: 
  a.  R4 și R5, ruta default către ISP1 
  b.  Core_SW1 și Core_SW2, ruta default către ISP2 
16.	(0.45p)	Configurați HSRP în IPv4 în partea de WAN1 și WAN2 astfel: 
  a.	R4 și R5 vor împărți un IP virtual din subnet 10.10.10.0/24 
  b.	b. Core_SW1 și Core_SW2 vor împarți un IP virtual din subnet 20.20.20.0/24 
17.	(0.45p)	Configurați rute statice de la ISP-uri către VLAN-uri astfel: 
  a.	Pe ISP1: către subnet-urile 192.x.10.0/24, 192.x.20.0/24 , 192.x.30.0/24 , 192.x.40.0/24 , 192.x.99.0/24  se va folosi ca next hop IP virtual configurat la pct 16a
  b.	Pe ISP2: către subnet-urile 172.z.10.0/24, 172.z.20.0/24, 172.z.30.0/24, 172.z.40.0/24, 172.z.98.0/24 se va folosi ca next hop IP virtual configurat la pct 16b
18.	(0.45p)	Configurați SSH pe SW2 și Core_Switch1 pentru access remote ți testați SSH funcțional de la  PC1 pe cele doua echipamente (UN: admin, PW: savnet)
  Exemplu de stivă de comenzi pentru SSH: 
  SW2(config)# ip domain-name cisco.com
  SW2(config)# Username admin1 secret uptac
  SW2(config)# Line vty 0 15
  SW2(config)# Transport input ssh
  SW2(config)# Login local
  SW2(config)# Exit
  SW2(config)# Crypto key generate rsa // se pune 1024
19.	(0.45p)	Configurați Telnet pe SW-urile din Customer Office  pentru access remote și testați Telnet funcțional de la PC1 pe echipamentele cu Telnet configurat (PW ales la alegere)
20.	(0.45p)	Salvați config din Customer Office pe serverul de TFTP.
