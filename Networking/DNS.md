# Domain Name System

In tele-communications or Computer Networking, DNS is used to perform resolution of domain names to its corresponding IP addresses or vice-versa.

DNS uses TCP or UDP for communications. Mostly, UDP is used but for zone transfers and if the message increases 512 bytes, TCP is used.

## DNS Follows hierarchical name space 

 Domain Name Space - The Domain name space is an inverted-tree structure with the root at the top

An example of domain would like www.domain.com. (A domain is a sequence of labels separated by dots (.)). A more formal definition of the domain name is a  sub-tree of the domain name space.

- The last . is the root domain (the root node of the tree). The root label is a null string (empty string)
- The next is the top level domain (TLD) called com; this can be com, net, org, us, in, etc etc.
- The next is the second level domain (SLD) called domain, or google, or amazon or any of the domains in the world.
- The next is the third level domain called www, which is a sub-domain to the domain. Examples: maps.google.com, shop.amazon.com, etc - you get the idea.
- The domain tree (domain name space) can have upto 127 levels in the tree (total excluding root domain level 0). 128 levels including root (level 0)

## FQDN - Fully Qualified Domain Name - any domain name (or label) that terminates with the root domain is a fully qualified domain name. Examples: google.com. or com. 

## PQDN - Partially Qualified Domain Name - any domain that doesn't have the root domain is a PQDN. Examples: Google or Shop.Amazon


## Zone - Since the complete domain name hierarchy cannot be stored on a single server, it is divided among many servers. What a server is responsible or has authority over is called a zone. We can define zone as a contiguous part of a domain tree. The server makes a zone file (which is a db that keeps all the information for every node under that domain). The info about the nodes in the sub-domains is stored on the servers at the lower level servers.

#Root-Server - tbd
#Primary and Secondary DNS Server - tbd
# Registrar
# Resolution
  #Resolver
  #recursive vs Iterative resolution
  # Caching
 
# DNS Messages
  #Format
  # Types of records
  # Query/Response
  
 # DNS Attacks - DNS Exfiltration and DNS Tunneling
 
 ## Foiling DNS
 
 Here is how the Foiling DNS attack works:

 `Step 1:` The victim uses a program/browser that resolves the domain name of a website (randombank.com) to an IP address. 
 `Step 2:` When the DNS request is being made, the attacker uses an MiTM program to sniff the DNS requests and sends a DNS response (to see the DNS requests the attacker may have to use ARP Cache poisoning technique)
 `Step 3:` The victim now surfs wherever the attacks wants them to.
 
 Note: Later a response from the real DNS server will come back but the victim will have already cached the earlier fake response. The real response is ignored because it comes too late. 
 
 The attacker doesn't have to be on the same LAN as the victim for this attack to work, they just need to be sitting between the victim and the DNS server.
 
# Prevention or Remediation

At the `Client` side this can be prevented (not completely) by using better practices like:

- Using VPN so that the end to end communication can be encrypted.
- Using Spoof detection tools 
- Regularly flushing DNS cache to make sure there are no malicious entries that are stored in there.
 

At the `Server` side this can be prevented by using DNSSEC which using public-key cryptography to encrypt the communication. However, its a new protocol and configuration errors can lead to eroded security. Additionally, DNSSEC uses more records and is therefore vulnerable to zone enumeration attack, which uses one record to walk through and collect all DNS records from a particular zone.
 
 
 
 DNSCat2 tool for DNS exfiltration
 DNS exfiltration technique - https://hinty.io/devforth/dns-exfiltration-of-data-step-by-step-simple-guide/
 
 
 # DNS Security
 
 Example of how DNS works when website.com is typed in a browser, what system files are checked.
 
 MacOS - DNS files and location
  # Difference between resolv.conf and /etc/hosts
  # flush DNS - `sudo killall -HUP mDNSResponder`

 WinOS - DNS files
  # flush DNS - cmd - `ipconfig /flushdns`

