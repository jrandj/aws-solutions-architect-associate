# Exam SAA-C03

- [Design Secure Architectures](#Design-Secure-Architectures)
- [Design Resilient Architectures](#Design-Resilient-Architectures)
- [Design High-Performing Architectures](#Design-High-Performing-Architectures)
- [Design Cost-Optimized Architectures](#Design-Cost-Optimized-Architectures)
- [Appendix](#Appendix)

## Design Secure Architectures

### Task Statement 1: Design secure access to AWS resources.

#### Knowledge of:

1. Access controls and management across multiple accounts.

    * AWS organizations is an account management service that enables you to consolidate multiple AWS accounts into an organization that you create and centrally manage.

    * Always enable multi-factor authentication on the root account. Always use a strong and complex password on the root account. The paying account should be used for billing purposes only. Do not deploy resources into the paying account. Enable/Disable AWS services using Service Control Policies (SCP) either on the OU or on individual accounts.

1. AWS federated access and identity services (for example, AWS Identity and Access Management [IAM], AWS Single Sign-On [AWS SSO]).

	* AWS IAM Identity Center makes it easy to centrally manage federated access to multiple AWS accounts and business applications and provide users with single sign-on access to all their assigned accounts and applications from one place.

	* AWS IAM Identity Center works with an IdP of your choice, such as Okta Universal Directory or Azure Active Directory (AD) via the Security Assertion Markup Language 2.0 (SAML 2.0) protocol.

1. AWS global infrastructure (for example, Availability Zones, AWS Regions).

	* A Region is a location. An Availability Zone is a Data Center. An Availability Zone may contain several Data Centres that are close to each other (within 100 km).

	* Edge locations are endpoints for AWS that are used for caching content. THere are many more edge locations than regions.

1. AWS security best practices (for example, the principle of least privilege).

	* Only assign a user the minimum amount of privileges they need to do their job.

1. The AWS shared responsibility model.

	* AWS are responsibile for security of the Cloud. The customer is responsibile for the security in the Cloud. If you can do it in the AWS Management Console you are generally responsible for it. Encryption is a shared responsibility.

#### Skills in:

1. Applying AWS security best practices to IAM users and root users (for example, multi-factor authentication [MFA]).

1. Designing a flexible authorization model that includes IAM users, groups, roles, and policies.

	* Permissions are assigned using IAM policy documents (consisting of JSON). A user is a physical person, a group is a function such as administrator and contains users, and roles are used internally within AWS to allow acccess from one service to another. A permission should be assigned to a group and then users inherit the permissions of the groups they are assigned. An explicit deny will always overwrite an allow.

1. Designing a role-based access control strategy (for example, AWS Security Token Service [AWS STS], role switching, cross-account access).

1. Designing a security strategy for multiple AWS accounts (for example, AWS Control Tower, service control policies [SCPs]).

1. Determining the appropriate use of resource policies for AWS services.

1. Determining when to federate a directory service with IAM roles.

### Task Statement 2: Design secure workloads and applications.

#### Knowledge of:

1. Application configuration and credentials security.

1. AWS service endpoints.

1. Control ports, protocols, and network traffic on AWS.

1. Secure application access.

1. Security services with appropriate use cases (for example, Amazon Cognito, Amazon GuardDuty, Amazon Macie).

1. Threat vectors external to AWS (for example, DDoS, SQL injection).

#### Skills in:

1. Designing VPC architectures with security components (for example, security groups, route tables, network ACLs, NAT gateways).

1. Determining network segmentation strategies (for example, using public subnets and private subnets).

1. Integrating AWS services to secure applications (for example, AWS Shield, AWS WAF, AWS SSO, AWS Secrets Manager).

1. Securing external network connections to and from the AWS Cloud (for example, VPN, AWS Direct Connect).

### Task Statement 3: Determine appropriate data security controls.

#### Knowledge of:

1. Data access and governance.

1. Data recovery.

1. Data retention and classification.

1. Encryption and appropriate key management.

#### Skills in:

1. Aligning AWS technologies to meet compliance requirements.

1. Encrypting data at rest (for example, AWS Key Management Service [AWS KMS]).

1. Encrypting data in transit (for example, AWS Certificate Manager [ACM] using TLS).

1. Implementing access policies for encryption keys.

1. Implementing data backups and replications.

1. Implementing policies for data access, lifecycle, and protection.

1. Rotating encryption keys and renewing certificates.

## Design Resilient Architectures

### Task Statement 1: Design scalable and loosely coupled architectures

#### Knowledge of:

1. API creation and management (for example, Amazon API Gateway, REST API).

1. AWS managed services with appropriate use cases (for example, AWS Transfer Family, Amazon Simple Queue Service [Amazon SQS], Secrets Manager).

1. Caching strategies.

1. Design principles for microservices (for example, stateless workloads compared with stateful workloads).

1. Event-driven architectures.

1. Horizontal scaling and vertical scaling.

1. How to appropriately use edge accelerators (for example, content delivery network [CDN]).

1. How to migrate applications into containers.

1. Load balancing concepts (for example, Application Load Balancer).

1. Multi-tier architectures.

1. Queuing and messaging concepts (for example, publish/subscribe).

1. Serverless technologies and patterns (for example, AWS Fargate, AWS Lambda).

1. Storage types with associated characteristics (for example, object, file, block).

1. The orchestration of containers (for example, Amazon Elastic Container Service [Amazon ECS], Amazon Elastic Kubernetes Service [Amazon EKS]).

1. When to use read replicas.

	* RDS Read replicas are for scaling read performance and not for disaster recovery. Key facts include:
		* A read replica can be cross-AZ and cross-region.
		* Each read replica has its own DNS endpoint.
		* Read replicas require automatic backup to be enabled.
		* Read replicas can be promoted to be their own database. This breaks the replication.

1. Workflow orchestration (for example, AWS Step Functions).

#### Skills in:

1. Designing event-driven, microservice, and/or multi-tier architectures based on requirements.

1. Determining scaling strategies for components used in an architecture design.

1. Determining the AWS services required to achieve loose coupling based on requirements.

1. Determining when to use containers.

1. Determining when to use serverless technologies and patterns.

1. Recommending appropriate compute, storage, networking, and database technologies based on requirements.

1. Using purpose-built AWS services for workloads.

### Task Statement 2: Design highly available and/or fault-tolerant architectures.

#### Knowledge of:

1. AWS global infrastructure (for example, Availability Zones, AWS Regions, Amazon Route 53).

    * A Region is a physical location in the world which consists of two or more Availability Zones (AZ's).

    * An AZ is one or more discrete data centres, each with redundant power, networking and connectivity, housed in separate facilities.

    * Edge Locations are endpoints for AWS which are used for caching content. Typically, this consists of CloudFront, Amazon's Content Delivery Network (CDN).

1. AWS managed services with appropriate use cases (for example, Amazon Comprehend,
Amazon Polly).

1. Basic networking concepts (for example, route tables).

1. Disaster recovery (DR) strategies (for example, backup and restore, pilot light, warm standby, active-active failover, recovery point objective [RPO], recovery time objective [RTO]).

1. Distributed design patterns.

1. Failover strategies.

1. Immutable infrastructure.

1. Load balancing concepts (for example, Application Load Balancer).

1. Proxy concepts (for example, Amazon RDS Proxy).

1. Service quotas and throttling (for example, how to configure the service quotas for a workload in a standby environment).

1. Storage options and characteristics (for example, durability, replication).

1. Workload visibility (for example, AWS X-Ray).

#### Skills in:

1. Determining automation strategies to ensure infrastructure integrity.

1. Determining the AWS services required to provide a highly available and/or fault-tolerant architecture across AWS Regions or Availability Zones.

1. Identifying metrics based on business requirements to deliver a highly available solution.

1. Implementing designs to mitigate single points of failure.

1. Implementing strategies to ensure the durability and availability of data (for example, backups).

1. Selecting an appropriate DR strategy to meet business requirements.

1. Using AWS services that improve the reliability of legacy applications and applications not built for the cloud (for example, when application changes are not possible).

1. Using purpose-built AWS services for workloads.

## Design High-Performing Architectures

### Task Statement 1: Determine high-performing and/or scalable storage solutions.

#### Knowledge of:

1. Hybrid storage solutions to meet business requirements.

1. Storage services with appropriate use cases (for example, Amazon S3, Amazon Elastic File System [Amazon EFS], Amazon Elastic Block Store [Amazon EBS]).

1. Storage types with associated characteristics (for example, object, file, block).

#### Skills in:

1. Determining storage services and configurations that meet performance demands.

1. Determining storage services that can scale to accommodate future needs.

### Task Statement 2: Design high-performing and elastic compute solutions.

#### Knowledge of:

1. AWS compute services with appropriate use cases (for example, AWS Batch, Amazon EMR,
Fargate).

1. Distributed computing concepts supported by AWS global infrastructure and edge services.

1. Queuing and messaging concepts (for example, publish/subscribe).

1. Scalability capabilities with appropriate use cases (for example, Amazon EC2 Auto Scaling, AWS Auto Scaling).

1. Serverless technologies and patterns (for example, Lambda, Fargate).

1. The orchestration of containers (for example, Amazon ECS, Amazon EKS).

#### Skills in:

1. Decoupling workloads so that components can scale independently.

1. Identifying metrics and conditions to perform scaling actions.

1. Selecting the appropriate compute options and features (for example, EC2 instance types) to meet business requirements.

1. Selecting the appropriate resource type and size (for example, the amount of Lambda
memory) to meet business requirements.

### Task Statement 3: Determine high-performing database solutions.

#### Knowledge of:

1. AWS global infrastructure (for example, Availability Zones, AWS Regions).

1. Caching strategies and services (for example, Amazon ElastiCache).

1. Data access patterns (for example, read-intensive compared with write-intensive).

1. Database capacity planning (for example, capacity units, instance types, Provisioned IOPS).

1. Database connections and proxies.

1. Database engines with appropriate use cases (for example, heterogeneous migrations, homogeneous migrations).

	* ACID stands for Atomic, Consistent, Isolated, and Durable:
		* **Atomic:** All changes to data must be performed successfully or not at all.
		* **Consistent:** Data must be in a consistent state before and after the transaction.
		* **Isolated:** No other process can change the data while the transaction is running.
		* **Durable:** The changes made by a transaction must persist. 

1. Database replication (for example, read replicas).

1. Database types and services (for example, serverless, relational compared with non-relational, in-memory).

#### Skills in:

1. Configuring read replicas to meet business requirements.

1. Designing database architectures.

1. Determining an appropriate database engine (for example, MySQL compared with
PostgreSQL).

1. Determining an appropriate database type (for example, Amazon Aurora, Amazon DynamoDB).

1. Integrating caching to meet business requirements.

### Task Statement 4: Determine high-performing and/or scalable network architectures.

#### Knowledge of:

1. Edge networking services with appropriate use cases (for example, Amazon CloudFront, AWS Global Accelerator).

1. How to design network architecture (for example, subnet tiers, routing, IP addressing).

1. Load balancing concepts (for example, Application Load Balancer).

1. Network connection options (for example, AWS VPN, Direct Connect, AWS PrivateLink).

#### Skills in:

1. Creating a network topology for various architectures (for example, global, hybrid, multi-tier).

1. Determining network configurations that can scale to accommodate future needs.

1. Determining the appropriate placement of resources to meet business requirements.

1. Selecting the appropriate load balancing strategy.

### Task Statement 5: Determine high-performing data ingestion and transformation solutions.

#### Knowledge of:

1. Data analytics and visualization services with appropriate use cases (for example, Amazon Athena, AWS Lake Formation, Amazon QuickSight).

1. Data ingestion patterns (for example, frequency).

1. Data transfer services with appropriate use cases (for example, AWS DataSync, AWS Storage Gateway).

    * AWS DataSync automatically encrypts data and accelerates transfer over the WAN. Datasync performs automatic data integrity checks in-transit and at-rest.

    * It is used to move large amounts of data from on-premises to AWS. It is used with NFS and SMB compatible file systems. The replication can be done hourly, daily, or weekly. The DataSync agent is required to start the replication. It can be used to replicate EFS to EFS.

1. Data transformation services with appropriate use cases (for example, AWS Glue).

1. Secure access to ingestion access points.

1. Sizes and speeds needed to meet business requirements.

1. Streaming data services with appropriate use cases (for example, Amazon Kinesis).

#### Skills in:

1. Building and securing data lakes.

1. Designing data streaming architectures.

1. Designing data transfer solutions.

1. Implementing visualization strategies.

1. Selecting appropriate compute options for data processing (for example, Amazon EMR).

1. Selecting appropriate configurations for ingestion.

1. Transforming data between formats (for example, .csv to .parquet).

## Design Cost-Optimized Architectures

### Task Statement 1: Design cost-optimized storage solutions.

#### Knowledge of:

1. Access options (for example, an S3 bucket with Requester Pays object storage).

1. AWS cost management service features (for example, cost allocation tags, multi-account billing).

1. AWS cost management tools with appropriate use cases (for example, AWS Cost Explorer, AWS Budgets, AWS Cost and Usage Report).

1. AWS storage services with appropriate use cases (for example, Amazon FSx, Amazon EFS, Amazon S3, Amazon EBS).

1. Backup strategies.

1. Block storage options (for example, hard disk drive [HDD] volume types, solid state drive [SSD] volume types).

1. Data lifecycles.

1. Hybrid storage options (for example, DataSync, Transfer Family, Storage Gateway).

1. Storage access patterns.

1. Storage tiering (for example, cold tiering for object storage).

1. Storage types with associated characteristics (for example, object, file, block).

#### Skills in:

1. Designing appropriate storage strategies (for example, batch uploads to Amazon S3 compared with individual uploads).

1. Determining the correct storage size for a workload.

1. Determining the lowest cost method of transferring data for a workload to AWS storage.

1. Determining when storage auto scaling is required.

1. Managing S3 object lifecycles.

1. Selecting the appropriate backup and/or archival solution.

1. Selecting the appropriate service for data migration to storage services.

1. Selecting the appropriate storage tier.

1. Selecting the correct data lifecycle for storage.

1. Selecting the most cost-effective storage service for a workload.

    * S3 pricing for US East (N. Virginia) is shown below:
        <p align="center">
        <img src="/res/storage_pricing.JPG">
        </p>

### Task Statement 2: Design cost-optimized compute solutions.

#### Knowledge of:

1. AWS cost management service features (for example, cost allocation tags, multi-account billing).

1. AWS cost management tools with appropriate use cases (for example, Cost Explorer, AWS Budgets, AWS Cost and Usage Report).

1. AWS global infrastructure (for example, Availability Zones, AWS Regions)

1. AWS purchasing options (for example, Spot Instances, Reserved Instances, Savings Plans)

1. Distributed compute strategies (for example, edge processing)

1. Hybrid compute options (for example, AWS Outposts, AWS Snowball Edge)

	* Snowball is a petabyte-scale data transport solution that uses secure appliances to transfer large amounts of data into and out of AWS. Using Snowball addresses common challenges with large-scale data transfers including high network costs, long transfer times, and security concerns. Transferring data with Snowball is simple, fast, secure, and can be as little as one-fifth the cost of high-speed internet.

    * Snowball comes in either a 50 TB or 80 TB size. Security controls include 256-bit encryption, and an industry-standard Trusted Platform Module (TPM) designed to ensure both security and full chain-of-custody of your data. Once the data job has been processed and verified, AWS performs a software erasure of the Snowball appliance.

    * AWS Snowball Edge is a 100 TB data transfer device with on-board storage and compute capabilities. You can use it to move large amounts of data into and out of AWS, as a temporary storage tier for large local datasets, or to support local workloads in remote or offline locations. Snowball Edge can cluster together to form a local storage tier and process your data on-premises, helping ensure your applications continue to run even when they are not able to access the cloud.

    * AWS Snowmobile is an Exabyte-scale data transfer service used to move extremely large amounts of data to AWS. You can transfer up to 100 PB per Snowmobile, a 45-foot long ruggedised shipping container, pulled by a semi-trailer truck. Snowmobile makes it easy to move massive volumes of data to the cloud, including video libraries, image repositories, or even a complete data centre migration.

    * A summary of when to consider Snowball is shown below:
        <p align="center">
        <img src="/res/snowball_use_case.JPG">
        </p>

1. Instance types, families, and sizes (for example, memory optimized, compute optimized, virtualization)

1. Optimization of compute utilization (for example, containers, serverless computing,
microservices)

1. Scaling strategies (for example, auto scaling, hibernation)

#### Skills in:

1. Determining an appropriate load balancing strategy (for example, Application Load Balancer [Layer 7] compared with Network Load Balancer [Layer 4] compared with Gateway Load Balancer).

1. Determining appropriate scaling methods and strategies for elastic workloads (for example, horizontal compared with vertical, EC2 hibernation).

1. Determining cost-effective AWS compute services with appropriate use cases (for example, Lambda, Amazon EC2, Fargate).

1. Determining the required availability for different classes of workloads (for example, production workloads, non-production workloads).

1. Selecting the appropriate instance family for a workload.

1. Selecting the appropriate instance size for a workload.

### Task Statement 3: Design cost-optimized database solutions.

#### Knowledge of:

1. AWS cost management service features (for example, cost allocation tags, multi-account billing).

1. AWS cost management tools with appropriate use cases (for example, Cost Explorer, AWS Budgets, AWS Cost and Usage Report).

1. Caching strategies.

1. Data retention policies.

1. Database capacity planning (for example, capacity units).

1. Database connections and proxies.

1. Database engines with appropriate use cases (for example, heterogeneous migrations,
homogeneous migrations).

1. Database replication (for example, read replicas).

1. Database types and services (for example, relational compared with non-relational, Aurora, DynamoDB).

#### Skills in:

1. Designing appropriate backup and retention policies (for example, snapshot frequency).

1. Determining an appropriate database engine (for example, MySQL compared with
PostgreSQL).

1. Determining cost-effective AWS database services with appropriate use cases (for example, DynamoDB compared with Amazon RDS, serverless).

1. Determining cost-effective AWS database types (for example, time series format, columnar format).

1. Migrating database schemas and data to different locations and/or different database engines.

### Task Statement 4: Design cost-optimized network architectures.

#### Knowledge of:

1. AWS cost management service features (for example, cost allocation tags, multi-account billing).

1. AWS cost management tools with appropriate use cases (for example, Cost Explorer, AWS Budgets, AWS Cost and Usage Report).

1. Load balancing concepts (for example, Application Load Balancer).

1. NAT gateways (for example, NAT instance costs compared with NAT gateway costs).

1. Network connectivity (for example, private lines, dedicated lines, VPNs).

1. Network routing, topology, and peering (for example, AWS Transit Gateway, VPC peering).

	* VPC Peering allows you to connect 1 VPC with another via a direct network route using private IP addresses.

	* Instances behave as if they were on the same private network.

	* You can peer VPCs with other AWS accounts as well as with other VPCs in the same account.

	* Peering is in a star configuration (i.e. 1 central VPC peer with 4 others). There is no transitive peering.

	* You can peer between regions.

1. Network services with appropriate use cases (for example, DNS).

#### Skills in:

1. Configuring appropriate NAT gateway types for a network (for example, a single shared NAT gateway compared with NAT gateways for each Availability Zone).

1. Configuring appropriate network connections (for example, Direct Connect compared with VPN compared with internet).

1. Configuring appropriate network routes to minimize network transfer costs (for example, Region to Region, Availability Zone to Availability Zone, private to public, Global Accelerator, VPC endpoints).

	* VPC Endpoints are used when you want to connect AWS services without leaving the Amazon internal network. Interface endpoints and gateway endpoints (S3 and DynamoDB).

1. Determining strategic needs for content delivery networks (CDNs) and edge caching.

1. Reviewing existing workloads for network optimizations.

1. Selecting an appropriate throttling strategy.
 
1. Selecting the appropriate bandwidth allocation for a network device (for example, a single VPN compared with multiple VPNs, Direct Connect speed).

## Appendix

### Key Technologies and Concepts

1. Compute.

1. Cost management.

1. Database.

1. Disaster recovery.

1. High performance.

1. Management and governance.

1. Microservices and component decoupling.

1. Migration and data transfer.

1. Networking, connectivity, and content delivery.

1. Resiliency.

1. Security.

1. Serverless and event-driven design principles.

1. Storage.

### AWS Services and Features

#### Analytics

1. Amazon Athena.

    * Amazon Athena is an interactive query service which enables you to analyse and query data located in S3 using standard SQL.

    * Athena is serverless and you pay per query. There is no need to setup complex Extract/Transform/Load (ETL) processes, and it works directly with data stored in S3.

    * Athena can be used to query log files stored in S3. It can also be used to generate business reports on data stored in S3.

1. AWS Data Exchange.

1. AWS Data Pipeline.

1. Amazon EMR.

1. AWS Glue.

1. Amazon Kinesis.

1. AWS Lake Formation.

1. Amazon Managed Streaming for Apache Kafka (Amazon MSK).

1. Amazon OpenSearch Service (Amazon Elasticsearch Service).

1. Amazon QuickSight.

1. Amazon Redshift.

#### Application Integration

1. Amazon AppFlow.

1. AWS AppSync.

1. Amazon EventBridge (Amazon CloudWatch Events).

1. Amazon MQ.

1. Amazon Simple Notification Service (Amazon SNS).

1. Amazon Simple Queue Service (Amazon SQS).

1. AWS Step Functions.

#### AWS Cost Management

1. AWS Budgets.

1. AWS Cost and Usage Report.

1. AWS Cost Explorer.

1. Savings Plans.

#### Compute

1. AWS Batch.

1. Amazon EC2.

	* Elastic Compute Cloud (EC2) is a web service that provides resizable compute capacity in the cloud. It is designed to make web-scale computing easier for developers. It reduces the time required to obtain and boot new server instances to minutes.

    * The following pricing types are available with EC2:
        * **On Demand:** Allows you to pay a fixed rate by the hour (or by the second) with no commitment.
        * **Reserved:** Provides you with a capacity reservation, and offers a significant discount on the hourly charge for an instance. Contract terms are 1 year or 3 year terms. Up to a 72% discount on the hourly charge.
        * **Spot:** Enables you to bid whatever price you want for instance capacity, providing for even greater savings if your applications have flexible start and end times. If your instance is terminated by Amazon, you will not be charged for a partial hour of usage. However, if you terminate the instance yourself, you will be changed for any hour in which the instance ran. Up to a 90% discount.
        * **Dedicated Hosts:** Physical EC2 server dedicated for your use. Helps reduce your costs by allowing you to use your existing server-bound software licenses.

    * Spot instances save up to 90% of the cost of on-demand instances. They are useful for any type of computing where you don't need persistent storage. A spot fleet is a collection of spot instances and, optionally, on-demand instances. You can block spot instances from terminating by using spot block.

    * Termination protection is turned off by default, it must be turned on. On an EBS-backed instance, the default action is for the root EBS volume to be deleted when the instance is terminated. However, other volumes will not be deleted by default. EBS root volumes and additional volumes can be encrypted. You can also use a third party tool (such as bitlocker) to encrypt the root volume, or this can be done when creating AMI's.

    * Regarding Security Groups:
        * All inbound traffic is blocked by default.
        * All outbound traffic is allowed.
        * Changes to Security Groups take effect immediately
        * You can have any number of EC2 instances within a security group.
        * You can have multiple security groups attached to EC2 instances.
        * Security Groups are stateful.
        * If you create an inbound rule allowing traffic in, that traffic is automatically allowed back out again.
        * You cannot block specific IP addresses using Security Groups, instead use Network Access Control Lists.
        * You can specify allow rules, but not deny rules.

    * Regarding network devices available in EC2:
        * **Elastic Network Interface (ENI):** A virtual network card. Used for basic networking. If you need a separate networks for production and logging, you can use multiple ENIs for each network.
        * **Enhanced Networking (EN):** Uses single root I/O virtualisation (SR-IOV) to provide high-performance networking capabilities on supported instance types. Used for when you need speeds between 10 Gbps and 100 Gbps. This is for reliable, high throughput.
        * **Elastic Fabric Adapter:** A network device that you can attach to your Amazon EC2 instance to accelerate High Performance Computing (HPC) and machine learning applications. Used for when you need to accelerate High Performance Computing (HPC) and machine learning applications, or you need to do an OS bypass.

    * Regarding EC2 Hibernate:
        * Hibernate preserves in-memory RAM on persistent storage (EBS). It is faster to boot because you do not need to reload the operating system.
        * Instance RAM must be less than 150 GB.
        * Instance families include C3, C4, C5, M3, M4, M5, R3, R4 and R5.
        * Hibernate is available for Windows, Amazon Linux 2 AMI, and Ubuntu.
        * Hibernate is available for on-demand instances and reserved instances.
        * Instances can't be hibernated for more than 60 days.

    * Roles are far more secure than storing your access key and secret access key on individual EC2 instances (in the .aws directory). Roles are easier to manage. Roles can be assigned to an EC2 instance after it is created using both the console and command line. Roles are universal, you can use them in any region.

	* A bootstrap script runs with administrator privileges on EC2 instance startup. It is configured in the "User data" section on instance creation.

    * Metadata can be queried to get information about an instance:
        ```shell
        curl http://<ip>/latest/meta-data/
        curl http://<ip>/latest/user-data/
        ```

    * EC2 instances can be grouped in different placement groups:
        * **Clustered Placement Group:** For low latency and high network throughput, instances are colocated in the same AZ.
        * **Spread Placement Group:** For critical EC2 instances where you want each instance on separate pieces of hardware. Can span multiple AZs.
        * **Partitioned Placement Group:** As for Spread Placement Group but you can have multiple instances for each piece of hardware. Can span multiple AZs.

    * A placement group name must be unique within your AWS account. Only certain types of instances can be launched in a placement group. AWS recommends homogenous instances within clustered placement groups. Placement groups cannot be merged, but instances can be moved into a placement group if it is in a stopped state. The move can currently only be done with the AWS CLI or an AWS SDK, the console does not support it.

1. Amazon EC2 Auto Scaling.

1. AWS Elastic Beanstalk.

1. AWS Outposts.

1. AWS Serverless Application Repository.

1. VMware Cloud on AWS.

1. AWS Wavelength.

#### Containers

1. Amazon Elastic Container Registry (Amazon ECR).

1. Amazon Elastic Container Service (Amazon ECS).

1. Amazon ECS Anywhere.

1. Amazon Elastic Kubernetes Service (Amazon EKS).

1. Amazon EKS Anywhere.

1. Amazon EKS Distro.

#### Database

1. Amazon Aurora.

	* Aurora is Amazon's proprietary relational database which is MySQL and PostgreSQL-compatible. It has 5x better performance than MySQL and 3x better than PostgresSQL.

	* 2 copies of your data are contained in each AZ, with a minimum of 3 AZs. 6 copies of your data.

	* You can share Aurora snapshots with other AWS accounts.

	* 3 types of replicas available: Aurora replicas, MySQL replicas, and PostgreSQL replicas. Automated failover is only available with Aurora replicas.

	* Aurora has automated backups turned on by default. You can also take snapshots with Aurora. You can share these snapshots with other AWS accounts.

1. Amazon Aurora Serverless.

	* Amazon Aurora Serverless is a serverless database cluster that automatically starts up, shuts down, and scales capacity up or down based on your application's needs.

	* Use Amazon Aurora Serverless if you want a simple, cost-effective option for infrequent, intermittent, or unpredictable workloads.

1. Amazon DocumentDB (with MongoDB compatibility).

1. Amazon DynamoDB.

	* Amazon DynamoDB is a fast and flexible non-relational database service for any scale. DynamoDB enables customers to offload the administrative burdens of operating and scaling distributed databases to AWS so that they don’t have to worry about hardware provisioning, setup and configuration, throughput capacity planning, replication, software patching, or cluster scaling.

	* Key facts about DynamoDB:
		* Stored on SSD.
		* Spread across 3 geographically distinct data centres.
		* Eventually consistent reads (default).
		* Strongly consistent reads.

	* Eventually consistent will achieve consistency within a second. Strongly consistent will achieve consistency instantly.

	* DynamoDB transactions provide developers ACIC properties across 1 or more tables within a single AWS account and region.

	* Point-in-Time Recovery (PITR) can protect against accidental writes or deletes. You can restore to any point in the last 35 days and up to 5 minutes in the past. Not enabled by default.

	* DynamoDB streams provide a time-ordered sequence of item-level changes in a table. Stored for 24 hours. The stream includes events such as inserts, updates, and deletes. Can be combined with Lambda function for functionality like stored procedures.

	* Global Tables provides managed multi-master, multi-region replication. It is based on DynamoDB streams. Replication latency is under 1 second.

1. Amazon ElastiCache.

1. Amazon Keyspaces (for Apache Cassandra).

1. Amazon Neptune.

1. Amazon Quantum Ledger Database (Amazon QLDB).

1. Amazon RDS.

	* RDS is for OLTP (Online Transaction Processing) workloads. This involves small transactions, like customer orders, banking transactions, payments, and booking systems.

	* Online Analytical Processing (OLAP) should use Redshift. This is for tasks such as analyzing large amounts of data, reporting, and sales forecasting.

	* Amazon Relational Database Service (Amazon RDS) is a managed service that makes it easy to set up, operate, and scale a relational database in the cloud. Amazon RDS gives you access to the capabilities of a familiar MySQL, MariaDB, Oracle, SQL Server, or PostgreSQL database.

	* Multi-AZ provides an exact copy of your production database in another AZ. Used for disaster recovery. In the event of a failure, RDS will automatically failover to the standby instance.

1. Amazon Redshift.

1. Amazon Timestream.

#### Developer Tools

1. AWS X-Ray.

#### Front-End Web and Mobile

1. AWS Amplify.

1. Amazon API Gateway.

1. AWS Device Farm.

1. Amazon Pinpoint.

#### Machine Learning

1. Amazon Comprehend.

1. Amazon Forecast.

1. Amazon Fraud Detector.

1. Amazon Kendra.

1. Amazon Lex.

1. Amazon Polly.

1. Amazon Rekognition.

1. Amazon SageMaker.

1. Amazon Textract.

1. Amazon Transcribe.

1. Amazon Translate.

#### Management and Governance

1. AWS Auto Scaling.

1. AWS CloudFormation.

1. AWS CloudTrail.

1. Amazon CloudWatch.

	* CloudWatch monitors your AWS resources and the applications you run on AWS in real time. You can use CloudWatch to collect and track metrics, which are variables you can measure for your resources and applications.

    * The CloudWatch home page automatically displays metrics about every AWS service you use. You can additionally create custom dashboards to display metrics about your custom applications and display custom collections of metrics that you choose. Alarms can also be created to notify you when thresholds are hit.

    * CloudWatch with EC2 will monitor events every 5 minutes by default. you can have 1-minute intervals by turning on detailed monitoring.

    * CloudWatch Events help you to respond to state changes in your AWS resources.
    
    * CloudWatch Logs help you to aggregate, monitor, and store logs.

    * CloudWatch monitors performance. CloudTrail monitors API calls in the AWS platform.

1. AWS Command Line Interface (AWS CLI).

1. AWS Compute Optimizer.

1. AWS Config.

1. AWS Control Tower.

1. AWS License Manager.

1. Amazon Managed Grafana.

1. Amazon Managed Service for Prometheus.

1. AWS Management Console.

1. AWS Organizations.

1. AWS Personal Health 
2. Dashboard.

1. AWS Proton.

1. AWS Service Catalog.

1. AWS Systems Manager.

1. AWS Trusted Advisor.

1. AWS Well-Architected Tool.

#### Media Services

1. Amazon Elastic Transcoder

1. Amazon Kinesis Video Streams

#### Networking and Content Delivery

1. Amazon CloudFront.

	* CloudFront is a Content Delivery Network (CDN) that works in conjunction with other services to provide developers with a simple way to distribute content to end users.

    * This service is useful for companies with a need for higher response times and large file content that want to distribute these files to a sizeable number of users. Once content is put in an origin server, like an Amazon Simple Storage Service bucket or an Elastic Compute Cloud instance, it’s pushed out to multiple CloudFront servers as content is requested.

    * An **Edge Location** is the location where content will be cached. This is separate to an AWS Region or AZ. Edge locations are not just read only, they can be written to as well. Objects are cached for the life of the Time to Live (TTL). Cached objects can be cleared but you will be charged.

    * The **Origin** is the origin of all the files that the CDN will distribute. This can be an S3 Bucket, an EC2 Instance, an Elastic Load Balancer, or Route 53.

    * The **Distribution** is the name given to the CDN which consists of a collection of Edge Locations.

    * A **Web Distribution** is typically for websites and a **RTMP** is used for media streaming.

    * Use signed URLs or cookies when you want to secure content so that only the people you authorise are able to access it. A signed URL is for individual files with 1 file corresponding to 1 URL. A signed cookie is for multiple files with 1 cookie corresponding to multiple files. If your origin is EC2, then use CloudFront. If your origin is S3, then use an S3 signed URL.

1. AWS Direct Connect.

	* Direct Connect directly connects your data centre to AWS. Useful for high-throughput workloads that require a stable and reliable secure connection.

1. Elastic Load Balancing (ELB).

1. AWS Global Accelerator.

1. AWS PrivateLink.

	* AWS PrivateLink enables peering VPCs to tens, hundreds, or thousands of customer VPCs. Does not require VPC peering, route tables, NAT Gateways, Internet Gateways, etc. Requires a Network Load Balance on the service VPC and an Elastic Network Interface (ENI) on the customer VPC.

1. Amazon Route 53.

	* An alias is an AWS concept, and should be choosed over CNAME.

	* Common DNS record types:
		* Start of Authority (SOA) Records. Stores the name of the server that supplied the data for the zone, the admministrator, the current version of thedata, and the default number of seconds for the time-to-live file on resource records.
		* Canonical Name (CNAME). Used to resolve one domain name to another. For example, you may have a mobile website with the domain name http://m.acloud.guru that is used for when users browse to your domain name on their mobile devices.
		* Name Server (NS) Records. Used by top-level domain servers to direct traffic to the content DNS server that contains the authoritative DNS records.
		* A Records. Fundamental type of DNS record. Used to translate the name of the domain to an IP address.
		* Alias Records. Used to map resource record sets in your hosted zone to load balancers, CloudFront distributions, or S3 buckets that are configured as websites. Work like a CNAME record in that you can map one DNS name to another "target" DNS name.

	* Time to Live (TTL) is the length that a DNS record is cached on either the resolving server or the user's own local PC.

	* Routing policies available in Route 53:
		* **Simple Routing:** You can only have one record with multiple IP addresses. If you specify multiple values, Route 53 returns all values to the user in a random order.
		* **Weighted Routing:** Route 53 will send certain percentage of traffic to AZs, regions etc.
		* **Latency-Based Routing:** Route53 will send traffic to the lower latency option.
		* **Failover Routing:** An Active Passive setup which will Failover automatically.
		* **Geolocation Routing:** Traffic will be sent based on the originating location.
		* **Geoproximity Routing (Traffic Flow Only):** Lets Route 53 route traffic to your resources based on the geographic location of your users and resources. You can also optionally choose to route traffic by specifying a value known as a bias. The bias expands or shrinks the size of the geopgraphic region from which traffic is routed to a resource. You must use Route 53 traffic flow.
		* **Multivalue Answer Routing:** Distributes DNS responses across multiple IP addresses.

	* You can buy domain names directly with AWS. It can take up to 3 days to register depending on the circumstances.

	* Health checks can be set on individual record sets. If a record fails, it will be removed from Route 53 until it passes. You can set SNS notifications to alert you about failed health checks.

1. AWS Transit Gateway.

	* AWS Transit Gateway works with Direct Connect as well as VPN connections. It supports IP multicast (which is not supported by any other AWS service). Mostly used for audio and video distribution.

1. Amazon VPC.

	* A Virtual Private Cloud (VPC) is a virtual network dedicated to a single AWS account. It is logically isolated from other virtual networks in the AWS cloud.

	* It consists of internet gateways (or virtual private gateways), route tables, network access control lists, subnets, and security groups.

	* 1 subnet is always in 1 AZ.

	* NAT Gateways are redundant inside the AZ. They start at 5 Gbps and scales to 45 Gbps. No patching is required. They are not associated with any Security Groups. They are automatically assigned a public IP address when created.

	* To create an AZ-independent architecture, create a NAT gateway in each AZ and configure your routing to ensure resources use the NAT gateway in the same AZ.

	* Security Groups are stateful - if you send a request from your instance, the response traffic for that request is allowed to flow regardless of inbound Security Group rules.

	* Network ACLs:
		* **Default:** Allows all outbound and inbound traffic.
		* **Custom:** Denies all outbound and inbound traffic until you add rules.

	* You can associate a network ACL with multiple subnets; however, a subnet can be associated with only 1 network ACL at a time. Network ACLs contain a numbered list of rules that are evaluated in order, starting with the lowest numbered rule.

	* Network ACLs are stateless; responses to allowed inbound traffic are subject to the rules for outbound traffic (and vice versa).

	* Each subnet in your VPC must be associated with a network ACL. If you do not explicitly associate a subnet with a network ACL, it will automatically be associated with the default network ACL.

	* Blocking IP addresses is done using network ACLs, and not Security Groups.

1. AWS VPN.

#### Security, Identity, and Compliance

1. AWS Artifact.

1. AWS Audit Manager.

1. AWS Certificate Manager (ACM).

1. AWS CloudHSM.

1. Amazon Cognito.

1. Amazon Detective.

1. AWS Directory Service.

1. AWS Firewall Manager.

1. Amazon GuardDuty.

1. AWS Identity and Access Management (IAM)

	* IAM allows you to manage users and their level of access to the AWS Console.

    * IAM is universal. It does not apply to regions. New users have NO permissions when first created. New users are assigned an Access Key ID & Secret Access Key when first created. These are not the same as a password and you cannot use them to login to the console. You can use these to access AWS is the APIs. You only get to view them once.

    * Multifactor authentication should always be setup on your root account. A password rotation policy can be also be created.

1. Amazon Inspector.

1. AWS Key Management Service (AWS KMS).

1. Amazon Macie.

	* Amazon Macie is a security service which uses Machine Learning (ML) and Natural Language Processing (NLP) to discover, classify and protect sensitive data stored in S3. It can also be used to analyse CloudTrail logs for suspicious API activity. It provides dashboards, reports, and alerting. It is great for PCI-DSS compliance and preventing ID theft.

1. AWS Network Firewall.

1. AWS Resource Access Manager (AWS RAM).

1. AWS Secrets Manager.

1. AWS Security Hub.

1. AWS Shield.

1. AWS Single Sign-On.

1. AWS WAF.

	* Amazon WAF is a web application firewall that lets you monitor the HTTP and HTTPS requests that are forwarded to Amazon CloudFront, an Application Load Balancer, or API Gateway. AWS WAF also lets you control access to your content.

    * Conditions that can be configured include:
        * The IP addresses that requests originate from.
        * The country that requests originate from.
        * The values in request headers.
        * The strings that appear in requests.
        * The length of requests.
        * The presence of SQL code that is likely to be malicious.
        * The presence of a script that is likely to be malicious.

    * Based on these conditions the application load balancer, CloudFront, or API Gateway will allow content to be received or to give HTTP 403 response.

#### Serverless

1. AWS AppSync.

1. AWS Fargate.

1. AWS Lambda.

	* Lambda lets you run code without provisioning or managing servers. You pay only for the compute time you consume.

#### Storage

1. AWS Backup.

	* Use AWS Backup to back up AWS services, such as EC2, EBS, EFS, Amazon FSx for Lustre, Amazon FSx for Windows File Server, and AWS Storage Gateway.

	* You can use AWS Organizations in conjunction with AWS Backup to back up your different AWS services across multiple AWS accounts.

	* AWS Backup gives you centralised control, letting you automate your backups and define lifecycle policies for your data. You get better compliance, as you can enforce your backup policies, ensure your backups are encrypted, and audit them once complete.

2. Amazon Elastic Block Store (Amazon EBS).

	* EBS provides persistent block storage volumes for your virtual machine drives. It stores data in equally sized blocks and organizes them into a hierarchy like a traditional file system. Each EBS volume is automatically replicated within its AZ to protect from component failure. The volumes are provisioned in size and attached to EC2 instances in a way that’s like the local disk drive on a physical machine.

	* Volumes are virtual hard disks that exist on EBS. You need a minimum of 1 volume per EC2 instance (the root device volume).

    * EBS must be paired with an EC2 instance and will always be in the same availability zone as the EC2 instance. You can change EBS volume sizes on the fly, including changing the size and storage type. When you need a high-performance storage service for a single instance, use EBS.

    * A summary of the EBS SSD types is shown below:
        <p align="center">
        <img src="/res/EBS_SSD_overview.JPG">
        </p>

    * A summary of the EBS SSD types is shown below:
        <p align="center">
        <img src="/res/EBS_HDD_overview.JPG">
        </p>

    * Regarding Snapshots:
	    * Snapshots exist on S3.
        * Snapshots are point in time copies of volumes.
        * Snapshots are incremental, only the blocks that have changed since your last snapshot are moved to S3.
        * To create a snapshot for EBS volumes that serve as root devices, you should stop the instance before taking the snapshot. A snapshot can be taken while the instance is running (although it is recommended to stop the instance).
        * You can create Amazon Machine Images (AMI's) from Snapshots.
        * To move an EC2 volume from one AZ to another, take a snapshot of it, create an AMI from the snapshot and then use the AMI to launch the EC2 instance in a new AZ.
        * To move an EC2 volume from one region to another, take a snapshot of it, create an AMI from the snapshot and then copy the AMI from one region to the other. Then use the copied AMI to launch the new EC2 instance in the new region.
        * Snapshots of encrypted volumes are encrypted automatically.
        * Volumes restored from encrypted snapshots are encrypted automatically.
        * Only unencrypted snapshots can be shared. They can be shared with other AWS accounts or made public.
        * You can now encrypt root device volumes upon creation of the EC2 instance.

    * AMI's are categorised as:
        * **EBS Volumes:** The root device for an instance launch from the AMI is an Amazon EBS volume created from an Amazon EBS snapshot.
        * **Instance Store Volumes:** The root device for an instance launched from the AMI is an instance store volume created from a template stored in Amazon S3.'

    * Instance Store Volumes are sometimes called ephemeral storage. This is because they cannot be stopped, and if the underlying host fails, you will lose your data.

    * EBS backed instances can be stopped. You will not lose the data on this instance if it is stopped. Both EBS Volumes and Instance Store Volumes can be rebooted without data loss.

    * By default, both root volumes will be deleted on termination. However, with EBS volumes, you can tell AWS to keep the root device volume.

1. Amazon Elastic File System (Amazon EFS).

	* Unlike EBS, EFS can be mounted by multiple EC2 instances, meaning many virtual machines may store files within an EFS instance. Its main feature is its scalability. EFS can grow or shrink according to demand, with more and more files being added without disturbing your application or having to provision new infrastructure.

    * EFS may be used whenever you need a shared file storage option for multiple EC2 instances with automatic, high-performance scaling.

    * EFS supports the NFSv4 protocol. You only pay for the storage you use with storage scaling up to petabytes. EFS can support thousands of NFS connections. Data is stored across multiple AZs within a region and EFS provides read after write consistency.

	* Compatible with Linux-based AMI (Windows not currently supported).

1. Amazon FSx (for all types).

	* Amazon FSx for Windows File Server provides a fully managed native Microsoft file system so you can easily move your Windows-based applications that require file storage to AWS. Amazon FSx is built on Windows Server.

    * Amazon FSx runs Windows Server Manage Block (SMB)-based file services. It also supports AD users, access control lists, groups, and security policies, along with Distributed File System (DFS) namespaces and replication.

    * Amazon FSx for Lustre is a fully managed file system that is optimised for compute-intensive workloads, such as high-performance computing, machine learning, media data processing workflows, and Electronic Design Automation (EDA).

1. Amazon S3.

	* Amazon S3 (Simple, Storage, Service) is an object storage system, designed to provide archiving and data control options and to interface with other services beyond EC2. It’s also useful for storing static html pages and shared storage for applications.

    * S3 is good at storing long-term data due to its archiving system. Things like reports and records, which may go unused for years, can be stored on S3 at a lower cost than the other two storage services discussed.

    * Files can be from 0 Bytes to 5 TB. Files are stored in Buckets which are basically folders. S3 is a universal namespace. That is, names must be unique globally. This is because a bucket can be accessed at a web address. When uploading a file to an S3 Bucket, a HTTP 200 response is received upon successful completion of the upload.

    * The format of the AWS URL is `https://<region>.amazonaws.com/<bucket>`.

    * Components of the S3 object include:
        * **Key:** The name of the object.
        * **Value:** The data which is made up of a sequence of bytes.
        * **Version ID:** Important for versioning.
        * **Metadata:** Data about data that you are storing.
        * **Access Control Lists:** Permissions of the object.
        * **Torrent:** 

    * S3 has read after write consistency for PUTS of new objects, and eventual consistency for overwrite PUTS and DELETES. This means that new files will be instantly readable after writing, but there may be a small delay to read the correct version after updating an existing file.

    * S3 has the following availability guarantees:
        * Built for 99.99% with a guarantee of 99.9%.
        * 99.99999999999% (11 9s) durability.

    * S3 has the following features:
        * Tiered Storage.
        * **Lifecycle Management:** Automates moving your objects between the different storage tiers. Can be used in conjunction with versioning.
        * **Versioning:** Stores all versions of an object (including all writes and even if you delete an object). Once enabled, versioning cannot be disabled, only suspended.
        * Encryption.
        * MFA Required for Delete.
        * Secure data using Access Control Lists and Bucket Policies.

    * S3 Storage Classes:
        * **S3 Standard:** 99.99% availability and 99.999999999% durability. Data is stored redundantly across multiple devices and in multiple facilities (>=3 AZs).
        * **S3 - IA (Infrequently Accessed):** For data that is accessed less frequently, but requires rapid access when needed. Lower fee than S3, but you are charged a retrieval fee.
        * **S3 One Zone - IA:** Like IA but you do not require multiple Availability Zone data resilience. This is 20% less than regular S3-IA. Great for long-lived, infrequently accessed, non-critical data.
        * **S3 - Intelligent Tiering:** Designed to optimise costs by automatically moving data to the most cost-effective access tier, without performance impact or operational overhead.
        * **Glacier Instant Retrieval:** Long-term data archiving with intance retrieval time. Retrieval fee applies.
        * **Glacier Flexible Retrieval:** Archive data that does not require immediate access but needs flexibility to retrieve larget sets of data at no cost (e.g. DR). Can be minutes or up to 12 hours. Retrieval fee applies.
        * **Glacier Deep Archive:** Cheapest storage designed for retaining data sets for 7-10 years. Standard retrieval time is 12 hours, and the bulk retrieval time is 48 hours. Retrieval fee applies.

    * A summary of the AWS storage tiers is shown below:
        <p align="center">
        <img src="/res/storage_overview.JPG">
        </p>

    * You are charged for S3 in the following ways:
        * **Storage:** How much data is stored.
        * **Requests:** How many requests are made.
        * **Storage Management Pricing:** The tier of storage.
        * **Data Transfer Pricing:** The cost to transfer objects from different regions.
        * **Transfer Acceleration:** Enables faster transfers of objects to end users and an S3 bucket. Uses Amazon CloudFront’s globally distributed edge locations to route data over an optimised network path.

    * S3 buckets can be configured to create access logs which log all requests made to the S3 bucket.

    * Encryption At Rest is achieved by:
        * **S3 Managed Keys - SSE-S3:** Key managed by Amazon.
        * **AWS Key Management Service, Managed Keys - SSE-KMS:** Key managed by you.
        * **Service Side Encryption With Customer Provided Keys - SSE-C:** Key managed by you.
        * **Client Side:** Encrypting the file before you upload it.

    * S3 Object Lock can be used to store objects in a Write Once, Read Many (WORM) model. It can help you prevent objects from being deleted or modified for a fixed amount of time or indefinitely.

    * S3 Glacier Vault Lock allows you to easily deploy and enforce compliance controls for individual S3 Glacier vaults with a Vault Lock policy. You can specify controls, such as WORM, in a Vault Lock policy and lock the policy from future edits. Once locked, the policy can no longer be changed.

    * Object locks come in governance mode and compliance mode. With governance mode, users can't overwrite or delete an object version or alter its lock settings unless they have special permissions. With compliance mode, a protected object version can't be overwritten or deleted by any user, including the root user in your AWS account.

    * Prefixes are the component of the pathname between the bucket name and the file name. More prefixes result in better performance. You can get 3,500 PUT/COPY/POST/DELETE and 5,500 GET/HEAD requests per second per prefix. This means that if you spread your reads across different prefixes you can allow more requests per second.

    * Multipart uploads can increase performance when uploading files to S3. This is recommended for files over 100 MB and must be used for any file over 5 GB. S3 byte-range fetches can also increase performance when downloading files from S3.

    * If you are using SSE-KMS to encrypt your objects in S3, keep in mind the KMS limits. Uploading or downloading will count towards the KMS quota. This is region-specific but is either 5,500, 10,000, or 30,000 requests per second. Currently you cannot request a quota increase for KMS.

    * S3 Select is used to retrieve only a subset of data from an object using simple SQL expressions. This allows you to save money on data transfer and increase speed.

    * S3 buckets can be shared across accounts using Bucket Policies and IAM (applies across the entire bucket) or using Bucket ACLs and IAM (individual objects) for programmatic access. To share with console access as well then you can create cross-account IAM roles.
    
    * When using cross region replication, the following should be considered:
        * Versioning must be enabled on both the source and destination buckets.
        * Files in an existing bucket are not replicated automatically.
        * All subsequent updated files will be replicated automatically.
        * Delete markers are not replicated.
        * Deleting individual versions or delete markers will not be replicated

1. Amazon S3 Glacier.

	* S3 Glacier is a secure, durable, and low-cost storage class for data archiving. Retrieval times configurable from minutes to hours.

    * S3 Glacier Deep Archive is the lowest-cost storage class where a retrieval time of 12 hours is acceptable.

1. AWS Storage Gateway.

	* AWS Storage Gateway is a service that connects an on-premises software appliance with cloud-based storage to provide seamless and secure integration between an organisations on-premises IT environment and AWS's storage infrastructure. The service enables you to securely store data to the AWS cloud for scalable and cost-effective storage.

    * AWS Storage Gateway is available for download as a virtual machine (VM) image that you install on a host in your datacentre. Storage Gateway supports either VMware ESXi or Microsoft Hyper-V. Once you've installed your gateway and associated it with your AWS account through the activation process, you can use the AWS Management Console to create the storage gateway option that is right for you.

    * Types of Storage Gateway include:
        * **File Gateway (NFS & SMB):** Files are stored in your S3 buckets, and accessed through a Network File System (NFS) mount point. Ownership, permissions, and timestamps are stored in S3 in the user-metadata of the object associated with the file. Once transferred to S3 they can be managed as native S3 objects.
        * **Volume Gateway (iSCSI):** Presents your applications with disk volumes using the iSCSI block protocol. Data written to these volumes can be asynchronously backed up point-in-time snapshots of your volumes and stored in the cloud as Amazon EBS snapshots. Snapshots are incremental backups that only capture changed blocks. All snapshot storage is compressed to minimise your storage charges. Stored volumes are where the entire dataset is stored on site and is asynchronously backed up to S3. Cached volumes are where the entire dataset is stored on S3 and the most frequently accessed data is cached on site.
        * **Tape Gateway (VTL):** The VTL interface provided lets you leverage your existing tape-based backup application infrastructure to store data on virtual tape cartridges that you create on your tape gateway. Each tape gateway is preconfigured with a media changer and tape drives, which are available to your existing client backup applications as iSCSI devices.