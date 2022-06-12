# AWS-Certified-Developer-Associate
This exam validates an examinee’s ability to effectively demonstrate knowledge of how to architect and deploy secure and robust applications on AWS technologies.

1. Which of the following cannot be retained when deleting an AWS Elastic Beanstalk 
environment?

A. Source code from the Git repository

B. Data from the automatic backups of an Amazon Relational Database Service (Amazon RDS) instance

C. Packaged code from the source bundle stored in an Amazon Simple Storage Service (Amazon S3) bucket

D. Data from the snapshot of an Amazon RDS instance

Anwser: D. Elastic Beanstalk cannot make automated changes to the policies attached to the service roles and instance roles.

2. You have an application running on Amazon Elastic Compute Cloud (Amazon EC2) that 
needs read-only access to several AWS services. What is the best way to grant that application permissions only to a specific set of resources within your account?

A. Use API credentials derived based on the AWS account.

B. Launch the EC2 instance into an AWS Identity and Access Management (IAM) role 
and attach the ReadOnlyAccess IAM-managed policy.

C. Declare the necessary permissions as statements in the AWS SDK configuration file on 
the EC2 instance.

D. Launch the EC2 instance into an IAM role with custom IAM policies for the permissions.

Anwser: D. Use the custom IAM policy to configure the permissions to a specific set of resources in 
your account. The ReadOnlyAccess IAM policy restricts write access but grants access to 
all resources within your account. AWS account credentials are unrestricted. Policies do not 
go in an SDK configuration file. They are enforced by AWS on the backend.

3. You have deployed a new application in the US West (Oregon) Region. However, you have 
accidentally deployed an Amazon Polly lexicon needed for your application in EU (London). 
How can you use your lexicon to synthesize speech while minimizing the changes to your 
application code and reducing cost?

A. Point your SDK client to the EU (London) for all requests to Amazon Polly, but to US 
West (Oregon) for all other API calls.

B. No action needed; the data is automatically available from all Regions.

C. Upload a copy of the lexicon to US West (Oregon).

D. Move the rest of the application resources to EU (London).

Anwser:C. This is the simplest approach because only a single resource is in the wrong Region. 
Option A is a possible approach, but it is not the simplest approach because it introduces 
cross-region calls that may increase latency and cross-region data transfer pricing.

4. When you’re placing subnets for a specific Amazon Virtual Private Cloud (Amazon VPC), 
you can place the subnets in which of the following?

A. In any Availability Zone within the Region for the Amazon VPC

B. In any Availability Zone in any Region

C. In any AWS edge location

D. In any specific AWS data center

Anwser: A. Each Amazon VPC is placed in a specific Region and can span all the Availability Zones 
within that Region. Option B is incorrect because a subnet must be placed within the 
Region for the selected VPC. Option C is incorrect because edge locations are not available 
for subnets, and option D is incorrect because you cannot choose specific data centers.

4. You have identified two Amazon Elastic Compute Cloud (Amazon EC2) instances in your 
account that appear to have the same private IP address. What could be the cause?

A. These instances are in different Amazon Virtual Private Cloud (Amazon VPCs).

B. The instances are in different subnets.

C. The instances have different network ACLs.

D. The instances have different security groups.

Anwser: A. Even though each instance in an Amazon VPC has a unique private IP address, you 
could assign the same private IP address ranges to multiple Amazon VPCs. Therefore, two 
instances in two different Amazon VPCs in your account could end up with the same private IP address. Options B, C, and D are incorrect because within the same Amazon VPC, 
there is no duplication of private IP addresses.

5. You have a workload that requires 15,000 consistent IOPS for data that must be durable. 
What combination of the following do you need? (Select TWO.)

A. Use an Amazon Elastic Block Store (Amazon EBS) optimized instance.

B. Use an instance store.

C. Use a Provisioned IOPS SSD volume.

D. Use a previous-generation EBS volume

Anwser:A, C. Amazon EBS optimized instances reserve network bandwidth on the instance for 
I/O, and Provisioned IOPS SSD volumes provide the highest consistent IOPS. Option B is 
incorrect because instance store is not durable. Option D is incorrect because a previousgeneration EBS volume offers an average of 100 IOPS.

6. Your company stores critical documents in Amazon Simple Storage Service (Amazon S3), 
but it wants to minimize cost. Most documents are used actively for only about one month 
and then used much less frequently after that. However, all data needs to be available 
within minutes when requested. How can you meet these requirements?

A. Migrate the data to Amazon S3 Reduced Redundancy Storage (RRS) after 30 days.

B. Migrate the data to Amazon S3 Glacier after 30 days.

C. Migrate the data to Amazon S3 Standard – Infrequent Access (IA) after 30 days.

D. Turn on versioning and then migrate the older version to Amazon S3 Glacier.

