This repository is dedicated to AWS developer associate program. Given below is the timeline and topics to cover. This timeline is can be chaged during the course as I will progress. The details of each topic will be appended as I will go through the course.


## AWS Certified Developer - Associate

**Day 1 | July 20 2020 | Monday**
- **Introduction**
	- Introduction To The Certified Developer - Associate Course
		- Roadmap of the course.
	- Information For Students Who Have Completed The Solutions Architect Course
	- How To Find The Resources For This Course
		- Exam is objective based from the following domains.
			|Domain|Weighting|
			|-----|-----|
			|Deployment|22%|
			|Security|26%|
			|Development with AWS Services|30%|
			|Refactoring|10%|
			|Monitoring & Troubleshooting|12%|  
	- [Exam Blue Print](https://d1.awsstatic.com/training-and-certification/docs-dev-associate/AWS_Certified_Developer_Associate_Updated_June_2018_Exam_Guide_v1.3.pdf)
		- Minimum Passing score is **720** out **1000**
		- $150 fee for exam
	- The Free Alexa Skill For Amazon

**Day 2 | July 21 2020 | Tuesday**
- **Beginners Guide To IAM**
	- IAM 101
		- Seting up users and granting them permissions to the console.
		- Centralized control of AWS accounts
		- Granular Permissions
			- Different levels of permissions to different users.
		- Multi-Factor Authentication
		- Users.
			- People registered in your AWS account via IAM.
				- Can give users customized permissions.
		- Groups.
			- Permissions which are common to users can be grouped togather and this group can be assigned to those users (e.g HR group, Marketing groups, and database team etc).
		- Roles.
			- Create roles and assign them to AWS resources.
				- Example: S3 bucket access using EC2 instance.
			- These roles can be consumed by both users and AWS resource.
		- Policies.
			- A document that defined one (or more) permissions.
			- Policy can be assigned to a User, Role, or a Group.
	- IAM Lab
		- Customizing the signin url
		- Activation of MFA on root account.
			- A virtual MFA device. 
			- Installing MFA competible application on your PC/phone/tablet etc, for accessing OTP.
			- Follow the instructions to complete MFA.
		- Create individual IAM users.
			- Programmatic Access.
				- Used for AWS API, CLI, SDK, and other development purposes.
			- AWS Management Console access.
				- Used for dealing with AWS management console.
			- Save the credentials before closing the window otherwise you won't get them back.
		- Use groups to assign permissions.
			- Creating groups and selecting relevant permissions for the groups.
			- View the policies by clicking on JSON.
			- Giving separate permissions along with grouped permissions. 
		- Apply an IAM password policy. 
			- Setting up rules for the password.
				- Length
				- Upper/Lower case
				- Digits
				- Special Charactors
				- and much more
		- IAM Roles.
			- Creating role for AWS services according to the needs.
		- [Relevant White Paper](https://d0.awsstatic.com/whitepapers/Security/AWS_Security_Best_Practices.pdf)
	- IAM Summary.

**Day 3 | July 22 2020 | Wednesday**
- **Beginners Guide to EC2 I**
	- EC2 101
		- Resizable compute capacity in the cloud
			- Reduces the time required to obtain and boot new server instances to minutes.
			- Scale the server in minutes up and down.
			- No upfront payments no long term commitments. 
		- On Demand instances.
			- A fixed hourly rate (or even per second) with no commitment.
		- Reserved instances.
			- Provides you with a capacity reservation, and offer a significant discount on hourly charge for an instance
				- 1 Year or 3 Years terms.
		- Spot Instances.	
			- Enables you to bid whatever price you want for instance capacity, providing for even greater savings if your application have flexible start and end times.
			- For running a training job etc.
			- Preferably use on weekends.
			- If the spot instance gets terminated you won't get charged for the hour in which it got terminated.
			- If you terminate the spot instance by yourself you will get charged for that whole hour.
		- Dedicated Hosts.
			- Physical EC2 instances dedicated for your use.
			- Can be purchased as on demand.
		- Families of EC2 instances.
			- **F.I.G.H.T.D.R.M.C.P.X** are the available families.
		- EBS (elastic block storage) volumes for disk.
			- SSD
				- General Purpose SSD.
					- Balances price and performance for a wide variety of workloads.
				- Provisioned IOPS SSD.
					- Highest performance SSD volume for mission-critical workloads.
			- Magnetic.
				- Throughput Optimized HHD
					- Low cost HHD volume designed for frequently accessed, throughput-intensive workloads.
				- Cold HHD.
					- Lowest cost HHD volume desgined for less frequently accessed workloads
				- Magnetic.
					- Previous Generation. Can be a boot volume.
	- EC2 Lab
		- Creating instance and SSH in the instance.
		- Configuring the security role.
		- Setting up a apache webserver.
	- Elastic Load Balancer
		- Helps us manage our load on multiple different servers.
		- Applicatoin Load Balancer.
			- Operates on OSI layer 7.
			- Can make clever routing and rooting decisions.
		- Network Load Balancer
		- Classic Load Balancer


**Day 4 | July 23 2020 | Thursday**
- **Beginners Guide to EC2 II**
	- Route53 Lab
		- AWS DNS Service
		- Registering and Purchasing a domain name
		- Creating Application Load Balancer
			- Listeners are used for the ELBs to tell on which port the ELB will listen.
	- CLI Demo
		- AWS CLI Configuration.
		- [AWS CLI Commands](https://awscli.amazonaws.com/v2/documentation/api/latest/index.html)
	- EC2 with S3 Role Lab
		- Applying role to EC2 for accessing S3 (without stoping it).


**Day 5 | July 24 2020 | Friday**
- **Beginners Guide to EC2 III**
	- RDS (Relational Database Service) 101
		- SQL server, Oracle, MySQL Server, Postgres Server, Amazon Aurora, and MariaDB.
		- Data Warehousing
	- RDS Lab
	- RDS Multi-AZ & Read Replicas
		- Automated Backups.
			- Can recover you database server at any point of time.
			- It will take full daily snapshot and will also store transaction log throughout the day.
			- When you do revercory, AWS will first choose the most recent snapshot of your database server, and then will apply the transaction logs.
		- Database snapshots.
			- You have to take the database snapshots manually.
			- Can be available after deletion of the origianl instance unlike automated backups.
		- Encryption.
		- Read & Write backup.
		- Multi-AZ
			- Disaster recovery
		- Read replica.
			- Scaling out your database by reading from replicate database and primary database.
	- Elasticache 101
		- A web service that makes it easy to deploy, operate, and scale an in-memory cache in cloud.
	- EC2 Summary 


**Day 6 | July 25 2020 | Saturday**
- **S3 I** 
	- S3 101
		- Simple storage service
			- Secure highly available & scalable for file storage.
		- Files can be from 0 bytes to 5 terabytes.
		- There is unlimited storage.
		- S3 is a universal namespace, which means names must be unique globally.
		- Bucket policies and Access controls.
		- Cross Origin Resource Sharing (CORS).
		- S3 IA (Infrequently Accessed)
			- For data which is accessed less frequently, but requires rapid access when needed. 
			- Lower fee than S3 but you are charged a retrieval fee.
		- S3 Glacier very cheap, but used for archival only.
		- S3 chages in amount as storage per GB.
		- Number of requests (Get, Put, Copy etc).
	- S3 Security
		- By default all S3 buckets created are PRIVATE.
		- Bucket policy
			- Bucket policies are used to control the access pattern.
			- Bucket policy is written in JSON.
			- Policies are applied to bucket level
		- Access Control list.
			- Applied at the object level.
	- S3 Policies
		- Creating an S3 bucket.
		- Changing bucket policies.
		- Policy generator.
	- S3 Encryption
		- In transit encryption.
			- SSL/TLS
		- At rest encryption.
			- S3 Managed Keys - SSE-S3
			- AWS key management service, managed keys, SSE-S3
			- Server side encryption with customer provided Keys - SSE-C
		- Client Side Encryption.
			- Encrypt files locally and then upload.
	- Setup Encryption On An S3 Bucket

**Day 7 | July 26 2020 | Sunday**
- **S3 II** 
	- CORS Configuration Lab
	- CloudFront
	- CloudFront Lab
	- S3 Performance Optimization
	- S3 Performance Update
	- S3 Summary


**Day 8 | July 27 2020 | Monday**
- **Introduction to Serverless Computing I**
	- Serverless 101
	- Lambda
	- API Gateway
	- Build a Simple Serverless Website with Route 53, API Gateway, Lambda and S3
	- Version Control With Lambda


**Day 9 | July 28 2020 | Tuesday**
- **Introduction to Serverless Computing II**
	- Make an Alexa Skill Lab
	- Step Functions
	- X-Ray
	- Advanced API Gateway
	- Serverless Summary


**Day 10 | July 29 2020 | Wednesday**
- **DynamoDB I**
	- Introduction to DynamoDB
	- Creating a DynamoDB Table Lab
	- Indexes Deepdive
	- Scan vs Query API Call
	- DynamoDB Provisioned Throughput


**Day 11 | July 30 2020 | Thursday**
- **DynamoDB II**
	- DynamoDB On Demand Capacity
	- DynamoDB Accelerator (DAX)
	- Elasticache
	- DynamoDB Transactions
	- DynamoDB TTL
	- DynamoDB Streams
	- Provisioned Throughput Exceeded & Exponential Backoff
	- DynamoDB Summary


**Day 12 | July 31 2020 | Friday**
- **KMS & Encryption on AWS**
	- KMS 101
	- KMS API Calls
	- KMS Envelope Encryption
	- KMS Exam Tips


**Day 13 | August 1 2020 | Saturday**
- **Other AWS Services I**
	- SQS
	- Simple Notification Service
	- Mobile App
	- SES vs SNS
	- ElasticBeanstalk 101
	- Deploying Applications Using ElasticBeanstalk


**Day 14 | August 2 2020 | Sunday**
- **Other AWS Services II**
	- Updating ElasticBeanstalk
	- Advanced ElasticBeanstalk
	- RDS & ElasticBeanstalk
	- Kinesis 101
	- Kinesis Lab
	- Maker Labs
	- Other AWS Services Summary


**Day 15 | August 3 2020 | Monday**
- **Developer Theory I**
	- What Is CICD
	- CodeCommit 101
	- CodeCommit Lab
	- CodeDeploy 101
	- CodeDeploy Lab


**Day 16 | August 4 2020 | Tuesday**
- **Developer Theory II**
	- CodePipeline 101
	- CodePipeline Lab
	- Advanced CodeDeploy the AppSpec File


**Day 17 | August 5 2020 | Wednesday**
- **Developer Theory III**
	- Docker and CodeBuild Lab Part 1
	- Docker and CodeBuild Lab Part 2
	- Docker and CodeBuild Lab Summary and Exam Tips


**Day 18 | August 6 2020 | Thursday**
- **Developer Theory IV**
	- CloudFormation
	- CloudFormation Lab
	- Serverless Application Model (SAM)
	- CloudFormation & SAM  Lab
	- CloudFormation Nested Stacks
	- Developer Theory Summary


**Day 19 | August 7 2020 | Friday**
- **Advanced IAM Summary**
	- Web Identity Federation
	- Cognito User Pools
	- Cognito Lab
	- Inline Policies vs Managed Policies vs Custom Policies
	- Advanced IAM Summary


**Day 20 | August 8 2020 | Saturday**
- **Monitoring**
	- Introduction To CloudWatch
	- CloudWatch Lab
	- CloudWatch Vs CloudTrail
