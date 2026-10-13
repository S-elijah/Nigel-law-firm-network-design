**Nigel Law Firm: Network Requirements Analysis & Design**  
Group project for **Data Communication & Networking** at Victoria University Kampala. We modelled the network of a small law firm that handles confidential client case files: 3 floors, a server room, 22 users and 30 end devices.  
**What we designed**  
| | |  
|-|-|  
| **Area** | **Decision** |   
| Topology | Extended star: Router 2811, one Core Switch 2960, four access switches (ground, first, second floor, server farm) |   
| Addressing | 192.168.10.0/24 split into /28 subnets (mask 255.255.255.240), one per VLAN |   
| VLANs | 10 Front Desk, 20 Partners, 30 Associates, 40 Accounts, 50 Managing Partner, 60 IT/Admin/Library + servers |   
| Media | Cat6 straight-through on the LAN, fiber on the ISP link, WPA2-PSK Wi-Fi |   
| Services | NAT gateway, DHCP and DNS, central file server, 3 network printers, VoIP with Call Manager Express |   
| Security | ACL blocking Front Desk from the File Server, router firewall, DHCP Snooping, encrypted file server, isolated reception/guest VLAN |   
   
**Subnets**  
| | | | | |  
|-|-|-|-|-|  
| **VLAN** | **Department** | **Network** | **Gateway** | **Usable range** |   
| 10 | Front Desk | 192.168.10.0/28 | 192.168.10.1 | .2 – .14 |   
| 20 | Partners Chambers | 192.168.10.16/28 | 192.168.10.17 | .18 – .30 |   
| 30 | Associates / Legal | 192.168.10.32/28 | 192.168.10.33 | .34 – .46 |   
| 40 | Accounts & Finance | 192.168.10.48/28 | 192.168.10.49 | .50 – .62 |   
| 50 | Managing Partner | 192.168.10.64/28 | 192.168.10.65 | .66 – .78 |   
| 60 | IT / Admin / Library + Servers | 192.168.10.80/28 | 192.168.10.81 | .82 – .94 |   
   
File Server: 192.168.10.86. DHCP/DNS Server: 192.168.10.87.  
**Repository contents**  
.  
 ├── README.md  
 ├── images/topology.png  
 ├── Nigel-Law-Firm-Network-Report-PUBLIC.docx  
 ├── Nigel-Law-Firm-Network-Design.pptx  
 └── <your-file>.pkt          
   
**Open the simulation**  
1. Install [Cisco Packet Tracer.](https://www.netacad.com/cisco-packet-tracer "https://www.netacad.com/cisco-packet-tracer")  
2. Open the .pkt file from this repository.  
**Team**  
Group 3, Victoria University Kampala. Report author and repository owner: [Elijah Senabulya.](https://github.com/S-elijah "https://github.com/S-elijah")  