Anwser:C. Migrating the data to Amazon S3 Standard-IA after 30 days using a lifecycle policy is 
correct. The lifecycle policy will automatically change the storage class for objects aged 
over 30 days. The Standard-IA storage class is for data that is accessed less frequently, but 
still requires rapid access when needed. It offers the same high durability, high throughput, and low latency of Standard, with a lower per gigabyte storage price and per gigabyte 
retrieval fee. Option A is incorrect because RRS provides a lower level of redundancy. The 
question did not state that the customer is willing to reduce the redundancy level of the 
data, and RRS does not replicate objects as many times as standard Amazon S3 storage. 
This storage option enables customers to store noncritical, reproducible data. Option B is 
incorrect because the fastest retrieval option for Amazon S3 Glacier is typically 3–5 hours. 
The customer requires retrieval in minutes. Option D is incorrect. Versioning will increase 
the number of files if new versions of files are being uploaded, which will increase cost. The 
question did not mention a need for multiple versions of files.

7. You are migrating your company’s applications and data from on-premises to the AWS 
Cloud. You have performed a data inventory and discovered that you will need to transfer 
about 2 PB of data to AWS. Which migration option will be the best choice for your company with minimal cost and shortest time?

A. AWS Snowball

B. AWS Snowmobile

C. Upload files directly to AWS over the internet using Amazon Simple Storage Service 
(Amazon S3) Transfer Acceleration.

D. Amazon Kinesis Data Firehose

Anwser:A. Option B is incorrect. You could use Snowmobile, but that would not be as cost effective 
because it is meant to be used for datasets of 10 PB or more. Option C is incorrect because 
uploading files directly over the internet to Amazon S3, even using Amazon S3 Transfer 
Accelerator, would take many months and would be using your on-premises bandwidth. 
Option D is incorrect because Amazon Kinesis Data Firehose would still be transferring 
over the internet and take months to complete while using your on-premises bandwidth.

8. You are changing your application to take advantage of the elasticity and cost benefits provided by AWS Auto Scaling. To do this, you must move session state information from the 
individual Amazon Elastic Compute Cloud (Amazon EC2) instances. Which of the following AWS Cloud services is best suited as an alternative for storing session state information?

A. Amazon DynamoDB

B. Amazon Redshift

C. AWS Storage Gateway

D. Amazon Kinesis

Anwser:A. DynamoDB is a NoSQL database store that is a good alternative because of its scalability, high availability, and durability characteristics. Many platforms provide open 
source, drop-in replacement libraries that enable you to store native sessions in DynamoDB. 
DynamoDB is a suitable candidate for a session storage solution in a share-nothing, 
distributed architecture

9. Your company’s senior management wants to query several data stores to obtain a “big picture” view of the business. The amount of data contained within the data stores is at least 
2 TB in size. Which of the following is the best AWS service to deliver results to senior 
management?

A. Amazon Elastic Block Store (Amazon EBS)

B. Amazon Simple Storage Service (Amazon S3)

C. Amazon Relational Database Service (Amazon RDS)

D. Amazon Redshift

Anwser:D. Amazon Redshift is the best choice for data warehouse workloads that typically span 
multiple data repositories and are at least 2 TB in size.

10. Your ecommerce application provides daily and ad hoc reporting to various business 
units on customer purchases. These operations result in a high level of read traffic to your 
MySQL Amazon Relational Database Service (Amazon RDS) instance. What can you do to 
scale up read traffic without impacting your database’s performance?

A. Increase the allocated storage for the Amazon RDS instance.

B. Modify the Amazon RDS instance to be a Multi-AZ deployment.

C. Create a read replica for an Amazon RDS instance.

D. Change the Amazon RDS instance DB engine version.

Anwser:C. Amazon RDS read replicas provide enhanced performance and durability for Amazon 
RDS instances. This replication feature makes it easy to scale out elastically beyond the 
capacity constraints of a single Amazon RDS instance for read-heavy database workloads. 
You can create one or more replicas of a given source Amazon RDS instance and serve 
high-volume application read traffic from multiple copies of your data, increasing aggregate 
read throughput.

11. Your company has refactored their application to use NoSQL instead of SQL. They would 
like to use a managed service for running the new NoSQL database. Which AWS service 
should you recommend?

A. Amazon Relational Database Service (Amazon RDS)

B. Amazon Elastic Compute Cloud (Amazon EC2)

C. Amazon DynamoDB

D. Amazon Redshift

Anwser:C. DynamoDB is the best option. The question states a managed service, so this eliminates 
the Amazon EC2 service. Additionally, Amazon RDS and Amazon Redshift are SQL database products. The company is looking for a NoSQL product. DynamoDB is a managed 
NoSQL service.

12. A company is currently using Amazon Relational Database Service (Amazon RDS); 
however, they are retiring a database that is currently running. They have automatic backups enabled on the database. They want to make sure that they retain the last backup 
before deleting the Amazon RDS database. As the lead developer on the project, what 
should you do?

A. Delete the database. Amazon RDS automatic backups are already enabled.

B. Create a manual snapshot before deleting the database.

C. Use the AWS Database Migration Service (AWS DMS) to back up the database.

D. SSH into the Amazon RDS database and perform a SQL dump.

Anwser:B. Automatic backups do not retain the backup after the database is deleted. Therefore, 
option A is incorrect. Option C is incorrect. The AWS Database Migration Service is used 
to migrate databases from one source to another, which isn’t what you are trying to accomplish here. Option D is incorrect because you cannot SSH into the 
Amazon RDS database, which is an AWS managed service.

