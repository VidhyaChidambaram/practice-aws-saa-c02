# VPC quick notes

- Your own private cloud
- One VPC can have more than one Availability zone
- One VPC is attached to ONE IGW

# IGW
- Like your modem
- Connection point to internet

## What is VPC
- your-own-private-cloud within AWS
- entry point from internet
- default VPC created when you create an AWS account
- Each VPC is linked to an internet gateway (IGW)

- Public subnet is attached to Route table and IGW
- private subnet is attached to Route table but the specific RT is not attached to IGW

## Subnet
- Home network 
- By default in a AWS account 4 subnets are created

## Routing table
- Provides entry for subnet and helps route traffic to the IGW
- Optionally attached to a IGW
- If the routing table is attached to IGW, then the underlying subnet becomes public subnet
- If the routing table is not attached to IGW, then the underlying subnet is a private subnet

## How can two subnets talk to each other in different AZ?
- Create subnet association in the routing table
- Even if the routing table attached to the other subnet does not have internet access, it is still
possible for both subnets to talk to each other.
- A private subnet can talk to a public subnet via routing table.

