# AWS-Cloud-Practitioner
Notes I used when studying for the AWS Cloud Practioner certification. Hope it helps!

## Cloud Concepts

AWS has lower variable costs and lower upfront costs compare to traditional and virtualized data centers.

Accessing forums, blogs, and whitepapers about security-related topics are available at no cost.

A recommended pattern for designing a highly available architecture on AWS is to ensure that the application is designed to accomodate failure of any single component. 

As application complexity increases, a best practice is application to be broken into smaller, loosely coupled components. This means that IT systems should be designed in a way that reduces interdependencies — a change or a failure in one component should not cascade to other components.

Ways of interacting with AWS: Web Console, command line interface, and software development kits (SDKs). 

AWS Marketplace is a digital catalog with thousands of software listings from independent software vendors that make it easy to find, test, buy, and deploy software that runs on AWS.

Data Center resilience is practiced through Availability Zones across data centers that reduce the impact of failures.

Fault isolation improvement can be made to traditional horizontal scaling by sharding (a method of grouping instances into groups called shards, instead of sending the traffic from all users to every node like in the traditional IT structure.)

Customers benefit from Amazon's massive economies of scale by periodic price reductions as the result of Amazon's operational efficiencies.

Serverless platform includes: AWS lambda, Amazon S3, DynamoDB, API gateway, Amazon SNS, AWS step functions, Amazon kinesis and developing tools and services.

Elasticity involves vertical (increasing/decreasing the size of an item) and horizontal (increasing/decreasing the number of items) scaling.

Disaster recovery scenarios:
* **Backup and Restore**: a simple, straightforward, cost-effective method that backs up and restores data as needed. Keep in mind that because none of your data is on standby, this method, while cheap, can be quite time-consuming.
* **Pilot Light**: this method keeps critical applications and data at the ready so that it can be quickly retrieved if needed.
* **Warm Standby**: This method keeps a duplicate version of your business' core elements running on standby at all times, which makes for a little downtime and an almost seamless transition.
* **Multi-Site Solution**: Also known as a Hot Standby, this method fully replicates your company's data/applications between two or more active locations and splits your traffic/usage between them. If a disaster strikes, everything is simply rerouted to the unaffected area, which means you'll suffer almost zero downtime. However, by running two separate environments simultaneously, you will obviously incur much higher costs.

Capital expenditure or capital expense (capex or CAPEX) is the money an organization or corporate entity spends to buy, maintain, or improve its fixed assets, such as buildings, servers 

Security in the cloud means, a responsibility of customer.
Security of the could means, a responsibility of AWS.

5 Pillars of Well Architected framework is:
* Operational excellence
* Security 
* Reliability
* Performance efficiency
* Cost optimization. 

There are more edge locations than AWS Regions. 
There are more Availability Zones than AWS Regions. 

## Billing 

Consolidated billing for AWS organizations helps consolidating billing and payment for multiple AWS accounts or multiple Amazon Internet Services accounts. Every organization in AWS organization has a master account that pays and member accounts. Benefits are:

* One bill: You get one bill for multiple accounts
* Easy tracking: You can track the charges across multiple accounts and download the combine cost and usage data.
* Combined usage: You can combine the usage across all accounts in the organization to share the volume pricing discounts.
* No extra free: This service has no additional cost.

## Technology

Reserved Instance pricing model: three-year, all upfrond, standard RI pricing provides the highest average savings compare to On-demand pricing.

A characteristic of edge locations is that they help lower latency and improve performace for users.

AWS IAM policies can limit Amazon S3 bucket access to specific users

Elastic Load Balancing is a service that will automatically scale with an expected increase in web traffic.

AWS list of Compute Services:
* Amazon EC2
* Amazon EC2 Auto Scaling
* Amazon Elastic Container Registry
* Amazon Elastic Container Service
* Amazon Elastic Kubernetes Service
* Amazon Lightsail
* AWS Batch
* AWS Elastic Beanstalk
* AWS Fargate
* AWS Lambda
* AWS Serverless Application Repository
* AWS Outposts
* VMware Cloud on AWS

## AWS Concierge

It is customer support service.

