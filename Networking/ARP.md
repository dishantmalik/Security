 # Address Resolution Protocol
 
 A logical address (IP) is an internetwork address. A physical address is a local address. The delivery of a packet to a host or a router requires these two levels of addressing.
 
 IP address is 32 bits and a MAC address is 48 bits. ARP converts an IP to Mac and vice-versa. This can be achieved using either of the 2 mapping techniques:

 1. Static Mapping, and
 2. Dynamic Mapping

Static Mapping means creating a table that associates a logical address with a physical address. Limitations of Static Mapping is that in some LANs, such as LocalTalk, the physical address changes each time a computer is rebooted. Additionally, a mobile computer can move from one physical network to another, resulting a change in its physical address. To implement these changes, a static mapping table needs to be updated periodically -- too much admin overload

To resolve this, we use Dynamic Mapping. 2 protocols:

- ARP
- rARP (reverse ARP)

## ARP is a level 2 (Data Link Layer) protocol. 

Anytime a host, or a router needs to find the physical address of another host or router on its network, it sends an ARP query packet, The router makes a broadcast request to all the hosts on the network to find out who owns the physical address in the message. The host machine on the network containing the requested physical address would reply with its physical address. 

Security was not taken into consideration when ARP was built in the year 1982. As a result, it is prone to attacks like ARP Spoofing or ARP Cache Poisoning (self explanatory), MiTM, DoS and, Session Hijacking


 
 
