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

