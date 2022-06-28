AWS Cloud Practitioner Study Topics
----------------------------------------
# MAIN DOMAIN TOPICS
* Cloud Concepts
* Security & Complaince
* Technology
* Billing & Pricing

---

## Domain 1: Cloud Concepts
- 26% of the exam
- Define the AWS Cloud and its value proposition
- Identify aspect of AWS Cloud economics
- Describe different cloud architecture design principles

## Domain 2: Security & Complaince
- 25% of the exam
- Define AWS Shared responsibility model
- Define AWS Cloud Security and complaince concepts
- Identify AWS access management capabilities
- Identify resources for security support

## Domain 3: Technology
- 33% of the exam
- Define method of deploying and operating IT applications in the AWS Cloud
- Define AWS global infrastructure
- Identify the core AWS Services
- Identify ways to contact support

## Domain 4: Billing & Pricing
- Makes up only 16% of the exam, but very tricky questions 
- Need to memorize (or be able to) the different pricing models for AWS
- Recognize various account structures in AWS billing pricing
- Identify resources available for billing support

*************************
[1. CLOUD CONCEPTS]

What is the Cloud? 
-------------------
- A Cloud -> The Internet
- The Internet -> A world-wide network of billions of devices connected together.
- Cloud Computing: utlizing someone's computer system (a collection of IT Resources) to run virtualization, servers, mail, storage etc via the internet and using a pay-as-you go model.

AWS is the leading cloud computing service provider. Started leasing their IT Resources in 2006. It has 25 major product category with over 200+ services ranging from Analytics to storage.

Official Definition of Cloud Computing
----------------------------------------
Cloud computing is the [on-demand delivery] of compute power, database, storage, applications, and other IT resources [through a cloud services platform] [via the internet] with [pay-as-you-go pricing]

Cloud Computing Features
------------------------
- Instantaneous access to resources
- Access resources where and when you want
- More flexible and affordable than legacy IT infrastructure
- No large upfront payment/investment in hardware

Cloud Computing Benefits
- Pay only when and what you consume
- Scale up or down instantaneously and only pay for what you use
- Benefits from economy of scale (multiple users on the platform bringing the price low)

6 (six) ADVANTAGES of Cloud Computing by AWS
---------------------------------------------
* Trade capital expense for variable expense:
	- Instead of having to invest heavily in data centers and servers before you know how you’re going to use them, you can pay only when you consume computing resources, and pay only for how much you consume.

* Benefit from massive economies of scale:
	- By using cloud computing, you can achieve a lower variable cost than you can get on your own. Because usage from hundreds of thousands of customers is aggregated in the cloud, providers such as AWS can achieve higher economies of scale, which translates into lower pay as-you-go prices.

* Stop guessing capacity
	- Eliminate guessing on your infrastructure capacity needs. When you make a capacity decision prior to deploying an application, you often end up either sitting on expensive idle resources or dealing with limited capacity. With cloud computing, these problems go away. You can access as much or as little capacity as you need, and scale up and down as required with only a few minutes’ notice.

* Increase speed and agility
	- In a cloud computing environment, new IT resources are only a click away, which means that you reduce the time to make those resources available to your developers from weeks to just minutes. This results in a dramatic increase in agility for the organization, since the cost and time it takes to experiment and develop is significantly lower. 

* Stop spending money running and maintaining data center
	- Focus on projects that differentiate your business, not the infrastructure. Cloud computing lets you focus on your own customers, rather than on the heavy lifting of racking, stacking, and powering servers.

* Go global in minutes
	- Easily deploy your application in multiple regions around the world with just a few clicks. This means you can provide lower latency and a better experience for your customers at minimal cost.


