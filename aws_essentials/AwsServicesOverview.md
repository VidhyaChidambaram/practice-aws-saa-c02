# Popular AWS Services
- SNS
- Cloudwatch
- Elastic Load balancer
- Autoscalingg
- Route53
- AWS Lambda

## SNS
- Simple Notification Service
- Usage: If EC2 instance goes down, notify alerts
- Key concepts:
    * Topics - Label and group different endpoints (subscriptions)
    * Subscriptions - Receiving endpoint (i.e, the email address or phone number)
    * Publishers - human / alarm / event that publishes the messages (Eg. ec2 instance)
- Multiple protocols available : SMS, Email, HTTP etc.,

## CloudWatch
- Monitor various elements of your AWS account
- Set thresholds to trigger alarms, which can then invoke SNS for email / sms
   <br/>
   Example thresholds:
    * EC2 instance CPU utilization > 80%
    * Number of objects in a S3 bucket > 100
    * AWS Bill amount increasing $100
- CloudWatch pricing overview:
    * Free tier available
    * Charged for :
        * each dashboard
        * custom metrics
        * CloudWatch API request
        * Detailed monitoring on EC2 instances
        * Cloudwatch logs
        * Cloudwatch custom events

# Elastic Load Balancer
- Regulates load from internet -> app servers
- increases resiliency and fault tolerance across AZ.
- Pricing Overview:
    * No free tier
    * Charged per hour or partial hour of load balancing
    * For each GB of data transferred through the load balancer
- Types : Classic ELB, Application Load balancer
- ELB Security : AWS Security Groups 

# Auto Scaling
- Add or remove servers based on demand
- This is a service provided by AWS, not a part of physical infrastructure, so it can span multiple
AZ and availability zone within VPC.
- Autoscaling configuration:
    
    * Launch configuration - the template used when autoscaling needs to add a server
    to your autoscaling group.
    
    * Auto Scaling Group - the settings and rules that define when a EC2 server is being 
    automatically added or removed. (Eg: Cpu Utilization > 70)
    
- No cost to set up autoscaling, but charged for resources provisioned by autoscaling (additional
servers provisioned in free tier)

# AWS Lambda
- Serverless architecture
- 1 million requests free per month
- Charged based on number of executions and duration of execution for requests
- Option to be included to execute within VPC and access to KMS




    
    

    