We offer a contact/call center software for inbound scheduling, messaging, texting, SMS, voice, chatting, appointment reminder, B2B.
Your AWS Concierge is a senior customer service agent who is assigned to your account when you subscribe to an Enterprise or qualified Reseller Support plan.

This is a support service.

## AWS Config

AWS Config is a service that enables you to assess, audit, and evaluate the configurations of your AWS resources. Config continuously monitors and records your
AWS resource configurations and allows you to automate the evaluation of recorded configurations against desired configurations. With Config, you can review changes in configurations and relationships between AWS resources, dive into detailed resource configuration histories, and determine your overall compliance against the configurations specified in your internal guidelines. This enables you to simplify compliance auditing, security analysis, change management, and operational troubleshooting.

## AWS CloudFormation

AWS CloudFormation provides a common language for you to describe and provision all the infrastructure resources in your cloud environment. CloudFormation allows you to use a simple text file to model and provision, in an automated and secure manner, all the resources needed for your applications across all regions and accounts. This file serves as the single source of truth for your cloud environment.

It provides the ability to manage infrastructure as code.

## AWS Trusted Advisor

Like your customized cloud expert, AWS Trusted Advisor analyzes your AWS environment and provides best practice recommendations in five categories: 
* Cost optimization
* Performance
* Security
* Fault tolerance
* Service limits

## AWS Simple Monthly Calculator

The AWS Simple Monthly Calculator is an easy-to-use online tool that enables you to estimate the monthly cost of AWS services for your use case based on your expected usage. The AWS Simple Monthly Calculator is continuously updated with the latest pricing for all AWS services in all Region


## CloudFront

CloudFront delivers your content through a worldwide network of data centers called edge locations. The regional edge caches are located between your origin web server and the global edge locations that serve content directly to your viewers. This helps improve performance for your viewers while lowering the operational burden and cost of scaling your origin resources.

## EC2

Amazon EC2 Reserved Instances (RI) provide a significant discount (up to 72%) compared to On-Demand pricing and provide a capacity reservation when used in a specific Availability Zone. Types:
* Standard RI: most significant discount (up to 72% off On-Demand) and are best suited for steady-state usage.
* Convertible RI: These provide a discount (up to 54% off On-Demand) and the capability to change the attributes of the RI as long as the exchange results in the creation of Reserved Instances of equal or greater value. Like Standard RIs, Convertible RIs are best suited for steady-state usage.
* Scheduled RI: These are available to launch within the time windows you reserve. This option allows you to match your capacity reservation to a predictable recurring schedule that only requires a fraction of a day, a week, or a month.

Reserved Instances payment methods are:
* All Upfront
* Partial Upfront
* No Upfront


Amazon EC2 Spot Instances let you take advantage of unused EC2 capacity in the AWS cloud. Spot Instances are available at up to a 90% discount compared to On-Demand prices. Spot prices are more predictable, updated less frequently, and are determined by supply and demand for Amazon EC2 spare capacity, not bid prices. Spot instances are not suitable for mission-critical or long-term workloads as they can be stopped at any moment should the resource be needed elsewhere.

On-Demand Instances let you pay for compute capacity by the hour or second (minimum of 60 seconds) with no long-term commitments. This frees you from the costs and complexities of planning, purchasing, and maintaining hardware and transforms what are commonly large fixed costs into much smaller variable costs. This is the most expensive tier.

A vCPU is metric used by AWS to describe the compute power you’ll get from a given instance. In a nutshell, the more you have, the more powerfull the instance will be.

EC2 instance types:
* General-purpose
* Compute-optimized
* Memory-optimized
* Accelerated-computing
* Storage-optimized

A dedicated instance is a regular EC2 instance that, instead of sharing a physical host with other AWS customers, runs on an isolated host that’s set aside exclusively for your account. A dedicated host also gives you instance isolation but, in addition, allows a higher level of control over how your instances will be placed and run within the host environment.

EC2 instance store volumes are ephemeral, no encryption is possible, and they lack flexibility. They have faster data reads and writes than EBS.  



## Elastic Load Balancing (ELB)

Elastic Load Balancing provides confidence that your applications will scale to the demands of your customers. With the ability to trigger Auto Scaling for your Amazon EC2 instance fleet when latency of any one of your EC2 instances exceeds a preconfigured threshold, your applications will always be ready to serve the next customer request

