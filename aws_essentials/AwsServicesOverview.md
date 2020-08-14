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
    
    

    