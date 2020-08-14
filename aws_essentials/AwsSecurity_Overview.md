# AWS Security Overview

## Security Groups
- similar to Firewall at instance level (inbound and outbound)
- How it differs from NACL?
    * NACL operates at subnet level
    * Security Groups operate at instance level
    * Allow or Deny rules differ from NACL 
    * By default, if an ALLOW rule is not added, traffic is denied.
    
## IP Addressing
- Allocate a public IP Address for the EC2 instance
- Like a street address used to find a home (Where is the instance right now?)
- Needed if the EC2 instance needs to communicate with IGW
- By default private IP address is allocated, add public IP manually if internet access is required

## Data flow from Internt to EC2 Instance

Internet <br/>
&downarrow; <br/>
IGW (attached to VPC) <br/>
&downarrow; <br/>
Route table (attached to IGW) <br/>
&downarrow; <br/> 
NACL (with allow rule) <br/>
&downarrow; <br/>
Security Groups (with allow rule) <br/>
&downarrow; <br/>
IP Addressing (with public ip address) <br/>
&downarrow; <br/>
EC2(the actual instance where app is deployed)





