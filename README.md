# Exam SAA-C02

- [Design Resilient Architectures](#Design-Resilient-Architectures)
- [Design High-Performing Architectures](#Design-High-Performing-Architectures)
- [Design Secure Applications and Architectures](#Design-Secure-Applications-and-Architectures)
- [Design Cost-Optimized Architectures](#Design-Cost-Optimized-Architectures)
- [Appendix](#Appendix)

## Design Resilient Architectures

### Design a multi-tier architecture solution

1. Determine a solution design based on access patterns.

1. Determine a scaling strategy for components used in a design.

1. Select an appropriate database based on requirements.

1. Select an appropriate compute and storage service based on requirements.

### Design highly available and/or fault-tolerant architectures

1. Determine the amount of resources needed to provide a fault-tolerant architecture across Availability Zones.

    * A Region is a physical location in the world which consists of two or more Availability Zones (AZ's).
    * An AZ is one or more discrete data centres, each with redundant power, networking and connectivity, housed in separate facilities.
    * Edge Locations are endpoints for AWS which are used for caching content. Typically, this consists of CloudFront, Amazon's Content Delivery Network (CDN).

1. Select a highly available configuration to mitigate single points of failure.

1. Apply AWS services to improve the reliability of legacy applications when application changes are not possible.

1. Select an appropriate disaster recovery strategy to meet business requirements.

1. Identify key performance indicators to ensure the high availability of the solution.

### Design decoupling mechanisms using AWS services

1. Determine which AWS services can be leveraged to achieve loose coupling of components.

1. Determine when to leverage serverless technologies to enable decoupling.

### Choose appropriate resilient storage

1. Define a strategy to ensure the durability of data.

1. Identify how data service consistency will affect the operation of the application.

1. Select data services that will meet the access requirements of the application.

1. Identify storage services that can be used with hybrid or non-cloud-native applications.

## Design High-Performing Architectures

### Identify elastic and scalable compute solutions for a workload

1. Select the appropriate instance(s) based on compute, storage, and networking requirements.

1. Choose the appropriate architecture and services that scale to meet performance requirements.

1. Identify metrics to monitor the performance of the solution.

### Select high-performing and scalable storage solutions for a workload

1. Select a storage service and configuration that meets performance demands.

1. Determine storage services that can scale to accommodate future needs.

### Select high-performing networking solutions for a workload

1. Select appropriate AWS connectivity options to meet performance demands.

1. Select appropriate features to optimize connectivity to AWS public services.

1. Determine an edge caching strategy to provide performance benefits.

1. Select appropriate data transfer service for migration and/or ingestion.

### Choose high-performing database solutions for a workload 

1. Select an appropriate database scaling strategy.

1. Determine when database caching is required for performance improvement.

1. Choose a suitable database service to meet performance needs.

## Design Secure Applications and Architectures

### Design secure access to AWS resources

1. Determine when to choose between users, groups, and roles.

1. Interpret the net effect of a given access policy.

1. Select appropriate techniques to secure a root account.

1. Determine ways to secure credentials using features of AWS IAM.

1. Determine the secure method for an application to access AWS APIs.

1. Select appropriate services to create traceability for access to AWS resources.

### Design secure application tiers

1. Given traffic control requirements, determine when and how to use security groups and network ACLs.

1. Determine a network segmentation strategy using public and private subnets.

1. Select the appropriate routing mechanism to securely access AWS service endpoints or internet-based resources from Amazon VPC.

1. Select appropriate AWS services to protect applications from external threats.

### Select appropriate data security options

1. Determine the policies that need to be applied to objects based on access patterns.

1. Select appropriate encryption options for data at rest and in transit for AWS services.

1. Select appropriate key management options based on requirements.

## Design Cost-Optimized Architectures

### Identify cost-effective storage solutions

1. Determine the most cost-effective data storage options based on requirements.

    * S3 pricing for US East (N. Virginia) is shown below:
        <p align="center">
        <img src="/res/storage_pricing.jpg">
        </p>

1. Apply automated processes to ensure that data over time is stored on storage tiers that minimize costs.

### Identify cost-effective compute and database services

1. Determine the most cost-effective Amazon EC2 billing options for each aspect of the workload.

1. Determine the most cost-effective database options based on requirements.

1. Select appropriate scaling strategies from a cost perspective.

1. Select and size compute resources that are optimally suited for the workload.

1. Determine options to minimize total cost of ownership (TCO) through managed services and serverless architectures.

### Design cost-optimized network architectures 

1. Identify when content delivery can be used to reduce costs.

1. Determine strategies to reduce data transfer costs within AWS.

1. Determine the most cost-effective connectivity options between AWS and on-premises environments.

## Appendix

### Key Tools and Technologies

1. Compute

1. Cost management

1. Database

1. High availability

1. Management and governance

1. Microservices and component decoupling

1. Migration and data transfer

1. Networking, connectivity, and content delivery

1. Security

1. Serverless design principles

1. Storage

### AWS Services and features

#### Analytics

1. Amazon Athena

1. Amazon Elasticsearch Service (Amazon ES)

1. Amazon EMR

1. AWS Glue

1. Amazon Kinesis

1. Amazon QuickSight

#### AWS Billing and Cost Management

1. AWS Budgets

1. Cost Explorer

#### Application Integration

1. Amazon Simple Notification Service (Amazon SNS)

1. Amazon Simple Queue Service (Amazon SQS)

#### Compute

1. Amazon EC2

    * Elastic Compute Cloud (EC2) is a web service that provides resizable compute capacity in the cloud. It is designed to make web-scale computing easier for developers.

1. AWS Elastic Beanstalk

1. Amazon Elastic Container Service (Amazon ECS)

1. Amazon Elastic Kubernetes Service (Amazon EKS)

1. Elastic Load Balancing

1. AWS Fargate

1. AWS Lambda

    * Lambda lets you run code without provisioning or managing servers. You pay only for the compute time you consume.

#### Database

1. Amazon Aurora

1. Amazon DynamoDB

    * Amazon DynamoDB is a fast and flexible non-relational database service for any scale. DynamoDB enables customers to offload the administrative burdens of operating and scaling distributed databases to AWS so that they don’t have to worry about hardware provisioning, setup and configuration, throughput capacity planning, replication, software patching, or cluster scaling.

1. Amazon ElastiCache

1. Amazon RDS

    * Amazon Relational Database Service (Amazon RDS) is a managed service that makes it easy to set up, operate, and scale a relational database in the cloud. Amazon RDS gives you access to the capabilities of a familiar MySQL, MariaDB, Oracle, SQL Server, or PostgreSQL database.

1. Amazon Redshift

#### Management and Governance

1. AWS Auto Scaling

1. AWS Backup

1. AWS CloudFormation

1. AWS CloudTrail

1. Amazon CloudWatch

    * CloudWatch monitors your AWS resources and the applications you run on AWS in real time. You can use CloudWatch to collect and track metrics, which are variables you can measure for your resources and applications.

    * The CloudWatch home page automatically displays metrics about every AWS service you use. You can additionally create custom dashboards to display metrics about your custom applications and display custom collections of metrics that you choose.

1. AWS Config

1. Amazon EventBridge (Amazon CloudWatch Events)

1. AWS Organizations

1. AWS Resource Access Manager

1. AWS Systems Manager

1. AWS Trusted Advisor

#### Migration and Transer

1. AWS Database Migration Service (AWS DMS)

1. AWS DataSync

1. AWS Migration Hub

1. AWS Server Migration Service (AWS SMS)

1. AWS Snowball

1. AWS Transfer Family

#### Networking and Content Delivery

1. Amazon API Gateway

1. Amazon CloudFront

    * CloudFront is a content delivery service that works in conjunction with other services to provide developers with a simple way to distribute content to end users.

    * This service is useful for companies with a need for higher response times and large file content that want to distribute these files to a sizeable number of users. Once content is put in an origin server, like an Amazon Simple Storage Service bucket or an Elastic Compute Cloud instance, it’s pushed out to multiple CloudFront servers as content is requested.

1. AWS Direct Connect

1. AWS Global Accelerator

1. Amazon Route 53

1. AWS Transit Gateway

1. Amazon VPC (and associated features)

    * A Virtual Private Cloud (VPC) is a virtual network dedicated to a single AWS account. It is logically isolated from other virtual networks in the AWS cloud.

#### Security, Identity, and Compliance

1. AWS Certificate Manager (ACM)

1. AWS Directory Service

1. Amazon GuardDuty

1. AWS Identity and Access Management (IAM)

    * IAM allows you to manage users and their level of access to the AWS Console.

1. AWS Key Management Service (AWS KMS)

1. Amazon Macie

1. AWS Secrets Manager

1. AWS Shield

1. AWS Single Sign-On

1. AWS WAF

#### Storage

1. Amazon Elastic Block Store (Amazon EBS)

    * EBS provides storage for your virtual machine drives. It stores data in equally sized blocks and organizes them into a hierarchy like a traditional file system. The volumes are provisioned in size and attached to EC2 instances in a way that’s like the local disk drive on a physical machine.

    * EBS must be paired with an EC2 instance. When you need a high-performance storage service for a single instance, use EBS.

1. Amazon Elastic File System (Amazon EFS)

    * Unlike EBS, EFS can be mounted by multiple EC2 instances, meaning many virtual machines may store files within an EFS instance. Its main feature is its scalability. EFS can grow or shrink according to demand, with more and more files being added without disturbing your application or having to provision new infrastructure.

    * EFS may be used whenever you need a shared file storage option for multiple EC2 instances with automatic, high-performance scaling.

1. Amazon FSx

1. Amazon S3

    * Amazon S3 (Simple, Storage, Service) is an object storage system, designed to provide archiving and data control options and to interface with other services beyond EC2. It’s also useful for storing static html pages and shared storage for applications

    * S3 is good at storing long-term data due to its archiving system. Things like reports and records, which may go unused for years, can be stored on S3 at a lower cost than the other two storage services discussed.

    * Files can be from 0 Bytes to 5 TB. Files are stored in Buckets which are basically folders. S3 is a universal namespace. That is, names must be unique globally. This is because a bucket can be accessed at a web address. When uploading a file to an S3 Bucket, a HTTP 200 response is received upon successful completion of the upload.

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
        * **S3 Standard:** 99.99% availability and 99.999999999% durability. Data is stored redundantly across multiple devices and in multiple facilities.
        * **S3 - IA (Infrequently Accessed):** For data that is accessed less frequently, but requires rapid access when needed. Lower fee than S3, but you are charged a retrieval fee.
        * **S3 One Zone - IA:** Like IA but you do not require multiple Availability Zone data resilience.
        * **S3 - Intelligent Tiering:** Designed to optimise costs by automatically moving data to the most cost-effective access tier, without performance impact or operational overhead.

    * A summary of the AWS storage options is shown below:
        <p align="center">
        <img src="/res/storage_overview.jpg">
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

1. Amazon S3 Glacier

    * S3 Glacier is a secure, durable, and low-cost storage class for data archiving. Retrieval times configurable from minutes to hours.
    * S3 Glacier Deep Archive is the lowest-cost storage class where a retrieval time of 12 hours is acceptable.

1. AWS Storage Gateway