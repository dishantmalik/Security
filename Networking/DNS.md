# Domain Name System

In tele-communications or Computer Networking, DNS is used to perform resolution of domain names to its corresponding IP addresses or vice-versa.

## DNS Follows hierarchical name space 

 Domain Name Space - The Domain name space is an inverted-tree structure with the root at the top

An example of domain would like www.domain.com. (A domain is a sequence of labels separated by dots (.)). A more formal definition of the domain name is a  sub-tree of the domain name space.

The last . is the root domain (the root node of the tree). The root label is a null string (empty string)
The next is the top level domain (TLD) called com; this can be com, net, org, us, in, etc etc.
The next is the second level domain (SLD) called domain, or google, or amazon or any of the domains in the world.
The next is the third level domain called www, which is a sub-domain to the domain. Examples: maps.google.com, shop.amazon.com, etc - you get the idea.
The domain tree (domain name space) can have upto 127 levels in the tree (total excluding root domain level 0). 128 levels including root (level 0)

## FQDN - Fully Qualified Domain Name - any domain name (or label) that terminates with the root domain is a fully qualified domain name. Examples: google.com. or com. 

## PQDN - Partially Qualified Domain Name - any domain that doesn't have the root domain is a PQDN. Examples: Google or Shop.Amazon


## Zone - Since the complete domain name hierarchy cannot be stored on a single server, it is divided among many servers. What a server is responsible or has authority over is called a zone. We can define zone as a contiguous part of a domain tree. The server makes a zone file (which is a db that keeps all the information for every node under that domain. The info about the nodes in the sub-domains is stored in the servers at the lower level servers.

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
 # DNS Security
 
 Example of how DNS works when website.com is typed in a browser, what system files are checked.
 
 MacOS - DNS files and location
  # Difference between resolv.conf and /etc/hosts
  # flush DNS - `sudo killall -HUP mDNSResponder`

 WinOS - DNS files
  # flush DNS - cmd - `ipconfig /flushdns`