It distributes incoming application traffic across one or more Amazon EC2 instances.

## Amazon Artifacts

It contains AWS compliance documents.

AWS Artifact is your go-to, central resource for compliance-related information that matters to you. It provides on-demand access to AWS's security and compliance reports and select online agreements. The AWS SOC 2 report is particularly helpful for completing questionnaires because it provides a comprehensive description of the implementation and operating effectiveness of AWS security controls. Another useful document is the Executive Briefing within the AWS FedRAMP Partner Package.

## DynamoDB

It is a fast, reliable and serverless NoSQL database. It could be considered as serverless.

## AWS Organizations

It is a service to consolidate and centrally manage multiple AWS accounts

## Amazon Route 53

It is an AWS managed Domain Name System (DNS) web service. 

It takes 24 hours for changes made to a hosted zone in Amazon Route 53 to reflect globally because DNS resolvers around the world can only reflect the changes in their cache after the TTL has expired, it is 24h by default.

The geolocation routing policy allows for different resources to serve content based on the origin of the request. This is useful to present a website in a specific language depending on which country the user is accessing from.

Routing Policies

In some cases, you just need a domain name to resolve to a particular IP address. But there are other times when you want the value of a resource record to change dynamically to work around failures or ensure users get pointed to the least busy server. Route 53 lets you accomplish this with a variety of routing policies.

**Simple**: The Simple routing policy is the default for new resource records. It simply lets you map a domain name to a single static value, such as an IP address. It doesn’t check whether the resource the record points to is available.

**Weighted**: A Weighted policy distributes traffic across multiple resources according to a ratio. For example, when introducing a new web server, you may want to route only 10 percent of the traffic to the new server while evenly distributing the load across the rest.

**Latency**: A Latency policy sends users to resources in the AWS Region that’s closest to them. This is useful if, for instance, you want to send European users to the eu-west-1 region while sending users in the United States to the us-east-1 region.

**Failover**: A Failover policy lets you route traffic to a primary resource unless it’s unavailable. In that case, traffic will be redirected to a secondary resource.

**Geolocation** A Geolocation policy lets you route users based on their specific continent, country, or state.

**Multivalue** Answer A Multivalue Answer policy allows you to evenly distribute traffic across multiple resources. Unlike Weighted policies that return a single record, a Multivalue Answer policy returns all records, sorted in a random order.

Health Checks

All routing policies with the exception of Simple can use health checks to determine whether they should route users to a given resource. A health check can check one of three
things: an endpoint, a CloudWatch alarm, or another health check. All health checks occur every 10 seconds or 30 seconds.

**Endpoint**  Endpoint health checks work by connecting to the endpoint you want to monitor via HTTP, HTTPS, or TCP. Route 53 has health checkers in several AWS Regions, and you can choose which health checkers a health check uses. This lets you ensure that an endpoint is reachable from various locations around the world.

**CloudWatch alarm**: A Route 53 health check can monitor the status of a CloudWatch alarm. This is useful if you want to consider a resource unhealthy if it’s experiencing high
latency or is servicing a high number of connections.

**Calculated** This type of health check monitors the status of other health checks. For example, if you want to consider the status of both an Endpoint health check and a CloudWatch alarm health check, you can create a Calculated health check to take both into account.

## AWS cloud9

AWS Cloud9 is a serverless online IDE used to author, edir, run, and debug code of various languages. 

## Amazon Redshift

It is a data warehouse product 

## Amazon S3

Provides a virtually unlimited amount of online highly durable object storage. Although the service is global, buckets are stored within an specific region. Standard Storage is designed to provide 99.999999999 percent durability and 99.99 percent availability

