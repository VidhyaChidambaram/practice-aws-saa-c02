# RDS Overview

Different types of RDS engine supported by AWS, underlying data source can be commercial.

- Aurora
- PostGreSQL
- Oracle

## DB Subnet Group
- option provided to create a group of minimum 2 subnets
- added as a group

## Provisioning an RDS instance
- Choose the right option for instance size and any db engine of choice
- Create Security group (or link to an existing one)
- Do not forget to update the security group to allow TCP on 3306 port (for mysql)
- Set up Key pair, database name and password

## Accessing RDS instance
- SSH tunneling : Practice of using SSH to access a resource without public IP address via 
a resource with a public IP address (inside a VPC)

