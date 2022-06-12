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