S3 classes:
* Standard: Durabilitiy: 99.999999999%, Availability: 99.99%, Availability Zones: > 2. Most expensive option in term of cost per GB
* Standard_IA: Durabilitiy: 99.999999999%, Availability: 99.9%, Availability Zones: > 2.  Designed for important data that can’t be re-created. 
* Intelligent_tiering: Durability: 99.999999999%, Availability: 99.9%, Availability Zones: > 2.  automatically moves objects to the most cost-effective storage tier based on past access patterns. An object that hasn’t been accessed for 30 consecutive days is moved to the lower-cost infrequent access tier. Once the object is accessed, it’s moved back to the frequent access tier. 
* Onezone_IA: Durability: 99.999999999%, Availability: 99.5%, Availability Zones: 1.
* Reduced Redundancy: Durabilitiy: 99.99%, Availability: 99.99%, Availability Zones: > 2. Meant for data that can be easily replaced, if it needs to be replaced at all. It has the lowest durability of all the classes, but it has the same availability as STANDARD. AWS recommends against using this storage class but keeps it available for people who have processes that still depend on it.

Object life cycle confi guration rules are applied to a bucket and consist of one or both of the following types of actions:

**Transition actions**: Transition actions move objects to a different storage class once they’ve reached a certain age. For example, you can create a rule to move objects from the STANDARD storage class to the STANDARD_IA storage class 90 days after creation.

**Expiration actions**: These can automatically delete objects after they reach a certain age. For example, you can create a rule to delete an object older than 365 days. If you have versioning enabled on a bucket, you can create expiration actions to delete object versions of a certain age. This allows you to take advantage of versioning without having to store endless versions of an object. 


## Amazon Relational Database Service (Amazon RDS)

Amazon Relational Database Service (Amazon RDS) makes it easy to set up, operate, and scale a relational database in the cloud. It provides cost-efficient and resizable capacity while automating time-consuming administration tasks such as hardware provisioning, database setup, patching and backups. It frees you to focus on your applications so you can give them the fast performance, high availability, security and compatibility they need.

## Amazon S3 Glacier

Amazon S3 Glacier is a secure, durable, and low-cost storage class of S3 for data archiving and long-term backup. Customers can store large or small amounts of data for as little as $0.004 per gigabyte per month. The S3 Glacier storage class is ideal for archives where data is regularly retrieved and some of the data may be needed in minutes.

It is designed to deliver 99.999999999 percent durability, with comprehensive security and compliance capabilities that can help meet even the most stringent regulatory requirements.

Three options to access archives:
* Expedited: 1-5 minutes to access data, $0.03 per GB, On-Demand: $0.01 per request ; Provisioned: $100 per Provisioned Capacity Unit
* Standard: 3-5 h, $0,01 per GB, $0.050 per 1,000 requests
* Bulk: 5-12 h, $0.0025 per GB, $0.025 per 1,000 requests

## AWS Snowball

Amazon Snowball is a petabyte-scale data transfer service that provides cost efficient data transfer to AWS from tamper proof physical devices. It basically allows you to transfer an immense amount of data to a phyisical device (HDD I assume) for then to be sent to AWS so that the AWS staff can transfer it to your account on the cloud.

Service fee per job: 
* Snowball 50 TB: $200
* Snowball 80 TB: $250

The first 10 days of onsite usage are free. Each extra onsite day is $15.

## AWS Elastic Block Storage (EBS)

Elastic block storage offers persistent block storage volumes for EC2 instances. It survives shutdowns and system crashes.

They can be encrypted and can be moved around, mounted on other instances, and converted to AMIs.



## AWS VPN

AWS Virtual Private Network solutions establish secure connections between your on-premises networks, remote offices, client devices, and the AWS global network. AWS VPN is comprised of two services: AWS Site-to-Site VPN and AWS Client VPN. Together, they deliver a highly-available, managed, and elastic cloud VPN solution to protect your network traffic.

AWS Site-to-Site VPN creates encrypted tunnels between your network and your Amazon Virtual Private Clouds or AWS Transit Gateways. For managing remote access, AWS Client VPN connects your users to AWS or on-premises resources using a free VPN software client.

## AWS Direct Connect

AWS Direct Connect enables you to securely connect your AWS environment to your on-premises data center or office location over a standard 1 gigabit or 10 gigabit Ethernet fiber-optic connection. AWS Direct Connect offers dedicated high speed, low latency connection, which bypasses internet service providers in your network path. An AWS Direct Connect location provides access to Amazon Web Services in the region it is associated with, as well as access to other US regions. AWS Direct Connect allows you to logically partition the fiber-optic connections into multiple logical connections called Virtual Local Area Networks (VLAN). You can take advantage of these logical connections to improve security, differentiate traffic, and achieve compliance requirements