13. When using Amazon Redshift, which node do you use to run your SQL queries?

A. Compute node

B. Cluster node

C. Master node

D. Leader node

Anwser:D. The leader node acts as the SQL endpoint and receives queries from client applications, 
parses the queries, and develops query execution plans. Option A is incorrect because the 
compute nodes execute the query execution plan. However, the leader node is where you 
will submit the actual query. Options B and C are incorrect because there is no such thing 
as a cluster or master node in Amazon Redshift.

14. Your company is building a recommendation feature for their application. They would like 
to use an AWS managed graph database. Which service should you recommend?

A. Amazon Relational Database Service (Amazon RDS)

B. Amazon Neptune

C. Amazon ElastiCache

D. Amazon Redshift

Anwser:B. Amazon Neptune is a managed graph database service, which can be used to build 
recommendation applications. Option A is incorrect, because Amazon RDS is a managed 
database service and you are looking for a graph database. Option C is incorrect. Amazon 
ElastiCache is a caching managed database service. Option D is incorrect. Amazon Redshift is a data warehouse servic

15. You have an Amazon DynamoDB table that has a partition key and a sort key. However, a 
business analyst on your team wants to be able to query the DynamoDB table with a different partition key. What should you do?

A. Create a local secondary index.

B. Create a global secondary index.

C. Create a new DynamoDB table.

D. Advise the business analyst that this is not possible.

Anwser:B. A global secondary index enables you to use a different partition key or primary key in 
addition to a different sort key. Option A is incorrect because a local secondary index can 
only have a different sort key. Option C is incorrect. A new DynamoDB table would not solve 
the issue. Option D is incorrect because it is possible to accomplish this.

16. An application is using Amazon DynamoDB. Recently, a developer on your team has 
noticed that occasionally the application does not return the most up-to-date data after a 
read from the database. How can you solve this issue?

A. Increase the number of read capacity units (RCUs) for the table.

B. Increase the number of write capacity units (WCUs) for the table.

C. Refactor the application to use a SQL database.

D. Configure the application to perform a strongly consistent read.

Anwser:D. The application is configured to perform an eventually consistent read, which may not 
return the most up-to-date data. Option A is incorrect—increasing RCUs does not solve 
the underlying issue. Option B is incorrect because this is a read issue, not a write issue. 
Option C is incorrect. There is no need to refactor the entire application, because the issue 
is solvable.

17. A developer on your team would like to test a new idea and requires a NoSQL database. 
Your current applications are using Amazon DynamoDB. What should you recommend?

A. Create a new table inside DynamoDB.

B. Use DynamoDB Local.

C. Use another NoSQL database on-premises.

D. Create an Amazon Elastic Compute Cloud (Amazon EC2) instance, and install a 
NoSQL database.

Anwser:B. DynamoDB Local is the downloadable version of DynamoDB that enables you to write 
and test applications without accessing the web service. Option A is incorrect. Although 
you can create a new table, there is a cost associated with this option, so it is not the best 
option. Option C is incorrect. Even though you can use another NoSQL database, your 
team is already using DynamoDB. This strategy would require them to learn a new database platform. Additionally, you would have to migrate the database to DynamoDB after 
development is done. Option D is incorrect for the same reasons as option C.

18. The AWS Encryption SDK provides an encryption library that integrates with AWS Key 
Management Service (AWS KMS) as a master key provider. Which of the following operations does the AWS Encryption SDK perform to build on the AWS SDKs?

A. Generates, encrypts, and decrypts data keys

B. Uses the data keys to encrypt and decrypt your raw data

C. Stores the encrypted data keys with the corresponding encrypted data in a single 
object

D. All of the above

Anwser:D. The AWS Encryption SDK is a client-side library designed to streamline data security 
operations so that customers can follow encryption best practices. It supports the management of data keys, encryption and decryption activities, and the storage of encrypted data. 
Thus, option D is correct

19. Of all the cryptographic algorithms that the AWS Encryption SDK supports, which one is 
the default algorithm?

A. AES-256

B. AES-192

C. AES-128

D. SSH-256

Anwser:A. Options B, C, and D refer to more outdated encryption algorithms. By default, the AWS 
Encryption SDK uses the industry-recommended AES-256 algorithm.

20. Amazon Elastic Block Store (Amazon EBS) volumes are encrypted by default.

A. True

B. False
Anwser:B. Encryption of Amazon EBS volumes is optional

21. Which of the following cannot be retained when deleting an AWS Elastic Beanstalk 
environment?

A. Source code from the Git repository

B. Data from the automatic backups of an Amazon Relational Database Service (Amazon 
RDS) instance

C. Packaged code from the source bundle stored in an Amazon Simple Storage Service 
(Amazon S3) bucket

D. Data from the snapshot of an Amazon RDS instanc

