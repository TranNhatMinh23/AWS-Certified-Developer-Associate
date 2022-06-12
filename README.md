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