AWS Direct Connect lets you establish a dedicated network connection between your network and one of the AWS Direct Connect locations. Using industry standard 802.1q VLANs, this dedicated connection can be partitioned into multiple virtual interfaces. This allows you to use the same connection to access public resources such as objects stored in Amazon S3 using public IP address space, and private resources such as Amazon EC2 instances running within an Amazon
Virtual Private Cloud (VPC) using private IP space, while maintaining network separation between the public and private environments. Virtual interfaces can be reconfigured at any time to meet your changing needs.

## AWS Service Health Dashboard

It is a concise representation of the general status of AWS services. It provides a minute-by-minute update of system outages and service erros on the AWS global infrastructure. 

## AWS Personal Health Dashboard

AWS Personal Health Dashboard provides alerts and remediation guidance when AWS is experiencing events that may impact you. While the Service Health Dashboard displays the general status of AWS services, Personal Health Dashboard gives you a personalized view into the performance and availability of the AWS services underlying your AWS resources.

User-specific view on the availabiltiy and performace of AWS services, underlying their AWS resources

A service that prompts the user with alerts and notifications on AWS scheduled activities, pending issues, and planned changes.


## AWS CloudWatch

Amazon CloudWatch is basically a metrics repository. An AWS service "" such as Amazon EC2 "" puts metrics into the repository, and you retrieve statistics based on those metrics. If you put your own custom metrics into the repository, you can retrieve statistics on these metrics as well.

## AWS Support Plans

**Developer**
* Recommended if you are experimenting or testing in AWS.
* Pricing: > 29$ month or 3% of monthly AWS usage
* Response times: General Guidance < 24 business hours; System impaired < 12 business hours

**Business**
* Recommended if you have production workloads in AWS.
* Pricing: > 100$ month or 10% month (0$-10K$); 7% month ($10K-$80K); 5% month ($80K - $250K); 3% month (>$250K)
* Response times: General guidance < 24h; System impaired < 12h; Production system impaired < 4h; Production system down < 1h
* Minimum support plan level that provide users with access to the AWS Support API

**Enterprise**
* Recommended if you have business and/or mission critical workloads in AWS.
* Pricing: > $15,000 month or 10% month (0-$150K); 7% month ($150K-$500K); 5% month ($500K - $1M); 3% month (> $1M)
* Response times: General guidance < 24h; System impaired < 12h; Production system impaired < 4h; Production system down < 1h; Business-critical system down < 15 minutes
* It has a designed Technical Account Manager (TAM) that coordinates access to programs and other AWS experts as needed and proactively monitor your environment and assist with optimization.

## AWS Auto Scaling

AWS Auto Scaling monitors your applications and automatically adjusts capacity to maintain steady, predictable performance at the lowest possible cost. Using AWS Auto Scaling, it's easy to setup application scaling for multiple resources across multiple services in minutes. The service provides a simple, powerful user interface that lets you build scaling plans for resources including Amazon EC2 instances and Spot Fleets, Amazon ECS tasks, Amazon DynamoDB tables and indexes, and Amazon Aurora Replicas. AWS Auto Scaling makes scaling simple with recommendations that allow you to optimize performance, costs, or balance between them. If you're already using Amazon EC2 Auto Scaling to dynamically scale your Amazon EC2 instances, you can now combine it with AWS Auto Scaling to scale additional resources for other AWS services. With AWS Auto Scaling, your applications always have the right resources at the right time.

## AWS Cost and Usage report

The Cost & Usage Report is your one-stop-shop for accessing the most granular data about your AWS costs and usage. You can also load your cost and usage information into Amazon Athena, Amazon Redshift, AWS QuickSight, or a tool of your choice.

## AWS Total Cost of Ownership (TCO) Calculator

AWS TCO calculators allow you to estimate the cost savings when using AWS and provide a detailed set of reports that can be used in executive presentations.

## AWS Storage Gateway