Anwser: B. Elastic Beanstalk automatically deletes your Amazon RDS instance when your environment is deleted and does not automatically retain the data. You must create a snapshot of 
the Amazon RDS instance to retain the data.
22. Which of the following is not part of the AWS Elastic Beanstalk functionality?
A. Notify the account user of language runtime platform changes
B. Display events per environment
C. Show instance statuses per environment
D. Perform automatic changes to AWS Identity and Access Management (IAM) policies
Anwser: D. Elastic Beanstalk cannot make automated changes to the policies attached to the service 
roles and instance roles.
23. What happens to AWS CodePipeline revisions that, upon reaching a manual approval gate, 
are rejected?
A. The pipeline continues.
B. A notification is sent to the account administrator.
C. The revision is treated as failed.
D. The pipeline creates a revision clone and continues.
Anwser: C. Option C is correct because if a revision does not pass a manual approval transition 
(either by expiring or by being rejected), it is treated as a failed revision. Successive revisions can then progress past this approval gate (if they are approved). Pipeline actions for a 
specific revision will not continue past a rejected approval gate, so option A is incorrect. A 
notification can be sent to an Amazon Simple Notification Service (Amazon SNS) topic that 
you specify when a revision reaches a manual approval gate, but no additional notification 
is sent if a change is rejected; therefore, option B is incorrect. Option D is incorrect, as AWS 
CodePipeline does not have a concept of “cloning” revisions.
24. Which of the following is an invalid strategy for migrating data to AWS CodeCommit?
A. Incrementally committing files from a large repository
B. Syncing the files from Amazon Simple Storage Service (Amazon S3) using the sync
AWS CLI command
C. Cloning an existing repository, updating the remote, and pushing
D. Manually creating files in the AWS Management Console
Anwser: B. Though option D would be time-consuming, it is still possible to create files in the AWS 
CodeCommit console. Option A is a recommended strategy for migrating a repository containing a large number of files. Option C is also a valid strategy for smaller repositories. 
However, there is no way to sync files directly from an Amazon S3 bucket to an AWS CodeCommit repository. Thus, option B is correct.
25. You have an AWS CodeBuild task in your pipeline that requires large binary files that do 
not frequently change. What would be the best way to include these files in your build?
A. Store the files in your source code repository. They will be passed in as part of the 
revision.
B. Store the files in an Amazon Simple Storage Service (Amazon S3) bucket and copy 
them during the build.
C. Create a custom build container that includes the files.
D. It is not possible to include files above a certain size.
Anwser: C. Option A is not recommended, because storing binary files in a Git-based repository 
incurs significant storage costs. Option B can work. However, you would have to pay 
additional data transfer costs any time a build is started. Option C is the most appropriate 
choice, because you can update the build container any time you need to change the files. 
Option D is incorrect, as AWS CodeBuild does not limit the size of files that can be used
26. When you update an AWS::S3::Bucket resource, what is the expected behavior if the Name
property is updated?
A. The resource is updated with no interruption.
B. The resource is updated with some interruption.
C. The resource is replaced.
D. The resource is deleted.
Anwser: C. Amazon Simple Storage Service (Amazon S3) bucket names are globally unique and 
cannot be changed after a bucket is created. Thus, options A and B are incorrect. Option 
D is incorrect because the resource is not being deleted, only updated. Option C is correct 
because you must create a replacement bucket when changing this property in AWS 
CloudFormation
27. What is the preferred method for updating resources created by AWS CloudFormation?
A. Updating the resource directly in the AWS Management Console
B. Submitting an updated template to AWS CloudFormation to modify the stack
C. Updating the resource using the AWS Command Line Interface (AWS CLI)
D. Updating the resource using an AWS Software Development Kit (AWS SDK)
Anwser: B. Option B is correct because you can manage resources declared in a stack entirely within 
AWS CloudFormation by performing stack updates. Manually updating the resource outside of AWS CloudFormation (using the AWS Management Console, AWS CLI, or AWS 
SDK) will result in inconsistencies between the state expected by AWS CloudFormation and 
the actual resource state. This can cause future stack operations to fail. Thus, options A, C, 
and D are incorrect.
28. When does the AWS OpsWorks Stacks configure lifecycle event run?
A. On individual instances immediately when they are first created
B. On individual instances after a deploy lifecycle event
C. On all instances in a stack when a single instance comes online or goes offline
D. On all instances in a stack after a deploy lifecycle event
Anwser: C. Option A is incorrect because this is not the only time configure events run on instances 
in a stack. Options B and D are incorrect because the configure event does not run after a 
deploy event. AWS OpsWorks Stacks issues a configure lifecycle event on all instances in a 
stack any time a single instance goes offline or comes online. This is so that all instances in 
a stack can be made “aware” of the instance’s status. Thus, option C is correct.
29. Which non-Amazon Elastic Compute Cloud (Amazon EC2) AWS resources can AWS 
OpsWorks Stacks manage? (Select THREE.)
A. Elastic IP addresses
B. Amazon Elastic Block Store (Amazon EBS) volumes
C. Amazon Relational Database Service (Amazon RDS) database instances
D. Amazon ElastiCache clusters
E. Amazon Redshift data warehouses
Anwser: A, B, C. AWS OpsWorks Stacks includes the ability to manage AWS resources such as 
Elastic IP addresses, EBS volumes, and Amazon RDS instances. Thus, options A, B, and C 
are correct. Options D and E are incorrect because OpsWorks Stacks does not include any 
automatic integrations with Amazon ElastiCache or Amazon Redshift
30. Which AWS Cloud service can Simple Active Directory (Simple AD) use to authenticate 
users?
A. Amazon WorkDocs
B. Amazon Cognito
C. Amazon Elastic Compute Cloud (Amazon EC2)
D. Amazon Simple Storage Service (Amazon S3)
Anwser: ption A is correct because Simple Active Directory (Simple AD) can be used to authenticate users of Amazon WorkDocs. Options B, C, and D are incorrect because Amazon 
Cognito is an identity provider (IdP), and you cannot use Simple AD to authenticate users 
of Amazon EC2 or Amazon S3.
31. What is the best application of Amazon Cognito?
A. Use instead of Active Directory for AWS Identity and Access Management (IAM) users.
B. Provide authentication to third-party web applications.
C. Use as an Amazon Aurora database.
D. Use to access objects in an Amazon Simple Storage Service (Amazon S3) bucket
B. Amazon Cognito acts as an identity provider (IdP) to mobile applications, eliminating 
the need to embed credentials into the web application itself. Option A is incorrect because 
if a customer is currently using Active Directory as their IdP, it is not good practice to create another IdP to operate and manage. Option C is incorrect because an Amazon Aurora 
database that is used to track data does not assign policies. Option D is incorrect because 
you can use Amazon Cognito to control an application’s access to either an S3 bucket or an 
Amazon S3 object. You don’t use it to directly control access to that bucket or object.
32. You manage a sales tracking system in which point-of-sale devices send transactions of this 
form:
{"date":"2017-01-30", "amount":100.20, "product_id": "1012", "region": 
"WA", "customer_id": "3382"}
You need to generate two real-time reports. The first reports on the total sales per day for 
each customer. The second reports on the total sales per day for each product. Which AWS 
offerings and services can you use to generate these real-time reports?
A. Ingest the data through Amazon Kinesis Data Streams. Use Amazon Kinesis Data Analytics to query for sales per day for each product and sales per day for each customer using 
SQL queries. Feed the result into two new streams in Amazon Kinesis Data Firehose.
B. Ingest the data through Kinesis Data Streams. Use Kinesis Data Firehose to query for 
sales per day for each product and sales per day for each customer with SQL queries. 
Feed the result into two new streams in Kinesis Data Firehose.
C. Ingest the data through Kinesis Data Analytics. Use Kinesis Data Streams to query for 
sales per day for each product and sales per day for each customer with SQL queries. Feed 
the result into two new streams in Kinesis Data Firehose.
D. Ingest the data in Amazon Simple Queue Service (Amazon SQS). Use Kinesis Data 
Firehose to query for sales per day for each product and sales per day for each 
customer with SQL queries. Feed the result into two new streams in Kinesis Data 
Firehose.
A. Option A is correct because you want to ingest into Amazon Kinesis Data Streams, pass 
that into Amazon Kinesis Data Analytics, and finally feed that data into Amazon Kinesis 
Data Firehose. Option B is incorrect because Kinesis Data Firehose cannot run SQL queries. Option C is incorrect because Kinesis Data Streams cannot run SQL queries. Option 
D is incorrect because Kinesis Data Analytics cannot run SQL queries against data in Amazon SQS.
33. You design an application for selling toys online. Every time a customer orders a toy, you 
want to add an item into the orders table in Amazon DynamoDB and send an email to the 
customer acknowledging their order. The solution should be performant and cost-effective. 
How can you trigger this email?
A. Use an Amazon Simple Queue Service (Amazon SQS) queue.
B. Schedule an AWS Lambda function to check for changes to the orders table every 
minute.
C. Schedule an Lambda function to check for changes to the orders table every second.
D. Use Amazon DynamoDB Streams.
D. Option D is correct because Amazon DynamoDB Streams allows Amazon DynamoDB 
to publish a message every time there is a change in a table. This solution is performant 
and cost-effective. Option A is incorrect because if you add an item to the orders table in 
DynamoDB, it does not automatically produce messages in Amazon Simple Queue Service 
(Amazon SQS). Options B and C are incorrect because if you check the orders table every 
minute or every second, it will degrade performance and increase costs.
34. A company would like to use Amazon DynamoDB. They want to set up a NoSQL-style 
trigger. Is this something that can be accomplished? If so, how?
A. No. This cannot be done with DynamoDB and NoSQL.
B. Yes, but not with AWS Lambda.
C. No. DynamoDB is not a supported event source for Lambda.
D. Yes. You can use Amazon DynamoDB Streams and poll them with Lambda.
D. AWS Lambda supports Amazon DynamoDB event streams as an event source, which 
can be polled. You can configure Lambda to poll this stream, look for changes, and create 
a trigger. Option A is incorrect because this can be accomplished with DynamoDB event 
streams. Option B is incorrect because this can be accomplished with Lambda. Option C 
DynamoDB is a supported event source for Lambda.

