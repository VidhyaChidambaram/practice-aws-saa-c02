## Serverless architecutre on AWS

N-tier architecture components - network, database, MVC application, REST endpoints, application/web servers

- Utilize VPC, EC2, RDS/DynamoDB, S3, API Gateway, AWS Lambda and Route 53 to create equivalent N-Tier architure
- For serverless apps,the architecture is hence translated as :

<ol>
<li> DynamoDB for data </li>
<li> AWS Lambda to act as DAO </li>
<li> API Gateway to act as integration layer exposing the endpoints for invoking the lambda </li>
<li> S3 acts as the presentation layer, and also doubles up as static webstite hosting and providing object storage </li>
<li> Secure the architecture using VPC by restricting access to the provisioned infrastructure along with WAF and SSL </li>
<li> Route 53 can be used to provision a DNS for the app </li>
</li>