AWS Storage Gateway is a hybrid cloud storage service that gives you on-premises access to virtually unlimited cloud storage. Customers use Storage Gateway to simplify storage management and reduce costs for key hybrid cloud storage use cases. These include moving tape backups to the cloud, reducing on-premises storage with cloud-backed file shares, providing low latency access to data in AWS for on-premises applications, as well as various migration, archiving, processing, and disaster recovery use case.

AWS Storage Gateway offers the following three virtual machine types for different use cases:
* File gateways:  lets you use the Network File System (NFS) and Server Message Block (SMB) protocols to store data in Amazon S3. Although data is stored on S3, it’s cached locally, allowing for low-latency access. A file gateway can function as a normal on-premises file server. Because data is stored in S3, you can take advantage of all S3 features including versioning, bucket policies, life cycle management, encryption, and cross-region replication
* Volume gateways: Volume gateways offer S3-backed storage volumes that your on-premises servers can use via the Internet Small Computer System Interface (iSCSI) protocol.
* Tape gateways offer access via the iSCSI block storage protocol, but tape gateways are specifically designed to work with common backup applications.

## AWS Inspector

Amazon Inspector is an automated security assessment service that helps improve the security and compliance of applications deployed on AWS. Amazon Inspector automatically assesses applications for exposure, vulnerabilities, and deviations from best practices. After performing an assessment, Amazon Inspector produces a detailed list of security findings prioritized by level of severity. These findings can be reviewed directly or as part of detailed assessment reports which are available via the Amazon Inspector console or API.

## AWS Macie

Amazon Macie is a security service that uses machine learning to automatically discover, classify, and protect sensitive data in AWS. Macie recognizes sensitive data such as personally identifiable information (PII) or intellectual property. It provides you with dashboards and alerts that give visibility into how this data is being accessed or moved.

## AWS Service Catalog

AWS Service Catalog Delivery Partners are APN Consulting Partners who help create catalogs of IT services that are approved by the customer's organization for use on AWS. With AWS Service Catalog, customers and partners can centrally manage commonly deployed IT services to help achieve consistent governance and meet compliance requirements while enabling users to self-provision approved services.

## AWS ElastiCache

Amazon ElastiCache for Redis is a great choice for implementing a highly available, distributed, and secure in-memory cache to decrease access latency, increase throughput, and ease the load off your relational or NoSQL databases and applications. ElastiCache can serve frequently requested items at sub- millisecond response times, and enables you to easily scale for higher loads without growing the costlier backend databases. Database query results caching, persistent session caching, and full-page caching are all popular examples of caching with ElastiCache for Redis.

## AWS Athena

Amazon Athena is defined as "an interactive query service that makes it easy to analyse data directly in Amazon Simple Storage Service (Amazon S3) using standard SQL." So, it's another SQL query engine for large data sets stored in S3. This is very similar to other SQL query engines, such as Apache Drill. But unlike Apache Drill, Athena is limited to data only from Amazon's own S3 storage service. However, Athena is able to query a variety of file formats, including, but not limited to CSV, Parquet, JSON, etc. 

## AWS VPC

Amazon Virtual Private Cloud (Amazon VPC) lets you provision a logically isolated section of the AWS Cloud where you can launch AWS resources in a virtual network that you define. You have complete control over your virtual networking environment, including selection of your own IP address range, creation of subnets, and configuration of route tables and network gateways. You can use both IPv4 and IPv6 in your VPC for secure and easy access to resources and applications.

You can easily customize the network configuration for your Amazon VPC. For example, you can create a public-facing subnet for your web servers that has access to the Internet, and place your backend systems such as databases or application servers in a private-facing subnet with no Internet access. You can leverage multiple layers of security, including security groups and network access control lists, to help control access to Amazon EC2 instances in each subnet.

From the Dashboard you can configure security groups and subnets. You can have configured subnets and endpoints within the VPC section of AWS management console.

VPC Flow Logs is a feature that enables you to capture information about the IP traffic going to and from network interfaces in your VPC. Flow log data can be published to Amazon CloudWatch Logs or Amazon S3. After you've created a flow log, you can retrieve and view its data in the chosen destination.