35. A company wants to access the infrastructure on which AWS Lambda runs. Is this possible?
A. No. Lambda is a managed service and runs the necessary infrastructure on your 
behalf.
B. Yes. They can access the infrastructure and make changes to the underlying OS.
C. Yes. They need to open a support ticket.
D. Yes, but they need to contact their Solutions Architect to provide access to the environment.
A. AWS Lambda uses containers to operate and is a managed service—you cannot access 
the underlying infrastructure. This is a benefit because your organization does not need to 
worry about security patching and other system maintenance. Option B is incorrect—you 
cannot access the infrastructure. Recall that Lambda is serverless. Option C is incorrect. 
AWS Support cannot provide access to the direct environment. Option D is incorrect—the 
Solutions Architect cannot provide direct access to the environment.
36. Using the smallest amount of memory possible for an AWS Lambda function, currently 
128 MB, will result in the lowest bill.
A. True. Lambda bills based on the total memory allocated.
B. False. Lambda has a flat rate—memory allocation is not important for billing, only 
performance.
C. False. Lambda bills based on memory plus the number of times that you trigger the 
function.
D. False. Lambda bills based on memory, the amount of compute time spent on a function 
in 100-ms increments, and the number of times that you execute or trigger a function.
D. AWS Lambda uses three factors when determining cost: the amount of memory allocated, the amount of compute time spent on a function (in 100-ms increments), and the 
number of times you execute or trigger a function. Options A, B, and C are all incorrect 
because Lambda is billed based on memory allocated, compute time spent on a function in 
100-ms increments, and the number of times that you execute or trigger a function.
37. Which Amazon services can you use for caching? (Select TWO.)
A. AWS CloudFormation
B. Amazon Simple Storage Service (Amazon S3)
C. Amazon CloudFront
D. Amazon ElastiCache
C, D. Option A is incorrect because AWS CloudFormation is a service that helps you model 
and set up your AWS resources. Option B is incorrect because you use Amazon S3 as a storage tool for the internet. Options C and D are correct because they are both caching tool
38. Which Amazon API Gateway feature enables you to create a separate path that can be helpful in creating a development endpoint and a production endpoint?
A. Authorizers
B. API keys
C. Stages
D. Cross-origin resource sharing (CORS)
C. Option A is incorrect, as authorizers enable you to control access to your APIs by using 
Amazon Cognito or an AWS Lambda function. Option B is incorrect because API keys are 
used to provide customers to your API, which is useful for selling your API. Option C is the 
correct answer. You can use stages to create a separate path with multiple endpoints, such 
as development and production. Option D is incorrect, as CORS is used to allow one service to call another service.