Type of Cloud Computing
---
# 1. Computing Model
* IaaS (host)- [Infrastructure as a Service] (main building blocks (aws, azure, gcp)
	- Infrastructure as a Service (IaaS) contains the basic building blocks for cloud IT and typically provides access to networking features, computers (virtual or on dedicated hardware), and data storage space. 

	- IaaS provides you with the highest level of flexibility and management control over your IT resources and is most similar to existing IT resources that many IT departments and developers are familiar with today

	Note: You control the servers, networking, security of your applications while AWS handles the building block of these servers for you including (Data center, Power, High Speed Networks, Regions, Availability etc)

* PaaS (build)- [Platform as a Service] (heroku, netlify)
	- Platform as a Service (PaaS) removes the need for your organization to manage the underlying infrastructure (usually hardware and operating systems) and allows you to focus on the deployment
	and management of your applications. This helps you be more efficient as you don’t need to worry about resource procurement, capacity planning, software maintenance, patching, or any of the other undifferentiated heavy lifting involved in running your application. 

* SaaS (consume)- [Software as a Service] (office365, AWS Cloud9, Google Workspace, Outlook, Gmail, Zoho)
	- Software as a Service (SaaS) provides you with a completed product that is run and managed by the
	service provider. In most cases, people referring to Software as a Service are referring to end-user applications. With a SaaS offering you do not have to think about how the service is maintained or how the underlying infrastructure is managed; you only need to think about how you will use that particular piece of software. A common example of a SaaS application is web-based email which you can use to send and receive email without having to manage feature additions to the email product or maintain the servers and operating systems that the email program is running on.


# 2. Deployment Models
* Cloud (Public Cloud) - utilize flexibility and affordaility of cloud computing
	- A cloud-based application is fully deployed in the cloud and all parts of the application run in the cloud. Applications in the cloud have either been created in the cloud or have been migrated from an existing infrastructure to take advantage of the benefits of cloud computing. Cloud-based applications can be built on low-level infrastructure pieces or can use higher level services that provide abstraction from the management, architecting, and scaling requirements of core infrastructure.

*  On-Premises (Private Cloud) - secured an on-premises, high-data retrieval speed, virtualizatio of legacy resources
	- The deployment of resources on-premises, using [virtualization and resource management tools], is
	sometimes called the “private cloud.” On-premises deployment doesn’t provide many of the benefits of
	cloud computing but is sometimes sought for its ability to provide dedicated resources. In most cases
	this deployment model is the same as legacy IT infrastructure while using application management and
	virtualization technologies to try and increase resource utilization. 

* Hybrid Cloud - partially on-premises and partially on the cloud
	- A hybrid deployment is a way to connect infrastructure and applications between cloud-based
	resources and existing resources that are not located in the cloud. The most common method of hybrid
	deployment is between the cloud and existing on-premises infrastructure to extend, and grow, an
	organization's infrastructure into the cloud while connecting cloud resources to the internal system.
	- They can use the cloud as a backup of their resources.


AWS Well-Architected Framework (5 best practices)
---
AWS Well-Architected helps cloud architects build secure, high-performing, resilient, and efficient infrastructure for a variety of applications and workloads. It is built around 6-pillars:

* Operational Excellence Pillar:
	- The operational excellence pillar focuses on running and monitoring systems, and continually improving processes and procedures. Key topics include automating changes, responding to events, and defining standards to manage daily operations.

* Security Pillar:
	- The security pillar focuses on protecting information and systems. Key topics include confidentiality and integrity of data, managing user permissions, and establishing controls to detect security events.

* Reliability Pillar:
	- The reliability pillar focuses on workloads performing their intended functions and how to recover quickly from failure to meet demands. Key topics include distributed system design, recovery planning, and adapting to changing requirements.

* Performance Efficiency Pillar: 
	- The performance efficiency pillar focuses on structured and streamlined allocation of IT and computing resources. Key topics include selecting resource types and sizes optimized for workload requirements, monitoring performance, and maintaining efficiency as business needs evolve.

* Cost Optimization Pillar:
	- The cost optimization pillar focuses on avoiding unnecessary costs. Key topics include understanding spending over time and controlling fund allocation, selecting resources of the right type and quantity, and scaling to meet business needs without overspending.

* Sustainability Pillar:
	- The sustainability pillar focuses on minimizing the environmental impacts of running cloud workloads. Key topics include a shared responsibility model for sustainability, understanding impact, and maximizing utilization to minimize required resources and reduce downstream impacts.  

AWS Well-Architected provides a consistent approach for customers and partners to evaluate architectures and implement scalable designs.  

References: 
---
- https://www.wellarchitectedlabs.com/
- https://aws.amazon.com/architecture/well-architected/?wa-lens-whitepapers.sort-by=item.additionalFields.sortDate&wa-lens-whitepapers.sort-order=desc

---
 The AWS Well-Architected Tool, available at no cost in the AWS Management Console, provides a mechanism for regularly [evaluating workloads], [identifying high-risk issues], and [recording improvements].

 Build the most secure, durable, efficient and high-performing IT infrastructure possible (sustainability)

As described by the lecturer on Linkedin.

1. Avoid unnecessary cost (cost optimization)
	-Use only what you need
	-Reserve resources in advance
	-Continue to monitor for optimization

2. Reliability
	-Test disaster recovery setings
	-Incorporate redundancy
	-Have duplicate copies of resources

3. Efficiency
	-To use computing resources to adjust your system requirement

4. Infrastructure Security (Information, systems, assets)
	- Best practices should be automated
	- Data should always be protected (Intransits and @rest (stored at a storage server)
	- Enable tracebility (strong identity foundation)
	- Manage access to resources

5. Operational excellence (ability to run and optimize system running smoothly)
	-Document everything
	-Refine operational procedures
	-Anticipate failure
	-Update processes
	-Learn from failure

Quick Fact of AWS 
---
- Jeff Bezos started amazon in 1994 as an humble e-commerce business
- Amazon Web Services was made public in 2006
- Planned on launching Merchant.com - an ecommerce platform for third-party shops instead paved the way for Amazon to evolve from "Online Store" to "Service Company"
- In 2007, 10% of Amazon's revenue came from AWS.
- Their initial serviced lauched in 2006 were
	* Simple Queue Services (SQS) - 2004
	* Simple Storage Services (S3) - March 2006
	* Elastic Compute Cloud (EC2) - August 2006
- They started offering ceritification program to support industry-wide training and skills standardization in 2013.
- In October 2018, AWS added new category "Blockchain" and "Satellite"

AWS - Amazon Web Service (a Cloud Platform) having 25 Categorized Products with 200+ cloud services. 

It is a Cloud Computing service providr that offers flexibility, reliability, and affordability.

[A CLOUD SERVICE PROVIDER] :  is a company which provides multiple Cloud Services, and those Cloud Services can be chained together to create cloud architectures most commonly through internet-hosted computing, storage, and software services.

## POPULAR AWS SERVICES
- Compute (EC2, Elastic Beanstack)
- Storage (S3)
- Database (RDB, DynamoDB, RedShift, Elastic Cache)

## PRACTICAL (HANDS-ON)
- Visit AWS Free Tier (aws.amazon.com/free)
- After 12months, you will be charge regular rate
- 3 times of free tier
	- Always free (always available)
	- 12 Months free (expires after 12months and if you go above the limit, 
	(limitations)
		* Use time
		* Number of requests
		* Amount of storage
		* Number of characters
		* Actions per month
	- Trials (less than 12months with strict limits)
		* a free tier that helps brings new customers to aws (marketing stunt)

PROJECT (USE CASE)
- Create a WordPress blog using AWS EC2 and Route 53

Project links:
- https://intellipaat.com/blog/aws-projects-ideas/
- https://www.upgrad.com/blog/aws-projects-ideas/
- https://mindmajix.com/aws-projects
- https://www.hackster.io/AmazonWebServices/projects


AWS GLOBAL INFRASTRUCTURE
---
- AWS Region 
	: An AWS Region is a physical location in the world where we have multiple Availability Zones. It is a geographical location

- AWS Availability
	: Availability Zones consist of one or more discrete data centers, each with redundant power, networking, and connectivity, housed in separate facilities
	: These Availability Zones offer you the ability to operate production applications and databases that are more highly available, fault tolerant, and scalable than would be possible from a single data center
	: Availability Zones are multiple, isolated locations within each Region.

- Edge Location


***************************
# [2. SECURITY & COMPLIANCE]

## Area of focus on AWS Security & Complaince
- Define the AWS Shared responsibility Model
- Define the AWS Cloud Security and compliance concepts
- Identify AWS Access management capabilities
- Identify resources for receiving security-related support

## Take note of these Recommended security practices
- Shared Responsibility Model
- Security Pillar of Well-Architected Framework
- Principle of least Privilege

## IT Infrastructre in the Past
- Server rooms secured with key cards
- Off-site data centers
- Lots of security devices and people
- Difficult to access


## Shared Responsibility Model (SRM)
(Your responsibility vs AWS responsibility)
Security of cloud computing infrastructures and data is a SHARED RESPONSIBILITY between the customer and AWS

- AWS is responsible for SECURITY OF THE CLOUD
- The customer is responsible for SECURITY IN THE CLOUD

AWS is responsible for "Security of the Cloud":
* AWS is responsible for protecting the infrastructure such as:
	- physical security of data centers hosting the AWS Cloud
	- Security of hardward, software, networing, and so on, that runs the cloud computing service
so in general, AWS is responsible for security of the computents that make up the AWS CLoud (like the data centers and physical servers)

Customers is responsible for "Security on the Cloud":
* Every customer on AWS Cloud is responsible for protecting their own services/data/infrastruture i.e the customer is responsible for security of things inside the AWS Cloud.
	- Customers are responsible for varying levels of security functions depending on the AWS Cloud service used, such as:
		- protecting customer data and data encryption
		- platform, applications , Identity and Access Management
		- patching operating systems of VMs etc
		- configuring firewalls etc

Reference: https://docs.aws.amazon.com/wellarchitected/latest/security-pillar/welcome.html
---

## The 3 Major Security Practice of AWS
1. Shared Responsibility Model.
2. SECURITY PILLAR of Well-Architected Framework.
3. Principle of Least Privilege.

## Security on AWS Well-architected framework - the five/six pillars include
Using the SCROPS - Structur
- Security
- Cost Optimization
- Reliability
- Operational Excellence
- Performance Efficiency
- Sustainability

Focusing on the Security part of the Well-architected Framwork, we have the following component that will help us to build architectures that protect your data and systems, control access, and respond automatically to security events.

### 5 SECURITY PILLAR COMPONENT INCLUDE:
- Identity & Access Management (IAM) including "Identity Management & Permission Management"
	* Actively manage all-user access
	* Use strong identity foundation
	* Principle of least privilege:
		Every role has a set of access permsissions necesary to effectively complete its job, and the individual in the role should have no more or no less than the optimal level of access.
			* Use Identity Access Management (IAM) to provide access
			* You can provide access to resources to both users and other AWS Services
			* Grouping users with the expected permission limits what each users in the group can do
			* Start with minimum set of permissions, and grand additional only as necessary
			* Determine what user/service needs to be able to do and craft policies to perform only those specific tasks

	[Tools: AWS IAM]

- Detective Control including 'Configure and Investigate'
	* Enable traceability: ""Who did what, when?"
	* Actively monitor alerts
	* Audit actions and changes to environment in real time
	
	[Tools:  AMAZON Shields, AWS Trusted Advior] 

- Infrastructure Protection including "Protecting Network & Protecting Compute"
	* Apply security on all layers of infrastructure
	* Not just the outer layer like the physcal data center
	* Virtual servers: security multiple ayers like subnet, load balancer, and OS
	* Security best practices should be automated to save time and money when scaling
	
	[Tools: AWS Shield & ]

- Data Protection including "Data Classification, Protecting Data at Rest, Protecting Data in Transit"
	* Data shoud be protected AT REST (images saved in s3 bucket)
	* Data should be protected IN TRANSIT (Email being sent from one server to another)
	* Security mechanisms should be adjusted depending on sensitivity of data
	* Keep people away from data (eliminate the need to direct access or manual proccessing of data)
	
	[Tools:  AWS Web Application Firewall (WAF)]

- Incident Response
	* Intervene, investigate, and deal with all security events
	* Once issue is resolved, update incident management process
	* Continue to learn from past mistakes and security events
	
	[Tools: Amazon Inspector]


## AWS Cloud Compliance Programs
The AWS Compliance Program helps customers to understand the robust controls in place at AWS to maintain security and compliance in the cloud. By tying together governance-focused, audit-friendly service features with applicable compliance or audit standards, AWS Compliance Enablers build on traditional programs, helping customers to establish and operate in an AWS security control environment.

These compliances are grouped according to Region. There are compliance that are acceptable globally while others are specific to either the industry or region.

They are broken down by:
- Certifications and Attestations
- Laws
- Regulations & Privacy
- Alignments and Framework

Compliance certifications and attestations are assessed by a third-party, independent auditor and result in a certification, audit report, or attestation of compliance. AWS customers remain responsible for complying with applicable compliance laws, regulations and privacy programs. Compliance alignments and frameworks include published security or compliance requirements for a specific purpose, such as a specific industry or function

More Reference: https://aws.amazon.com/compliance/programs/
---

## SECURITY SERVICES OFFERED BY AWS
* AWS Identity and Access Management (IAM)
	- Manage acces to services and resources on the AWS Cloud
	- Manage users and groups
	- Manage roles
	- Can provide access to users or other AWS Service
	- Permissions are [global]: any access setting will be true across all regions
	- Always Follow th principle of least privilege

	<strong>Benefits of IAM</strong>
		- Enhance security
		- Granular control
		- Ability to provide temporary credentials
		- Flexible security credential management
		- Federated access
		- Seamless integration across various AWS Services

	* Access to AWS Cloud can be controlled using
		- Manage Users
		- Manage IAM Roles
		- Manage Federated Users (users from already existing platform e.g Microsoft Active Directory)

* AWS Web Application Firewall ( AWS WAF)
	- Protects web apps running on the AWS Cloud from common web exploits
	- Firewall service for web application
	- Protect web apps against exploits that could compromise security or availability
	- Protect apps from exploits that could force your app to consume excessive resources (i.e becoming expensive)

	<strong>Benefits of WAF</strong>
		- Improves web traffic visibility
		- Provides cost-effective web app protection
		- Increased security and protection against web attacks
		- Easy to deploy and maintain
		- It can be deployed & maintain on Amazon CloudFront as part of your content deliver network solution or Amazon API Gateway

* AWS Shield (DDoS Protection)
	- An Attempt to make a machine or network resource unavailable
	- Most often by making excessive repeated requests to the websit using thousands of unique IP addresses

	AWS Shield is a tool that can help to resolved most of the issues stipulated above.
		- Provides detection and automatic mitigations
		- Minimize effects of DDoS attacks on your apps
		- Help minimize application downtime and latency when an attack happen

	AWS Shield has two edition:
		- Standards:
			- Automatically enabled
			- Free
			- Protects web application againsts a majority of common DDoS attacks
			- Get comprehensive availability protection against all known infrastructure attacks when you used it with CloudFront and Route 53
		- Advanced:
			- Continous, 247 acces to AWS-DDoS ressponse team
			- Near real-time visibility into events
			- Integrates with AWS WAF
			- Provides higher-level protections, network and transport layer protections, and automated application traffic monitoring
			- Also provides Financial protection against DDoS-related spikes in charges for EC2, elastic load balancers, CloudFront, and Route 53
			- Available globally on all CloudFront and Route 53 Edge locations
			- Your web application can be hosted anywhere in the world and still be protected by AWS Shield

* Amazon Inspector
	- Automated security assessment service for applications
	- Automatically assess for exposure, vulnerabilities, and derivations from best practices
	- Generate detailed reports to help check your vulnerabilities
	- Security teams can get reports validating that tests were performed

	<strong>Benefits of Amazon Inspector</strong>
		- Reduce risk of introducing security issues during deployment and development
		- You can define standards and best practices
		- Or you can use AWS constantly updated standards

* AWS Trusted Advior
	- Guides provisioning of resources to follow AWS best practices
	- Scans your infrastructure and advises you on how it is or is not following AWS best practices
	- It base its decision on Five (5) categories:
		- Cost optimization
		- Performance
		- Security
		- Fault tolenrance
		- Service limits
	- It then provides action recommendations to meet best practice standards

	Note: All AWS users [Basic Support and Developer Support plan] have free 7 (seven) checks free by AWS Trusted Adviser.They are :
		- S3 Buckets permissions
		- Security groups - specific ports unrestricted
		- IAM use
		- MFA on root account
		- EBS public snapshots
		- RDS public snapshots
		- Service limits (list of other services offered by AWS)

	Enterprise users have so much more from AWS Trusted Advisers. If you have a Business, Enterprise On-Ramp, or Enterprise Support plan, you can also use the AWS Support API and the AWS Command Line Interface (AWS CLI) to access your checks.

		- They also get weekly updates
		- More type of checks on top of core checks (used by Basic & Develper plan users)
		- Set up automated actions in response to alerts using Cloud Watch
		- Programmatic access to scan results via AWS Support API

References: https://docs.aws.amazon.com/awssupport/latest/user/trusted-advisor-check-reference.html
---

* Amazon GuardDuty
	- An Online 24/7 threat detection service for the AWS Cloud
	- Monitors for malicious activity and unauthorized behaviour
	- Analyzes events to send actionable alerts via CloudWatch
	- It uses machine learning, anomaly detection, and integrated threat intelligence to identify potential threats.



*************************
[3. TECHNOLOGY]
*************************




*************************
[4. BILLING & PRICING]
*************************