VPC Peering can be established between VPCs in different AWS Regions and in separate AWS accounts. The logical networks still use the same common AWS backbone network infrastructure to communicate. By utilizing this infrastructure, VPC Peering makes it possible to securely store mission-critical data to geographically distinct locations for fault-tolerance, disaster recovery and redundancy.

## APN Consulting Partners

APN Consulting Partners are professional services firms that help customers of all sizes design, architect, build, migrate, and manage their workloads and applications on AWS. Consulting Partners include System Integrators (SIs), Strategic Consultancies, Agencies, Managed Service Providers (MSPs), and Value-Added Resellers (VARs).

## AWS Quick Start

Quick Starts are built by AWS solutions architects and partners to help you deploy popular technologies on AWS, based on AWS best practices for security and high availability. These accelerators reduce hundreds of manual procedures into just a few steps, so you can build your production environment quickly and start using it immediately.

## AWS Lambda

AWS provides a set of fully managed services that you can use to build and run serverless applications. Serverless applications don't require provisioning, maintaining, and administering servers for backend components such as compute, databases, storage, stream processing, message queueing, and more. You also no longer need to worry about ensuring application fault tolerance and availability. Instead, AWS handles all of these capabilities for you.

AWS Lambda is charging its users by the number of requests for their functions and by the duration, which is the time the code needs to execute.

## AWS Directory Service

Single sign-on only works when used on a computer that is joined to the AWS Directory Service directory. It cannot be used on computers that are not joined to the directory.

## Availability Zones

Availability Zones are multiple, isolated locations within an AWS Region that are connected by low-latency networks.

## AWS Compliance Program

The AWS Compliance Program helps customers to understand the robust controls in place at AWS to maintain security and compliance in the cloud.

## AWS Security Groups

AWS Security Groups act like a firewall for your Amazon EC2 instances controlling both inbound and outbound traffic. When you launch an instance on Amazon EC2, you need to assign it to a particular security group. After that, you can set up ports and protocols, which remain open for users and computers over the internet.