39. Which of the following methods does Amazon API Gateway support?
A. GET
B. POST
C. OPTIONS
D. All of the above
D. API Gateway supports all of the methods listed. GET, POST, PUT, PATCH, DELETE, HEAD, 
and OPTIONS are all supported methods.
40. Which authorization mechanisms does Amazon API Gateway support?
A. AWS Identity and Access Management (IAM) policies
B. AWS Lambda custom authorizers
C. Amazon Cognito user pools
D. All of the above
D. With Amazon API Gateway, you can enable authorization for a particular method with 
IAM policies, AWS Lambda custom authorizers, and Amazon Cognito user pools. Options 
A, B, and C are all correct, but option D is the best option because it combines all of them
41. Which tool can you use to develop and test AWS Lambda functions locally?
A. AWS Serverless Application Model (AWS SAM)
B. AWS SAM CLI
C. AWS CloudFormation
D. None of the above
B. Option A is incorrect. Though AWS SAM is needed for the YAML/JSON template 
defining the function, it does not allow for testing the AWS Lambda function locally. 
Option B is the correct answer. AWS SAM CLI allows you to test the Lambda function 
locally. Option C is incorrect. AWS CloudFormation is used to deploy resources to the AWS 
Cloud. Option D is incorrect because AWS SAM CLI is the tool to test Lambda functions 
locally
42. Which serverless AWS service can you use to store user session state?
A. Amazon Elastic Compute Cloud (Amazon EC2)
B. Amazon ElastiCache
C. AWS Elastic Beanstalk
D. Amazon DynamoDB
D. Option A is incorrect. Amazon EC2 is a virtual machine service. Option B is incorrect 
because Amazon ElastiCache deploys clusters of machines, which you are then responsible 
for scaling. Option C is incorrect because Elastic Beanstalk deploys full stack applications 
by using Amazon EC2. Option D is correct because ElastiCache can store session state in a 
NoSQL database. This option is also serverless.
43. Which AWS service can you use to store user profile information?
A. Amazon CloudFront
B. Amazon Cognito
C. Amazon Kinesis
D. AWS Lambda
B. With Amazon Cognito, you can create user pools to store user profile information and 
store attributes such as user name, phone number, address, and so on. Option A is incorrect. Amazon CloudFront is a content delivery network (CDN). Option C is incorrect. 
Amazon Kinesis is a service that you can implement to collect, process, and analyze streaming data in real time. Option D is incorrect. By using AWS Lambda, you can create custom 
programming functions for compute processing.

