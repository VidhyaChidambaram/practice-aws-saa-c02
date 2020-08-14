# EC2 quick notes

## AMI

- amazon machine images
- this is a template that will hold the software, packages and resources that can be used to clone
and create other EC2 instances that will hold the exact same configuration
- Types : community-ami, aws-marketplace-ami (licensed software)

## EC2 Instance Types
- different sizes
- categorized based on family, type, vCPU, memory, storage type, storage optimizations
- large price differences between categories

### IOPS
- Input output operations per second (speed of read and writes)
- Larger the volume, higher is the IOPS

### EBS volume
- Terminate the instance and default terminate EBS on termination is checked
- When unchecked, same EBS volume can be swapped to another EC2 instance

#### Snapshot
- back up of volume or image of volume (replica)
- used to populate another EBS volume from data in the original EBS volume

## When provisioning a EC2 instance
- Root Volume == hard drive in your personal computer (CPU)
- Add an optional additional storage volume (EBS) to store data that can be easily detached
- Add a security group (or existing security group)