AWS Security Groups are very flexible. You can use the default security group and still customize it according to your liking (although we don't recommend this practice because groups should be named according to their purpose.) Or you can create a security group that you want for your specific applications. To do this, you can write the corresponding code or use the Amazon EC2 console to make the process easier.

## AWS Cost Explorer

Cost Explorer to forecast cost based on historical data. AWS Cost Explorer has an easy-to-use interface that lets you visualize, understand, and manage your AWS costs and usage over time.

## AWS Budget

AWS Budgets gives you the ability to set custom budgets that alert you when your costs or usage exceed (or are forecasted to exceed) your budgeted amount. You can also use AWS Budgets to set RI utilization or coverage targets and receive alerts when your utilization drops below the threshold you define. RI alerts support Amazon EC2, Amazon RDS, Amazon Redshift, and Amazon ElastiCache reservations.

## AWS Cost & Usage reports

The AWS Cost & Usage Report is a single location for accessing comprehensive information about your AWS costs and usage. The AWS Cost & Usage Report lists AWS usage for each service category used by an account and its IAM users in hourly or daily line items, as well as any tags that you have activated for cost allocation purposes. You can also customize the AWS Cost & Usage Report to aggregate your usage data to the daily or monthly level.

## Elastic Beanstalk

Service for deploying and scaling web applications and services. To deploy on AWS only not on-prem. 

Upload your code and Elastic Beanstalk automatically handles the deployment, from capacity provisioning, load balancing, auto-scaling to application health monitoring. At the same time, you retain full control over the AWS resources powering your application and can access the underlying resources at any time.

It bills per resources consumed.

## CodeCommit

Fully-managed source control service that hosts secure Git-based repositories

## Data Pipeline

Web service that helps you reliably process and move data between different AWS compute and storage services, as well as on-premises data sources

## CodePipeline

Fully managed continuous delivery service that helps you automate your release pipelines for fast and reliable application and infrastructure updates

## AWS KMS

AWS Key Management Service (AWS KMS) is a managed service that makes it easy for you to create and control customer master keys (CMKs), the encryption keys used to encrypt your data.

## AWS CloudHSM

AWS CloudHSM is a cloud-based hardware security module (HSM) that enables you to easily generate and use your own encryption keys on the AWS Cloud.

The AWS CloudHSM service helps you meet corporate, contractual, and regulatory compliance requirements for data security by using dedicated Hardware Security Module (HSM) instances within the AWS cloud. AWS and AWS Marketplace partners offer a variety of solutions for protecting sensitive data within the AWS platform, but for some applications and data subject to contractual or regulatory mandates for managing cryptographic keys, additional protection may be necessary. CloudHSM complements existing data protection solutions and allows you to protect your encryption keys within HSMs that are designed and validated to government standards for secure key management. CloudHSM allows you to securely generate, store, and manage cryptographic keys used for data encryption in a way that keys are accessible only by you.

## AWS Global Accelerator

AWS Global Accelerator uses the AWS global network to optimize the path from your users to your applications, improving the performance of your traffic by as much as 60%. AWS Global Accelerator continually monitors the health of your application endpoints and redirects traffic to healthy endpoints in less than 30 seconds.

## AWS Shield

AWS Shield is a managed Distributed Denial of Service (DDoS) protection service that safeguards applications running on AWS. AWS Shield provides always-on detection and automatic inline mitigations that minimize application downtime and latency, so there is no need to engage AWS Support to benefit from DDoS protection. There are two tiers of AWS Shield - Standard and Advanced.

AWS Shield Standard provides protection for all AWS customers from common, most frequently occurring network and transport layer DDoS attacks that target your web site or application at no additional charge.

## AWS EC2 Auto Scaling

They automatically add or replace instances across multiple Availability Zones when the application needs it. 

## AWS Opswork

AWS OpsWorks is a configuration management service that provides managed instances of Chef and Puppet. ... OpsWorks lets you use Chef and Puppet to automate how servers are configured, deployed, and managed across your Amazon EC2 instances or on-premises compute environments.

## AWS WAF

AWS WAF is a web application firewall that helps protect web applications from common web exploits that could affect application availability, compromise security, or consume excessive resources. You can use AWS WAF to define customizable web security rules that control which traffic accesses your web applications. If you use AWS Shield Advanced, you can use AWS WAF at no extra cost for those protected resources and can engage the DRT to create WAF rules.

## Amazon Machine Images (AMI)

An image is a software bundle that was built from a template definition and made available within a single AWS Region. AMIs are organized into:
* Quick Start 
* Custom AMIs
* AWS Marketplace
* Community AMIs

## Amazon Lightsail

It is a managed service that offers blueprints that will automatically provision all the compute, storage, database, and network resources needed to make your deployment work. You can select from the following list:
* OS: Amazon Linux, Ubuntu, Debian, FreeBSD, OpenSUSE, and Windows Server
* Applications: WordPress, Magento, Drupal, Joomla, Redmine, and Plesk
* Stacks: Node.js, Gitlab, LAMP, MEAN, and Ngnix

It bills at a flat rate per month.

## AWS System Manager

AWS Systems Manager gives you visibility and control of your infrastructure on AWS. Systems Manager provides a unified user interface so you can view operational data from multiple AWS services and allows you to automate operational tasks across your AWS resources.

## AWS EMR

Amazon Elastic Map Reduce (EMR) provides a managed Hadoop framework that makes it easy, fast, and cost-effective to process vast amounts of data across dynamically scalable Amazon EC2 instance.

## AWS Glue

AWS Glue is a fully managed extract, transform, and load (ETL) service that makes it easy for customers to prepare and load their data for analytics. You can create and run an ETL job with a few clicks in the AWS Management Console.

## Amazon SWF

Amazon Simple Workflow (Amazon SWF) helps developers build, run, and scale background jobs that have parallel or sequential steps. You can think of Amazon SWF as a fully-managed state tracker and task coordinator in the cloud

## Amazon Polly

It is an AWS service that turn text into life-like speech.

## AWS Control Tower

Control Tower automates the process of setting up a new baseline multi-account AWS environment that is secure, well-architected, and ready to use. Control Tower incorporates the knowledge that AWS Professional Service has gained over the course of thousands of successful customer engagements.

## AWS Transit Gateway

Allows a user to easily scale connectivity among thousands of VPCs

## Amazon Elastic Container Service (Amazon ECS)

Helps users install, operate, and scale the cluster management infrastructure

