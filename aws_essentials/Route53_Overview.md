# Route53 Overview

- Definitions
- DNS Servers
- How webservers are located
- Pricing Overview

## Definition
Configure and manage web domains for websites and applications hosted on AWS
Three main functions: <br/>
- Domain name registration (like GoDaddy, acts as registrar).
- Acts as DNS Server (Translates friendly domain names to IP Addresses). Has a global network of 
authoritative DNS Servers, and this reduces latency.
- Healthchecks - automated requests to your application to verify if it is reachable, available
and functional.

## How websites are located
- Domain name entered by user
- Computer needs IP address to route to server
- DNS Server : Database of domain name and IP addresses, DNS Servers usually run by a third party.

So, when we purchase a domain name, the Domain Registration process helps update our details
(Key = friendly_dns_name, Value = "IP Address") to the various DNS Server providers across the world.

Computer invokes dnsName and routes to internet <br/>
&downarrow; <br/>
Routed to DNS Servers <br/>
&downarrow; <br/>
DNS Servers return the IP address to computer via Internet <br/>
&downarrow; <br/>
Now, computer invokes internet with IP Address <br/>
&downarrow; <br/>
Routed to Route53 <br/>
&downarrow; <br/>
Hits IGW <br/>
&downarrow; <br/>
If ELB is present, routed to one of the available sites <br/>
&downarrow; <br/>
Passed via NACL <br/>
&downarrow; <br/>
Checked at security Group <br/>
&downarrow; <br/>
Routed to Web Server where website is hosted.

## Pricing Overview
- No free tier
- Number of hosted zone
- Standard query
- Traffic flow
- Register or transfer a domain

### Configuring Route 53
- When domain name is purchased via AWS, hosted zones and record sets are created automatically.
- Create 2 A records or A record sets for your domain that route to ELB
    * one record for the domain name with www.
    * One record for the domain name without www.
- Add routing policy (simple routing policy)
- Optionally select Evaluate Health