44. Which of the following objects are good candidates to store in a cache? (Select THREE.)
A. Session state
B. Shopping cart
C. Product catalog
D. Bank account balance
A, B, C. Option D is incorrect because when compared to the other options, a bank balance is not likely to be stored in a cache; it is probably not data that is retrieved as frequently as the others. Options A, B, and C are all better data candidates to cache because 
multiple users are more likely to access them repeatedly. However, you could also cache the 
bank account balance for shorter periods if the database query is not performing well.
45. Which of the following cache engines does Amazon ElastiCache support? (Select TWO.)
A. Redis
B. MySQL
C. Couchbase
D. Memcached
A, D. Options A and D are correct because Amazon ElastiCache supports both the Redis 
and Memcached open source caching engines. Option B is incorrect because MySQL is not a 
caching engine—it is a relational database engine. Option C is incorrect because Couchbase 
is a NoSQL database and not one of the caching engines that ElastiCache supports.
46. How can you aggregate Amazon CloudWatch metrics across Regions?
A. CloudWatch does not aggregate data across Regions.
B. This is enabled by default.
C. Send the metric data from other Regions to Amazon Simple Storage Service (Amazon S3) 
for retrieval by CloudWatch.
D. Stream the metric data to Amazon Kinesis, and retrieve it using an AWS Lambda 
function.
A. Amazon CloudWatch does not aggregate data across Regions; therefore, option A is 
correct.
47. Why would an Amazon CloudWatch alarm report as INSUFFICIENT_DATA instead of OK or 
ALARM? (Select THREE.)
A. The alarm was just created.
B. The metric is not available.
C. There is an AWS Identity and Access Management (IAM) permission preventing the 
metric from receiving data.
D. Not enough data is available for the metric to determine the alarm state.
A, B, D. Amazon CloudWatch alarms changes to a state other than INSUFFICIENT_DATA only 
when the alarm resource has had sufficient time to initialize and there is sufficient data available for the specified metric and period. Option C is incorrect because permissions for sending 
metrics to CloudWatch are the responsibility of the resource sending the data. Option D is 
incorrect because the alarm does not create successfully unless it has a valid period.
E. The alarm period is missing.
48. You were asked to develop an administrative web application that consumes low throughput and rarely receives high traffic. Which of the following instance type families will be 
the most optimized choice?
A. Memory optimized
B. Compute optimized
C. General purpose
D. Accelerated computing
C. General-purpose instances provide a balance of compute, memory, and networking resources. T2 instances are a low-cost option that provides a small amount of CPU 
resources that can be increased in short bursts when additional cycles are available. They 
are well suited for lower-throughput applications, such as administrative applications or 
low-traffic websites. For more details on the instance types, see https://aws.amazon 
.com/ec2/instance-types/.
49. Which of the following AWS Cost Management Tools can you use to view your costs and 
find ways to take advantage of elasticity?
A. AWS Cost Explorer
B. AWS Trusted Advisor
C. Amazon CloudWatch
D. Amazon EC2 Auto Scaling
A. AWS Cost Explorer reflects the cost and usage of Amazon Elastic Compute Cloud 
(Amazon EC2) instances over the most recent 13 months and forecasts potential spending 
for the next 3 months. By using Cost Explorer, you can examine patterns on how much you 
spend on AWS resources over time, identify areas that need further inquiry, and view trends 
that help you understand your costs. In addition, you can specify time ranges for the data 
and view time data by day or by month. Option D is incorrect because Amazon EC2 Auto 
Scaling helps you to maintain application availability and enables you to add or remove EC2 
instances automatically according to conditions that you define. It does not give you insights 
into costs incurred.
50. Because cloud resources are easier to deploy and they incur usage-based costs, your organization is setting up good governance rules to manage costs. They are currently focusing on 
controlling and restricting Amazon Elastic Compute Cloud (Amazon EC2) instance deployments. Which of the following is an effective recommendation?
A. Seek approval from Cost Engineering teams before deploying any EC2 instances.
B. Use AWS Identity and Access Management (IAM) policies to enable engineers to 
deploy EC2 instances only when specific mandatory tags are used.
C. Review Amazon CloudWatch metrics to optimize the resource utilization.
D. Use AWS Cost Explorer usage and forecasting reports.
B. You can use tags to control permissions. Using IAM policies, you can enforce the tag to 
gain precise control over access to resources, ownership, and accurate cost allocation. Option 
A is incorrect because eventually deployments become unmanageable, given the scale and rate 
at which resources get deployed in a successful organization. Options C and D are incorrect 
because Amazon CloudWatch and AWS Cost Explorer are unrelated to access controls and 
measures, and these tools monitor resources after they are created.
51. Because your applications are showing a consistent steady-state compute usage, you have 
decided to purchase Amazon Elastic Compute Cloud (Amazon EC2) Reserved Instances to 
gain significant pricing discounts. Which of the following is not the best purchase option?
A. All Upfront
B. Partial Upfront
C. No Upfront
D. Pay-as-you-go
D. You can choose among the three payment options when you purchase a Standard 
or Convertible Reserved Instance. With the All Upfront option, you pay for the entire 
Reserved Instance term with one upfront payment. This option provides you with the largest discount compared to On-Demand Instance pricing. With the Partial Upfront option, 
you make a low upfront payment and then are charged a discounted hourly rate for the 
instance for the duration of the Reserved Instance term. The No Upfront option requires no 
upfront payment and provides a discounted hourly rate for the duration of the term.

52. Your application processes transaction-heavy and IOPS-intensive database workloads. You 
need to choose the right Amazon Elastic Block Store (Amazon EBS) volume so that application performance is not affected. Which of the following options would you suggest?
A. HDD-backed storage (st1)
B. SSD-backed storage (io1)
C. Amazon Simple Storage Service (Amazon S3) Intelligent Tier class storage
D. Cold HDD-backed storage (sc1)
B. The performance of the transaction-heavy workloads depends primarily on IOPS; SSDbacked volumes are designed for transactional, IOPS-intensive database workloads, boot volumes, and workloads that require high IOPS. For more information, see https://docs.aws.
amazon.com/AWSEC2/latest/UserGuide/AmazonEBS.html.
53. A legacy financial institution is planning for a huge technical upgrade and planning to go 
global. The architecture depends heavily on using caching solutions. Which one of the following services does not fit into the caching solutions?
A. Amazon ElastiCache for Redis
B. Amazon ElastiCache for Memcached
C. Amazon DynamoDB Accelerator
D. Amazon Elastic Compute Cloud (Amazon EC2) memory-optimized
D. Options A, B, and C help in building a high-speed data storage layer that stores a subset of 
data. This data is typically transient in nature so that future requests for that data are served 
up faster than is possible by accessing the data’s primary storage location. Option D only supplements the setup of your own caching mechanism, and that is not the preferred solution for 
this scenario. For more information, see https://aws.amazon.com/caching/aws-caching/.
54. Which of the following characteristics separates Amazon DynamoDB from the Amazon 
Relational Database Service (Amazon RDS) design?
A. Incurs the performance costs of an ACID-compliant transaction system
B. Normalizes data and stores it on multiple tables
C. Keeps related data together
D. May require expensive joins
C. Keeping data together is a basic characteristic of a NoSQL database such as Amazon 
DynamoDB. Keeping related data in proximity has a major impact on cost and performance. Instead of distributing related data items across multiple tables, keep related items 
in your NoSQL system as close together as possible. Options A, B, and D are typical characteristics of a relational database.

55. Which of the following partition key choices is an inefficient design that leads to poor distribution of the data in an Amazon DynamoDB table?
A. User ID, where the application has many users
B. Device ID, where each device accesses data at relatively similar intervals
C. Status code, where there are only a few possible status codes
D. Session ID, where the user session remains distinct
C. The status code option suggests an inefficient partition key, because few possible status 
codes lead to uneven distribution of data and cause request throttling. Options A, B, and D 
suggest the efficient partition keys because of their distinct nature, which leads to an even 
distribution of the data. For more information, see:
https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/ 
bp-partition-key-design.html
56. You are planning to build serverless backends by using AWS Lambda to handle web, 
mobile, Internet of Things (IoT), and third-party API requests. Which of the following are 
the main benefits in opting for a serverless architecture in this scenario? (Select THREE.)
A. No need to manage servers
B. No need to ensure application fault tolerance and fleet management
C. No charge for idle capacity
D. Flexible maintenance schedules
E. Powered for high complex processing
A, B, C. Using a serverless approach means not having to manage servers and not incurring 
compute costs when there is no user traffic. This is achieved while still offering instant scale 
to meet high demand, such as a flash sale on an ecommerce site or a social media mention 
that drives a sudden wave of traffic. Option D is incorrect because AWS Lambda runs your 
code on a high-availability compute infrastructure and performs all the administration 
of the compute resources, including server and operating system maintenance, capacity 
provisioning and automatic scaling, code and security patch deployment, and code monitoring and logging. Option E is incorrect because you can configure Lambda functions to 
run up to 15 minutes per execution. As a best practice, set the timeout value based on your 
expected execution time to prevent your function from running longer than intended.
57. Your enterprise infrastructure has recently migrated to the AWS Cloud. You are now trying 
to optimize the storage solutions. Which of the following are the appropriate storage management tools that you can use to review and analyze the storage classes and access patterns 
usage to help reduce costs? (Select TWO.)
A. Amazon Simple Storage Service (Amazon S3) analytics
B. Cost allocation Amazon S3 bucket tags
C. Amazon S3 Transfer Acceleration
D. Amazon Route 53
E. AWS Budgets
A, B. Use this feature to analyze storage access patterns to help you decide when to transition the right data to the right storage class. This feature observes data access patterns to 
help you determine when to transition less frequently accessed STANDARD storage to the 
STANDARD_IA storage class. Option B is correct. A cost allocation tag is a key-value pair 
that you associate with an Amazon S3 bucket. To manage storage data most effectively, 
you can use these tags to categorize your Amazon S3 objects and filter on these tags in your 
data lifecycle policies. Options C and D are incorrect. These options focus on establishing 
a solution with an efficient data transfer. Option E is incorrect. With AWS Budgets, you 
can set custom budgets that alert you when your costs or usage exceed (or are forecasted to 
exceed) your budgeted amount.
