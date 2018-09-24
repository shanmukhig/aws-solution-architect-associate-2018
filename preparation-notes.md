# AWS 10000 Feet Overview

## Global Infrastructure

  - A Region is geographical area consisting of 2 or more availability zones.

  - Availability zone is logical data center

  - Edge Locations are CDN End Points for CloudFront. Many more edge locations exist than regions.

## The AWS Platform

  - Networking & Content Delivery

      - VPC [know VPC in and out] – Virtual Data Center. You can have multiple VPCs per region. VPCs can also be connected to each other.

      - Route53 – Amazon’s DNS Service

      - CloudFront – Content delivery network. Edge locations cache assets.

      - Direct Connect – Connect your physical DCs to AWS using dedicated telephone lines

  - Compute 

      - EC2 – Elastic Compute Cloud.

      - EC2 Container Services (ECS) – supports Docker.

      - Elastic Beanstalk (important for developer exam). Just upload your code here. Elastic Bean stalk will provision all infrastructure required.

      - Lambda. Alexa, Echo devices rely on Lambda

  - Storage

      - S3 - Object Store

      - Glacier – Archive files from S3 into Glacier – use when you don’t need immediate access to files

      - EFS (Elastic File Service) - Block Store - can be used for storing databases. It can be attached to multiple EC2 instances.

      - Storage Gateway (VM) - communicates between your data center and S3 storage.
       - file storage (nfs protocol)
       - volume storage 
        - storage gateway (all files are stored locally, and backed up to s3 async), 
         - good use case for backing up all your local data while maintaining a local copy
        - storage cached (all files stored in s3, only frequently used files are stored in cache)
         - good use case when you are running out of storage space in on-premises
       - virtual tape library (vtl) - for archival purpose
        - peta byte scale archival storage 
  - Databases

      - RDS ( MySQL, PostgreSQL, SQL Server, MariaDB, Aurora)

      - DynamoDB - Non relational DB (important for developer exam)

      - Redshift  - Data warehousing system - 

      - ElastiCache - Cloud in-memory DB (important for developer / architect exam)
       - Memcached
       - Redis
  
  - Migration

      - Snowball - Transfer Data - next step over Export Import gateway. Store all your data from enterprise into Snowball and then ship to AWS.
      - Snowball edge – add compute capacity to storage device – so that you can run analytics on top of the huge dataset collected, without having to transfer to cloud. AWS Lambda is supported on Snowball edge.
      - snowmobile - 45foot long container for moving big data centers

      - DMS - Database migration services - migrate existing DBs to Cloud, also migrate existing Cloud DBs to other regions. Can migrate from Oracle/MySQL/PostgreSQL/ to Aurora.  

      - SMS - Server migration services - migrate existing VMs on premise to the Cloud -up to 50 concurrent ones.

  - Analytics

      - EMR -Elastic Map Reduce - process large amounts of data. Based on Hadoop, Apache Spark. Log Analytics etc.

      - Kinesis - streaming and analysis real time data (important for architect exam). used for collating large amounts of data streamed from multiple sources

  - Security & Identity

      - IAM – Important for all AWS exams. How you setup and assign users / groups etc.

  - Management Tools (important for architect exam)

      - Cloud Watch - monitor performance of AWS environment – standard infrastructure metrics.

      - Cloud Formation - Infrastructure into Code - document which describes the infrastructure which uses AWS resources.

      - Cloud Trail - audit usage of AWS Resources. Important for security exam.

      - Config manager - monitors environments and **provides alerts for events**. E.g. someone creates a security group which is against policy

      - Trusted Advisor - automated tips for cost & performance optimization, security tips, architecture and design

  - Application Services

      - Step functions – visualize application internals – which micro services is your application using.

      - SWF - Simple Workflow Service. Used in Amazon fulfillment center.

      - API Gateway - Create, Publish & monitor API services. Access back-end services. 

      - Elastic Transcoder - convert video into multiple formats to suit all devices.

  - Messaging  (important for associate exam)

      - SNS – Notify by email / text messages/ http-end points

      - SQS - Post messages to Queue. De-couple your applications.

      - SES – send email via AWS

# Identity & Access Management

## IAM 101

  - Configure who uses AWS and their level of access to the AWS Console.

  - Centralized control over AWS Account

  - Share access for AWS Account

  - Granular permissions for users / services

  - Identity Federation – Facebook, LinkedIn and Active Directory- You can login to AWS with your corporate credentials.

  - Multi-factor authentication – helps secure the account. Especially for root account

  - Temporary access to users and services

  - Setup password rotation policy

  - Integration with other AWS services.

  - Supports PCI-DSS compliance

### Critical Terms

IAM consists of the following

  - Users – End users / people.

  - Groups – Users having one set of permissions.

  - Roles – Create roles and assign them to AWS resources.

  - Policies – Document (JSON format) that defines one or more permissions – assign to user or groups

### IAM Features

  - IAM is a global service. It is not region specific

  - Root account is the email address you use to sign up for AWS

  - AWS recommends very limited usage of root account

  - Setup MFA on root account.

  - You can attach permissions to individual users and groups.

  - Secret access key can be retrieved only once during user creation. In case you lose it then you can re-generate it.

  - IAM Password policy can be set to access the admin console.

  - New users have no permissions when first created. Everything has to be explicitly added.

  - Power User Access allows Access to all AWS services except the management of groups and users within IAM.

Manage AWS resources via

1. Management console – Using username and password

2. Rest APIs – Using Access Key ID and Secret Access Key

3. AWS CLI - Using Access Key ID and Secret Access Key

4. AWS SDK – various programming languages supported.

Using Access Key ID and Secret Access Key – can be used only via accessing programmatically. Akin to username and password used while accessing the console

# AWS Object Storage & CDN – S3, Glacier and CloudFront

## S3 101

### S3 Object Storage Classes

  - S3-Standard - Durability of 99.999999999% and availability of 99.99%.

  - S3-IA (Infrequently Accessed) - Durability of 99.999999999% and availability of 99.9%.

  - S3-RRS (Reduced Redundancy Storage) - Durability and availability of 99.99%. Use when you don’t care if data is occasionally lost and can easily be re-created.
  
  - Glacier - For archival only. Takes 3 - 5 hours to restore files. Durability of 99.999999999%.

### S3 Buckets

  - S3 Namespace is global. Region independent.

  - A bucket name in any region should only contain lower case characters. It has to be DNS Compliant

  - Object versioning - Different versions of the same object in a bucket.

  - Only Static website can be hosted. Auto scaling, Load Balancing etc. all managed automatically.

  - You can tag buckets (or any AWS resoruce) to track costs. Tags consist of keys and (optional) value pairs.

  - Lifecycle management of objects can be set. e.g. move to Glacier after 30 days

  - Every bucket created, object uploaded is private by default.

  - Object Permissions – Access to Object ACLs

  - Prefix in bucket is a folder in the bucket.

  - Minimum file size that I can store on S3 bucket is 0 byte.

  - Max 100 S3 buckets per account by default.

  - Individual Amazon S3 objects can range in size from a minimum of **0 bytes** to a maximum of **5 terabytes**. The largest object that can be uploaded in a single PUT is **5 gigabytes**. For objects larger than **100 megabytes**, customers should consider using the Multipart Upload capability.

### S3 Versioning

  - Once versioning is turned on it cannot be removed. It can only be suspended. To remove versioning, you have to create a new bucket and transfer all files from old to new

  - For newer version of an object, you still have to set permissions to allow access. It is disabled by default even if previous version is public.

  - All versions of the file add up to the storage. Hence for larger objects, ensure that there is some lifecycle versioning in place.

  - Version deleted cannot be restored.

  - Object deleted can be restored – Delete the Delete marker.

  - Versioning is a good backup tool.

  - For versioning. MFA can be setup for Delete capability for object / bucket – Complicated setup.

## Cross Region Replication

  - To allow for cross region replication, the both source and target buckets must have versioning enabled.

  - When cross region replication is enabled, all existing objects in the bucket are not copied over to replica site. Only Updates to existing objects and newer objects are replicated over. All previous versions of the updated objects are replicated.

  - Permissions are also replicated from one bucket to another.

  - Transitive replications do not work. E.g. if you setup bucket C to replicate content from bucket B which replicates content from bucket A – Changes made to bucket A will not get propagated to C. You will need to manually upload content to bucket B to trigger replication to C.

  - Delete markers are replicated.

  - If you delete source replication bucket objects, they are deleted from replica target bucket too. When you delete a Delete marker or version from source, that action is not replicated.

## Lifecycle Management

  - Objects stored in Glacier incur minimum 90 day storage cost.

  - Lifecycle management can be used in conjunction with versioning

  - Objects can be transitioned to S3-IA after 30 days and to Glacier class storage - 30 days IA.

  - You can also permanently delete objects.

## CloudFront CDN Overview

### Important terms

  - CDN – collection of distributed servers where the content is served to users based on the user’s location and the location of content origin.

  - Edge location – location where content will be cached. Different from AWS Region / AZ

  - Origin – Can be S3 Bucket, an EC2 Instance, an Elastic Load Balancer or Route53

  - Distribution – is the name given to CDN collection which consists of Edge locations.

  - Web Distribution – Typically used for websites & web content only.

  - RTMP – Used for Media Streaming. Adobe Flash media server’s protocol – video streaming.

  - First request is slow as it comes from source origin. Subsequent requests improve speed as they are cached in nearest edge location and routed there until TTL expires.

  - CloudFront also works with non AWS origin which can be on premise as well. .

  - Edge locations are for read and write as well. Objects PUT on edge location are sent to origin

  - Objects are cached for life of TTL. TTL can be set for 0 seconds to 365 days. Default TTL is 24 hours. If objects change more frequently update the TTL

  - You can clear cached objects, with charges.

  - Origin domain name – either S3 bucket, ELB or on premise domain

### CloudFront Security.

  - You can force them to use CDN URL instead of S3 DNS

  - To restrict bucket access you need to create origin access identity. And allow this user read permission S3 bucket content –

  - Set video protocol policy – redirect http to https, http or https

  - Allows various HTTP methods – GET, PUT, POST, PATCH, DELETE, and HEAD.

  - Restrict viewer access for S3 and CDN using pre-Signed URLs or Signed cookies. E.g. You can view video only using that URL

  - Using Web Application Firewalls to prevent SQL injection, CSS attacks

  - For https access, you can either use default CloudFront certificate or own certificate can be imported via ACM.

  - Provisioning / Updating CloudFront distribution takes up to 15-20 minutes.

  - Geo-restriction can be setup. Either whitelist or blacklist – countries from where content can be accessed.

  - Invalidating removes objects from CloudFront. It can be forced to remove from Cache – obviously costs.

  - You can force users to get content via CloudFront after removing read access to S3 bucket.

  - You can also upload content to CloudFront.

## S3 Security & Encryption

### Security

  - By default all newly created buckets are Private

  - Control Access to buckets using

      - Bucket Policies – bucket wide.

      - Access Control Lists – up to individual objects.

  - S3 buckets can log all access requests to another S3 bucket even another AWS account.

### Encryption

  - In Transit

Secured using SSL/TLS

  - Data at rest

1. Server Side

    1. S3 Managed Keys – SSE – S3

    2. AWS KMS Managed Keys – SSE – KMS – Envelop Key. Provides audit trail

    3. SSE using customer provided keys. Key Management is responsibility of user. SSE-C

2. Client Side

Encrypt data at client side and then upload to S3.

## Storage Gateway

  - It is a service which connects an on-premises software appliance (virtual) with cloud based storage to provide seamless and secure connectivity between the two. Either via internet or Direct connect.

  - It can also provide connectivity from EC2 instance in VPC to S3 via Storage Gateway in same VPC

  - The virtual appliance will asynchronously replicate information up to S3 or Glacier

  - Can be downloaded as a VM – VMware ESXi / Hyper-V.

  - 4 Types of Storage Gateways.

 1.[Brand New] *File Gateway (NFS) – Just store files in S3 – Word, Pictures, PDFs, and no OS. ( Saves a lot of money)
  -Files are stored as objects in S3 buckets and accessed over NFS mount point
  -File attributes as stored as S3 object metadata.
  -Once transferred to S3, standard S3 features apply to all files.

 2.Volumes Gateway (iSCSI) – uses block based storage – virtual hard disk, operating system.
  - Stored Volumes – Store entire data set copy on-prem. Data async backed up to AWS S3.
  - Cached Volumes – Stored only recently accessed data on-prem. Rest on AWS S3

  Volume gateway interface presents applications with disk volumes using iSCSI protocol. They take virtual hard disks on premise and back them up to virtual hard disks on AWS. Data written to these volumes can be asynchronously backed up as point in time snapshots of volumes and stored in cloud as EBS snapshots.

 3.Gateway Virtual Tape Library (VTL) – Backup and Archiving solution. Create tapes and send to S3. You can use existing backup applications like NetBackup, Backup Exec, and Veam etc.

## Snowball

Next version of Import / Export Gateway

You could accelerate moving large amounts of data into and out of AWS using portable storage devices for transport. Ship the storage device – no need to transfer over the internet.  Problem arose with different types of disks

### Snowball Standard
  - Bigger than briefcase sized storage devices
  - Petabyte scale data transport solution used to transfer data in/out of AWS
  - Cost is 1/5th as compared to transfer via high speed internet.
  - 80TB snowball available.
  - Multiple layers of security to protect data. Tamper resistant enclosure, 256-bit encryption
  - Once data is transferred, AWS performs software erasure of Snowball appliance.


### Snowball Edge
  - 100 TB data transfer device which has onboard storage and compute capabilities.
  - Move large amounts of data in and out of AWS, as a temporary storage tier for large local datasets.
  - You can run Lambda functions.
  - Devices connect to existing applications and infrastructure using standard storage interfaces.
  - Snowball Edges can be clustered together to process your data on premise


### Snowmobile
  - Massive 45 foot long ruggedized shipping container, pulled by a truck.
  - Petabyte or Exabyte of data that has to be transferred to AWS. 100 PB per snowmobile.
  - You can use it for data center migration.

Using snowball – Import / Export S3. If using Glacier first need to import into S3 and then into Snowball.

## S3 Transfer Acceleration

It utilizes the CloudFront Edge Network to accelerate uploads to S3. Instead of uploading directly to S3, you can use a distinct URL to upload directly to an edge location which will then transfer to S3 using Amazon’s backbone network.

The farther you are from S3 bucket region the higher is the improvement you can observe using S3 Transfer Acceleration. High cost for usage than standard S3 transfer rates.

# EC2 – The Backbone of AWS

## EC2 101

  - Elastic Compute Cloud

  - Provides resizable compute capacity in cloud ( scale up and down)

  - Helps developers failure resilient systems and isolate them

### EC2 Pricing

  - On demand.

  - Pay per hour of usage.

  - Applications with short term, spiky usage patterns or unpredictable workloads that cannot be interrupted.

  - New apps on AWS

  - Reserved pricing

  - Reserve capacity over significant period of time. Significant discount.

  - Applications with steady or predictable usage over a period of time. Reserved capacity required.

  - Further discount if upfront payment

  - Spot pricing –

  - Bid your price for compute. When bid price is higher than Spot price, then you can provision it. When it goes lower, instance is terminated. Useful for applications who have flexible start / stop times

  - [Exam Tip] If AWS terminates instance, you are not charged for partial hour. If you terminate, you will be charged for the hour.

  - Applications that are feasible only at very low compute prices. E.g. pharma simulations

  - Applications with urgent computing capacity

  - Dedicated physical machines – pay by hour.

  - Massive discount for reserved instances over a long period of time – upto 70% for 3 years.

  - Useful for regulatory requirements

  - Certain licensing agreements prevent usage on virtual machine / multi-tenancy deployments.

### EC2 Instance Types

 - Amazon EC2 instances are grouped into 5 families: 

  - General Purpose - General Purpose Instances have memory to CPU ratios suitable for most general purpose applications and come with fixed performance (M5, M4) or burstable performance (T2);
 
  - Compute Optimized -  Compute Optimized instances (C5, C4) have proportionally more CPU resources than memory (RAM) and are well suited for scale out compute-intensive applications and High Performance Computing (HPC) workloads;

  - Memory Optimized - Memory Optimized Instances (X1e, X1, R4) offer larger memory sizes for memory-intensive applications, including database and memory caching applications;

  - Storage Optimized - Storage Optimized Instances (H1, I3, D2) that provide very high, low latency, I/O capacity using SSD-based local instance storage for I/O-intensive applications, with D2 or H1, the dense-storage and HDD-storage instances, provide local high storage density and sequential I/O performance for data warehousing, Hadoop and other data-intensive applications.

  - Accelerated Computing instances.    Accelerating Computing instances (P3, P2, G3, F1) take advantage of the parallel processing capabilities of NVIDIA Tesla GPUs for high performance computing and machine/deep learning; GPU Graphics instances (G3) offer high-performance 3D graphics capabilities for applications using OpenGL and DirectX; F1 instances deliver Xilinx FPGA-based reconfigurable computing; 

  - When choosing instance types, you should consider the characteristics of your application with regards to resource utilization (i.e. CPU, Memory, Storage) and select the optimal instance family and instance size.

[Exam Tip] You will be asked to provide which instance type to use for a given scenario. Usually 3 options are fictitious.

EC2 Key Pairs are region specific

## EBS

- Block based storage

- You can install OS, Database on it, unlike S3

- Placed in specific AZ. Automatically replicated within the AZ to protect from failure.

- [Exam Tips]*  - EBS Volume Types**

SSD Drives

  - (root volume) General Purpose SSD – up to 10,000 IOPS. 3 IOPS per GB. Balances price and performance. You can burst upto 3000 IOPS for 1GB

- (root volume) Provisioned SSD – when you need more than 10,000 IOPS. Large RDBMS DBs and NoSQL DBs. Up to 20000 IOPS now

Magnetic Drives

- HDD, Throughput Optimized– ST1 – Required for data written in sequence. Big Data, DWH, Log processing. Cannot be used as boot volumes

- HDD, Cold– SC1 – Data that isn’t frequently accessed. E.g. File Server. Cannot be used as boot volume

- (root volume) HDD, Magnetic (Standard) – *Cheapest bootable EBS volume type*. Used for apps where data is less frequently accessed and low cost is important.

- You cannot mount 1 EBS volume to multiple EC2 Instances. Use EFS instead.

- EBS Root Volumes can be encrypted on custom AMIs only. Not on the default available AMIs. To encrypt root volumes, create a new AMI and encrypt root volume. You can also encrypt using 3rd party software like Bit Locker. Additional volumes attached to EC2 instance can be encrypted.

- EC2 – 1 subnet equals 1 Availability Zone.

- Default VPC & Security group is created in when you create your account.

- Default CloudWatch monitoring – every 5 mins. Can enabled advanced monitoring to check at interval of each minute.

- Volume – Virtual Hard Disk

- Tag everything on AWS

- Default Linux EC2 username is ec2-user

- Default Windows EC2 username is Administrator

- Termination protection is turned off by default. You need to turn it on.

- When instance is terminated, root volume is deleted. You can turn if off.

- System Status Check – Overall health of hosting infrastructure. If they arise, Terminate instance and recreate

- Instance Status Check – Health of instance. If they arise, reboot the instance.

## EC2 Security Groups

  - A security group is a virtual firewall.

  - First line of defense. Network ACLs are second line.

  - 1 instance can have multiple security groups. As each security group only "allows" inbound traffic, there will never be a conflict on security group rules.

  - Security group changes are applied immediately.

  - Security groups are "stateful". Rules added as inbound rules – automatic outbound rules are added. Response back on the same channel. NACLs are stateless.

  - All inbound traffic is blocked by default. You have to allow specific inbound rules for protocols

  - All outbound traffic is allowed by default.

  - Only allow rules, no deny rules exist. Use NACLs to deny specific IPs

  - Any number of EC2 instances in a security group.

  - EC2 instances in the default security group can communicate with each other.

  - Multiple security groups can be attached to an instance.

## Volumes and Snapshots

  - Volumes are virtual hard disks.

  - You can attach volume to EC2 instance belonging to same AZ

  - To Detach a volume from EC2 instance, you have to umount it first

  - Snapshots are point in time copies of volumes – stored in S3. Taking first snapshot takes a while.

  - Subsequent snapshots will only store the delta in S3. Only changed blocks are stored in S3.

  - You can create volumes from Snapshots. During this you can also change Volume Storage Type

  - Volume is just block data. You need to format it create specific file system e.g. ext4

  - Root Volume is one where OS is installed / booted. It is not encrypted by default on AWS AMIs
  
### EBS Volumes

  - EBS volume can be changed on the fly(except for magnetic standard)
  
  - Best practice is to stop the EC2 instance and then change the volume
  
  - You can change volume types by taking a snapshot and then using the snapshot to create a new volume
  
  - If you change a volume on the fly you must wait for 6 hours before you make another change
  
  - You can scale EBS volume up only

### RAID, Volumes & Snapshots.

  - RAID 0 – Striped, No Redundancy , Good Performance – No Backup/Failover

  - RAID 1 – Mirrored, Redundancy

  - RAID 5 – Good for reads, bad for writes. AWS doesn’t recommend using RAID 5 on EBS

  - RAID 10 – Raid 0 + Raid 1 - Good Redundancy , Good Performance - Done for very high I/O

  - Use RAID Arrays when a single volume IOPs are not sufficient for your need. E.g. Database. Then you create RAID Array to meet IOPs requirements.

  - To take snapshot of RAID Array –

    1. Stop the application from writing to cache and  flush all cache to Disk

    2. Freeze the file system

    3. Umount the RAID Array

    4. Shutdown the EC2 instance

  - Snapshots of encrypted volumes are encrypted automatically.

  - You can copy snapshot to another region while encrypting it.

  - Create Image from snapshot.

  - The EC2 instance thus created will have root volume encrypted.

  - You can’t share encrypted snapshots as the encryption key is tied to your account.

## EBS backed v/s Instance store

  - You can reboot or terminate instance store backed EC2 VMs

  - You can start, stop, reboot or terminate EBS backed EC2 VMs

  - EC2 instance on instance store is lost if host hypervisor fails. Not so with EBS backed instances.

  - EBS volumes can be attached / detached to EC2 instances. One at a time

  - EBS backed AMI is from EBS snapshot

  - Instance store back volume is from template in S3. Hence slower to provision

  - You will not lose data if you reboot for both.

  - With EBS, you can ask AWS not to delete the volume upon instance termination.

## EC2 Status Checks

There are two types of status checks: system status checks and instance status checks.

### System Status Checks

Monitor the AWS systems required to use your instance to ensure they are working properly. These checks detect problems with your instance that require AWS involvement to repair. When a system status check fails, you can choose to wait for AWS to fix the issue, or you can resolve it yourself (for example, by stopping and starting an instance, or by terminating and replacing an instance).

The following are examples of problems that can cause system status checks to fail:

  - Loss of network connectivity

  - Loss of system power

  - Software issues on the physical host

  - Hardware issues on the physical host that impact network reachability

## Instance Status Checks

Monitor the software and network configuration of your individual instance. These checks detect problems that require your involvement to repair. When an instance status check fails, typically you will need to address the problem yourself (for example, by rebooting the instance or by making instance configuration changes).

The following are examples of problems that can cause instance status checks to fail:

  - Failed system status checks

  - Incorrect networking or startup configuration

  - Exhausted memory

  - Corrupted file system

  - Incompatible kernel

## Load Balancers

  - The Classic Load Balancer that routes traffic based on either application or network level information, and the Application Load Balancer that routes traffic based on advanced application level information that includes the content of the request.

  - The Classic Load Balancer is ideal for simple load balancing of traffic across multiple EC2 instances, while the Application Load Balancer is ideal for applications needing advanced routing capabilities, microservices, and container-based architectures
  
  - Instances monitored by load balancers are reported as InService/OutOfService

## CloudWatch

  - Default Metrics – Network, Disk , CPU and Status check ( Instance and System)

  - Memory – RAM is a custom metric

  - You can create custom dashboards all CloudWatch metrics.

  - CloudWatch alarms – set notifications when particular thresholds are hit.

  - CloudWatch events help you respond to state changes. E.g. run Lambda function in response to.

  - CloudWatch logs helps you monitor EC2 instance/application/system logs. Logs send data to CloudWatch

  - Standard monitoring 5 mins. Detailed monitoring 1 minute - out of free tier.

  - CloudWatch is for logging. CloudTrail is for auditing your calls.

## AWS CLI Usage

  - Users can login with Access Key ID and Secret Access Key. If anything is compromised, you can regenerate the secret access key.

  - Also you can delete the user and recreate.

## IAM Roles for EC2

  - Avoid using user credentials on servers

  - IAM roles can be assigned/replaced to existing EC2 instances using AWS CLI. Not through the console.

  - A trick is to assign policies to the existing role. This will avoid the need to create new instances.

  - Role assigned to instance is stuck to the lifetime of the instance – until you delete the role. Easier to modify existing role by adding / removing policies.

  - Roles are universal. Applicable to all regions.

## Bootstrap scripts.

  - Scripts can be passed on to the EC2 instance at first boot time as part of user-data.

## EC2 Instance Meta-Data

  - curl [http://169.254.169.254/latest/meta-data/](http://169.254.169.254/latest/meta-data/)

  - curl [http://169.254.169.254/latest/user-data/](http://169.254.169.254/latest/user-data/)

  - Instance information is available in Meta-Data. Not in User-Data

## Auto Scaling 101

  - Before you can create Auto scaling group you need to create a launch configuration

  - Launch Configuration – Select AMI, Instance Type , Bootstrap script

  - No actual instances are created just with launch configuration

  - Auto scaling group – Set minimum size, spread it over subnets (AZs)- select all available AZs

  - Run health checks from ELB

  - Configure Auto scaling policy – Based on Alarm take action – trigger a new instance creation when CPU Utilization is greater than 90% for 5 minutes. You can also delete instance based on alarms

  - When Auto scaling group is launched it creates the instances based on definition.

## EC2 Placement groups

  - Logical grouping of instances within a single AZ

  - Instances can participate in low latency, 10 GBPs network.
  
## EFS(Elastic File System)

  - You pay only for the storage you use and can scale upto petabytes 
  
  - Unlike EBS, a EFS can be accessed by multiple EC2s - Acts like a central repository
  
  - Supports the NFSv4 protocol
  
  - Can support thousands of concurrent NFS connections
  
  - Data is stored across multiple AZs withing a region
  
  - Block based storage and not object based storage
  
  - Has read after write consistency

# Route 53

## DNS 101

DNS = Convert Human Friendly domain names into IP addresses.

IP4 (32 bit), IP6 (128 bits) - created to address exhaustion of IP addresses in IP4 space

VPCs are now IP6 compatible.

Top level domains vs second level domains

Domain Registrars - assign domain names under one or more top level domain names.

### Types of DNS Records -

1. SOA Record 

2. NS Record - AWS is now a Domain Registrar as well. 

3. A Record - fundamental 

4. CNAME - Canonical - resolve one domain name to another. Can’t use CNAME for Naked domains.

5. ALIAS record - only on AWS - are used to map resource record sets in your hosted zone to ELBs, Cloud Front Distribution, or S3 buckets that are configured as websites. E.g. you can have DNS names which point to ELB domain names -w/o the need for changing IP when ELB Ip changes.  Route 53 automatically recognizes changes in the record sets. Most common usage- map naked domain name (zone apex) to ELB names. Always use Alias v/s CNAME as Alias has no charges. Answering CNAME queries has a cost on Route53

6. AAAA Record – Ipv6

TTL - Cache the DNS record for TTL seconds. Before DNS migration, shorten the TTLs - so no more responses are cached. 

### Hosted Zone

Collection of resource record sets. NS, SOA, CNAME, Alias etc. types of records for a particular domain.

e.g. [https://www.tcpiputils.com/dns-lookup/google.com/ALL](https://www.tcpiputils.com/dns-lookup/google.com/ALL)

## Route53 Routing Policies

Most of the questions are scenario based.

1. Simple - Default - when a single resource performs function for your domain - only one webserver serves content

2. Weighted – send x% of traffic to site A and remainder (100 – x) % of it to site B. Need not be two different regions. Can be even two different ELBs.  This split is over length of day not based on number of individual subsequent requests.

Weights – a number between 0 and 255. Route53 calculates auto %age

AWS Takes Global view of DNS – not local / ISP view.

A/B testing is perfect use case for Weighted Routing policy

3. Latency – allows you to route traffic based on lowest network latency for your end user. To the region which gives fastest response time

Create record set for EC2 or ELB resource in each region that hosts website. When R53 receives a query it will then determine response based on lowest latency

How will the users get the best experience?  – evaluated dynamically by R3.

4. Failover – When you want to create an active /passive setup. DR site. R53 monitors health of site. If active fails then R53 routes traffic to passive site.   Here you designate a primary and secondary endpoint for your hosted zone record.

5. Geo-location – Choose where to route traffic based on geographic location of users.

Different from Latency based as the routing is hardwired irrespective of latency.

## DNS Exam Tips

  - ELBs cost money – ensure to delete them when not using.

  - ELBs always have DNS name – no public IP Addresses. Trick question might induce you into believing IP4 address for ELB

  - Remember difference between Alias and CNAME

  - Given a choice between Alias Record vs CNAME – always choose Alias. Alias records are free and can connect to AWS resources.

  - R53 supports zone apex records

  - With Route 53, there is a default limit of 50 domain names. However, this limit can be increased by contacting AWS support.

Naked domain – which doesn’t have the www in front of the domain e.g. acloud.guru. [www.acloud.guru](http://www.acloud.guru) isn’t

# Databases on AWS

## Databases 101

### RDBMS

RDBMS Types

  - MS-SQL Server

  - Oracle

  - MySQL

  - PostgreSQL

  - Aurora

  - MariaDB

### NoSQL DBs

Document Oriented

  - Dynamo DB

Collection = Table, Document = Row, Keys-Value Pairs = Fields

### Data Warehousing

OLTP (pulls out specific / narrow record set) vs OLAP – (pulls in large number of records). It used different architecture and infrastructure layer.  Differ in terms of queries run on top of data. OLAP is more about aggregation.

### ElastiCache

In memory cache in cloud.

  - Memcached

  - Redis

Exam – Improve database performance – e.g. top 10 deals of the day.

### Database Migration Service

Migrate production database to AWS. AWS manages all complexities of migration process. Source database remains fully operational. Both homogenous (Oracle to Oracle) as well as heterogeneous migrations are supported (Oracle to Aurora or Microsoft SQL). Can also be used for continuous data replication with high availability

**AWS Schema migration tool makes heterogeneous database**  - migrations  - easy by automatically converting the source database schema and a majority of the custom code, including views, stored procedures, and functions, to a format compatible with the target database. Any code that cannot be automatically converted is clearly marked so that it can be manually converted.

## RDS – Back Ups, Multi AZs & Read Replicas

OLTP systems.

### Backups

  - Automated Backups – full daily snapshot & will also store transaction logs.  

  - Enabled by default. Stored in S3. Free backup storage in S3 upto the RDS Instance size.  

  - You can define backup window. Choose wisely.

  - Backups are deleted when the RDS Instance is deleted.

### Snapshots

  - Done manually. They are stored even after you delete the instance.

  - You can copy snapshots across regions.

  - You can publish the snapshot to make it publically available.

  - Restoring Backups/ Snapshots – The restored version will be a new RDS instance with new end point.

  - You can check the instance size to restore.

  - You cannot restore to existing instance

### Encryption

  - Encryption at rest is supported for MySQL, SQL Server, Oracle and PostgreSQL & MariaDB.

  - Managed by AWS KMS.

  - Cannot encrypt an already present instance. To encrypt, create new instance with encryption enabled and then migrate your data to it.

### Multi-AZ Deployment

  - A standby copy is created in another AZ. AWS handles replication and auto-failover

  - AWS can automatically failover RDS instance to another instance.

  - In case of failover, No need to change connection string.

  - This can be used for DR purpose only. This option has to be selected at instance creation time. This option is not useful for improving performance / scaling.

### Read Replica Databases.

  - Read-replica – async data transfer to another RDS instance. You can actually read from these instances, unlike Multi-AZ deployments. You can also have read replicas of read-replicas up to 5 copies. (Watch out as async causes latency)-

  - Read-replicas can be used for Dev/Test environments, run certain workloads only against them and not against direct production deployment – Intensive workloads.

  - *MySQL , MariaDB, PostgreSQL only for read-replicas , no Oracle & SQL Server*

  - You cannot have read-replicas that have multi-AZ. However, you can create read replicas of Multi AZ source databases.

  - Read replicas can be of a different size than source DB.

  - Each read-replica will have its own DNS end point

  - Automatic backups must be turned on in order to deploy a read replica

  - Read Replicas can be promoted to be their own databases. This breaks replication. E.g. Dev/Test can be connected to the replica by first promoting it as DB itself.

  - Read Replicas can be done in a second region for MySQL and MariaDB – no PostgreSQL.

  - Application re-architecture is required to make use of Read replicas

  - Read replicas are not used for DR. they are used for performance scaling only.

## DynamoDB

  - Fast and flexible NoSQL database

  - Consistent, single digit millisecond latency.

  - Fully managed DB – supports both document based & Key-value data models.

  - Great fit for mobile, IoT, web, gaming etc. applications.

  - Stored on SSDs

  - Stored on 3 geographically distinct DCs (not AZs). Built in redundancy

  - Consistency

1. Eventual consistent reads - Consistency reached up to 1 second (default)

2. Strongly Consistent reads - Consistency reached after writes to all copies are completed. <1 second

Select type based on application needs

  - Pricing – Write Capacity Units and Read Capacity Units ($/hr.). Also Storage cost per month. You provision capacity in units/second. It can scale on the fly. Provisioned capacity.

  - Dynamo DB – Expensive for Writes. Cheap for Reads. Important point v/s RDS.

  - You can dynamically add columns – without the need to update other rows with the column data. As this is no RDBMS.

  - Reserved capacity is available for DynamoDB as well.

### RDS v/s DynamoDB

  - Use DynamoDB for Push button scaling. With RDS – to scale horizontally a new instance has to be created.

  - DynamoDB is cheap for reads and expensive for writes.

  - Observe workload characteristics and decide

  - Use RDS if data requires joins and relationships.

  - In RDBMS database structure cannot be dynamically altered. With DynamoDB you can.

## Redshift

Petabyte scale DW solution in cloud.  Used for OLAP – sum of various columns and joining the data.

### Configurations

  - Single Node – 160 GB. Used by Small and Medium Size businesses.

  - Multi-Node – Leader Node (handles all incoming connections & receives queries) & compute Node (store data and perform queries and computations – up to 128 Compute Nodes)

### Performance

  - Redshift is 10 times faster than usual OLAP systems.

  - It uses Columnar Data Store.  Columnar data is stored sequentially on storage system. Hence low I/O required – improving performance.

  - Advanced Compression (easier to do it via Columns instead of via Rows – which have different data types). Columns have similar type of data. Doesn’t use indexes and views – hence less storage required.

  - Based on data, appropriate data compression scheme is used.

  - Allows for massive parallel processing

### Pricing  

  - Based on Compute Node hours (compute node only – no leader node).

  - Backup and Data Transfer (only within VPC)

### Security

  - Transit encrypted via SSL,

  - At rest using AES-256 encryption

  - Can use your own HSM or default AWSK Key management.

### Availability

Not Multi-AZs. Can restore snapshots

Exam Tips – Database warehousing service, cheap, faster. Best seller AWS Service. Speed achieved due to columnar storage. And Data stored sequentially on disk – hence faster.

## ElastiCache

  - Easy to deploy, operate and scale an in-memory cache in the cloud.

  - Improve performance by avoiding repeated calls to DB.

  - Improve latency and throughput for read-heavy applications.

  - Can be used for compute intensive data

### Memcached

  - All Memcached tooling can be easily ported over.

### Redis

  - Supports Master / Slave replication and multi-AZ deployment to get redundancy.

Exam Tips

  - ElastiCache is used if DB is primarily read-heavy and not frequently changing

  - Use Redshift – if application is slow due to constant OLAP transactions on top of OLTP focused DB.

## Aurora

  - Bespoke Database Engine.

  - It is MySQL compatible.

  - However you can’t download and install on your workstation.

### Performance

5 times better performance than MySQL. At a fraction of cost as compared to Oracle.

### Scaling

  - Outset 10 GB Storage, auto increment of storage up to 64 TB

  - No Push button scaling – unlike DynamoDB

### Fault Tolerance

  - Maintains 2 copies of your data in at least 3 availability zones. This is for the Data only not for the instances that runs the Database.

  - 2 copies lost – no impact on write availability.

  - 3 copies lost – no impact on read availability.

  - Storage is self-healing.

### Replicas

  - MySQL Read Replica can be created from the Aurora source DB.(up to 5 of them)

  - Aurora Replicas – up to 15 of them. If leader crashes, the replica with the highest tiers becomes the leader. While creating replicas, remember to assign different tier levels.

  - Cluster Endpoint vs Individual Endpoint

No Free Tier usage available. Also available only in select regions. Takes slightly longer to provision

## Exam Tips

  - Why you can’t connect to DB Server from DMZ. Check the security group – if it is removed or added

  - Have separate groups for EC2 Instance and RDS Instance.

  - Multi-AZ for Disaster Recovery only. Not for performance improvement. For performance improvement use, multiple read-replicas

  - Dynamo DB v/s RDS

If you want push button scaling, without any downtown, you will always want to use DynamoDB.

With RDS scaling is not so easy, you have to use a bigger instance or add read replicas (manual process).

  - If you are using Amazon RDS Provisioned IOPS storage with a MySQL or Oracle database engine, what is the maximum size RDS volume you can have by default? – **6TB**

  - What data transfer charge is incurred when replicating data from your primary RDS instance to your secondary RDS instance? - **There is no charge associated with this action**.

  - When you have deployed an RDS database into multiple availability zones, can you use the secondary database as an independent read node? – **No**

  - RDS automatically creates RDS Security Group w/ TCP port # 3306 enabled. 

  - In VPC Security Group, the answer would be YES because you will have manually specify access to port & protocol.

# VPC

Important section for all exams☺. You should be able to build out own VPCs from memory.

## Introduction

  - VPC is a logical data center within an AWS Region.

  - Control over network environment, select IP address range, subnets and configure route tables and gateways.

  - Do not span regions, but can span AZs.

  - Can create public facing subnet (Web) having internet access and private facing subnet (DB) with no internet access

  - Public Subnet – Web Servers/ Jump Boxes

  - Private Subnet – Applications Servers / Database servers

  - Leverage multiple layers of security – Security groups and Network ACLs to control access to EC2 instances

  - Create hardware VPN connection between your local DC and AWS.

  - AWS gives a maximum of /16 network.

  - Bastion host/ Jump Box in Public subnet

  - Security groups, Network ACLs, Route Tables can span subnets/AZs.

  - Each subnet is always mapped to an availability zone. 1 subnet = 1 AZ

  - Only one internet gateway per VPC. [Trick question – improve performance by adding Gateway – just not possible]

  - Security groups are stateful. Network ACLs are stateless.

By default, how many VPCs am I allowed in each AWS Region? == 5

Typical Private IP address ranges – not publically routable.

  - 10.0.0.0 - 10.255.255.255 (10/8 prefix)

  - 172.16.0.0 - 172.31.255.255 (172.16/12 prefix)

  - 192.168.0.0 - 192.168.255.255 (192.168/16 prefix)

VPC Diagram - Public and Private subnets ![VPC with Public and Private subnets](VPC-Diagram.jpg)

To use AWS Stencils download them at the [AWS Simple Icons for Architecture Diagrams](https://aws.amazon.com/architecture/icons/) site

## Default v/s Custom VPC

  - When you create an account a default VPC is created for you in each Region.

  - All subnets in default VPC have a route out to the internet

  - Each EC2 instance in default VPC will have a public and private IP address

  - If you delete default VPC, only way to restore it is by contacting Amazon.

## Custom VPC Info

  - Default Security group, network ACL & route table are created for each custom VPC you create.

  - Doesn’t create subnets or internet gateways out of the box.

  - In each VPC you create, 5 IP addresses are reserved by AWS for itself. First 4 and last IP in the CIDR block.

  - You can't change the size of a VPC after you create it. If your VPC is too small to meet your needs, create a new, larger VPC, and then migrate your instances to the new VPC. To do this, create AMIs from your running instances, and then launch replacement instances in your new, larger VPC. You can then terminate your old instances, and delete your smaller VPC. 

  - You can’t attached multiple Internet Gateways to the VPC to boost performance.

  - When creating VPCs do not modify default route table to add your custom rules. If you modify the default route, it will affect all instances. Create a new route table for customization.

## NAT Instance & NAT Gateway

  - NAT Instance is one EC2 instance. You are responsible for performance management, scale out and security groups. NAT Gateway is a managed service.

  - On NAT instance, *remember to disable source/destination IP check*. This is required to allow private subnet internet connectivity. This is not required on NAT Gateway.

  - Allow both HTTP and HTTPS access on security groups associated with NAT instances. Security groups are always associated with NAT Instances.

  - Both *NAT Instance and NAT Gateways are deployed to public subnet*. Elastic IP has to be added to NAT Instance. NAT Gateway is automatically assigned a public IP.

  - In VPC, update default route table to allow connectivity from Private subnet to NAT Instance and Gateway

  - NAT instance is single point of failure. You can place NAT instance behind Auto Scaling group, multiple subnets in different AZs and scripted failover. To improve performance increase the size of the NAT instance to allow for higher throughput.

  - You can use Network ACLs to control traffic for both NAT Instance and Gateway.

  - NAT Gateways scale up to 10GBps. No need to disable source/ destination checks on Gateways.

## Network ACLs & Security Groups
|Security Group| Network ACL|
|-------------|-------------| 
|Operates at the instance level (first layer of defense)| Operates at the subnet level (second layer of defense)|
|Supports allow rules only| Supports allow rules and deny rules|
|Is stateful: Return traffic is automatically allowed, regardless of any rules| Is stateless: Return traffic must be explicitly allowed by rules|
|We evaluate all rules before deciding whether to allow traffic| We process rules in number order when deciding whether to allow traffic. Lower order rules take effect in case of conflict with higher order rules.|
|Applies to an instance only if someone specifies the security group when launching the instance, or associates the security group with the instance later on| Automatically applies to all instances in the subnets it's associated with (backup layer of defense, so you don't have to rely on someone specifying the security group)|


  - With default ACL, all inbound and outbound traffic is allowed automatically

  - When custom ACL, all inbound and outbound traffic is denied by default

  - 1 subnet <=> 1 AZ <=> 1 ACL.  ACLs can be associated to only 1 subnet at a time. You can reassign to another subnet. If subnet is not associated with an ACL, the default ACL is applied.

  - AWS Recommends adding ACL rules in increments of 100s

  - Ephemeral ports – Allow inbound /outbound traffic from 1024 – 65535. As clients can initiate outbound connection from any random port. Ports < 1024 reserved for super user access.

  - If you have to block a specific IP address / range, use ACLs instead of security groups. SGs can’t deny traffic – they only allow.

## Custom VPC & ELB

  - To have HA in general or for ELB, ensure that you have at-least 2 public and or private subnets in different availability zones.

## NAT & Bastion

  - You cannot use NAT instance to SSH / RDP into private subnet. For that Bastion (Jump Box) is required.

  - Bastions are used for secure administrative tasks only. Bastions are placed in Public subnets and connect to private subnets via private IP

  - For Bastion HA, have multiple Bastions in different AZs – at least 2 public subnets. Auto scaling in multiple AZ, route 53 doing health checks.

  - NAT instance is used to provide internet connectivity to private subnets.

## VPC Flow Logs

  - Enable Flow Logs for Custom VPC to see all traffic.

  - Enable to capture IP traffic flow information for the NICs of your resources. All information is reported to CloudWatch

  - Create IAM role to allow all logs to flow into CloudWatch

  - Create log group in CloudWatch and inside that create stream where you can then see all the traffic flow.

# Application Services

## SQS – Simple Queue Service

  - SQS is a distributed web service that gives you access to a message queue that can be used to store messages while waiting for a computer to process them.

  - SQS helps decouple the components of an application so they can run independently.  

  - Messages can be retrieved via SQS API

  - The producer and consumer can run at their own independent throughput.

  - The queue acts as a buffer between consumer and producer. Ensures delivery of messages at least once. Ensure your application isn’t affected by processing the same message multiple times.

  - Allows multiple readers and writers. Single queue can be used simultaneously by various applications – helps scale out applications

  - SQS Message size up to 256KB of text in any format. May consist of 1-10 messages.

  - Does not guarantee FIFO messages. If order is important, add sequencing information in each message.

  - For SQS, you have to pull messages. It doesn’t push messages – unlike SNS. You are billed at 64KB Chunks

Pricing

  - First 1 million SQS Requests per month are free.

  - $0.50 per 1 million SQS requests per month thereafter.

  - 64KB chunk = 1 request. So a message of 256KB = 4 requests.

  - Each messages has a visibility timeout – 12 hours by default. Visibility timeout period only starts when a worker node has picked up the message for processing. During this interval, the message is invisible to other processor workers.

  - SQS can do auto-scaling. If queue grows beyond a threshold, instantiate new web/app servers. Use Auto scaling + SQS to achieve this.

Exam Tip - De-couple ➔ SQS

## SWS – Simple Workflow Service

  - SWS is a web service that makes it easy to coordinate work across distributed application components. Co-ordinate tasks & workflows.

  - Amazon uses SWS to process orders on its website.

  - No EC2 components involved.

  - It can also involve human actors.

Trick Question – when to use SQS or SWS

|Attribute|SQS|SWS|
|----|----|----|
|Retention |14 days|1 year|
|API|Message Oriented|Task Oriented|
|Assignment|Might be assigned multiple times|Only once|
|State|Write code to implement tracking|Keeps Track of State & Events|

SWS Actors

1. WF Starters – e-commerce application

2. WF Deciders – Control flow of activity tasks.

3. WF Activity workers – Carry out actual task

## SNS – Simple Notification Service

  - Makes it easy to setup, operate and send notifications from the cloud.

  - Immediate delivery to subscribers or other applications

  - SNS consists of Topics and you can publish messages to topics.

  - You can send emails, text and other alerts. Apple Push, Android etc.

  - Publish messages to SQS queues, trigger Lambda functions.  Lambda function can then manipulate information and then send to other SNS Topics

  - SNS is Push based messaging.

  - You can group multiple recipients using topics. Recipients can subscribe to topics to receive notifications.

  - Flexible message delivery over multiple protocols.

  - Is used in conjunction with CloudWatch and AutoScaling.

EC2 instances pull SQS messages from a standard SQS queue on a FIFO (First In First out) basis.  – False

## Elastic Transcoder

  - Allows to convert media files from source to different media formats.

  - You pay the minutes you transcode and the resolution

  - S3 → Lambda Function → E. Transcoder → S3

## API Gateway

  - Managed web service which enables developers to publish, monitor and secure APIs at any scale.

  - Create an API that acts as front door for applications to access data, business logic or any functionality from your backend services

  - API Caching – Cache your endpoint’s responses. Reduces load on endpoints based on duration of TTLs

  - Low cost & Efficient. Scales

  - Throttle requests as required to prevent attacks.

  - Log requests to CloudWatch.

  - For application built on top of multiple domains, you need to enable CORS on API Gateway.

## Amazon Kinesis

  - Streaming data is something which is generated by thousands of data sources – stock prices, game information, social network data, geo-spatial data, purchases from online stores, IoT sensor data.

  - Kinesis is an AWS platform to analyze streaming data.

  - Kinesis Streams
        - Stores data for 24 hours to 7 days.
        - Data stored in **shards**.
        - Data consumers (EC2 instances) analyze the stream and then derive results/take next actions.
        - Data capacity of stream is a function of the number of shards you specify for the stream.

  - Kinesis Firehose 

      - Don’t have to worry about shards, streams – completely automated.
      - No automatic data retention window. Data is either immediately analyzed or sent to S3 and then to Redshift, elastic search cluster
      - Data is immediately analyzed via **Lambda**.

  - Kinesis Analytics –

      - Run SQL type queries on top of data contained in Streams or Firehose and store the results in S3 / Redshift and Elastic Search cluster.

# Well Architected Framework

Framework developed by various SAs based on their experience with customers

It is a set of questions to check how well aligned is your architecture to best practices

**4 Pillars of WAF**

1. Security

2. Reliability

3. Performance Efficiency

4. Cost Optimization

Each Pillar has Design Principles, Definition, Best Practices, Key AWS Services these pillars apply to.

**General Design Principles**

1. Stop guessing your capacity needs.

2. Test systems at production scale – Use Cloud Formation and test in other regions

3. Lower risk of architecture change.

4. Automate to make architecture experimentation easier.

5. Allow for evolutionary architectures. (E.g. Physical servers earlier you are stuck with it but now Cloud you can move to newer cloud features as soon as they are available.)


### Design Principles

1. Apply security at all layers.

    1. Not just edge firewalls. Apply it a subnet level , ACLs , which ports used on ELB, instances

    2. Run anti-virus on Windows instances

2. Enables traceability

3. Automate responses to security events – E.g. SNS notification for ssh

4. Focus on securing your system.

5. Automate security best practices. – Use hardened AMIs

6. AWS Shared Responsibility Model – Customer responsible for data and OS. AWS responsible for security of underlying infrastructure & as a service offerings – RDS etc.

### Security Areas

  1. Data protection
  2. Privilege management
  3. Infrastructure protection
  4. Detective controls

### Best Practices

1. Data protection

  - Basic data classification should be in place. Organize data into segments. Who should have access to data? Implement least privilege principle
  - Encrypt everything where possible – both at rest and in transit
  - AWS customers maintain full control of their data
  - AWS makes it easier for you to encrypt your data and manage keys – KMS or by a customer
  - Detailed logging available.
  - AWS systems are exceptionally resilient.
  - Versioning can be used as data lifecycle management.
  - AWS never initiates movement of data between regions unless a feature is enabled or leverages a services

How are you encrypting data at rest and transit (SSL)? – ELB, EBS, S3, RDS

2. Privilege management

  - Allow only authorized and authenticated users are able to access resources. This is achieved via
  - ACLs,
  - RBAC – Role based access control
  - Password Management

How are you protecting access to and use of AWS root account credentials?

How are you defining roles and responsibilities of system users to control human access to AWS Console and APIs – e.g. Groups for system admins, group for HR and other departments?

How are you limiting automated access to AWS resources? – Application scripts, tools – by using roles

How are you managing keys and credentials?

3. Infrastructure protection

How do you protect your data center – RFID controls, security, CCTV etc?

Infrastructure protection essentially exists at VPC level – Physical infra is managed by AWS

How are you enforcing network and host-level boundary protection? E.g. Jump host. Local down which ports can be used.

How are you enforcing AWS Service level protections? Are you using IAM?

How are you protecting integrity of operating system?

4. Detective controls

Detect or identify a security breach

AWS Services which can help

  - CloudTrail

  - CloudWatch

  - Config

  - S3

  - Glacier

How are you capturing and analyzing your AWS logs. CloudTrail is a regional service. Which 3rd party tools you are using for this analysis.

  2. Reliability / Fault Tolerance

  - Ability of system to recover from service or infrastructure outages/disruptions

  - Ability to dynamically scale

### Design Principles

  - Test recovery procedures. E.g. Netflix simian army

  - Automatically recover from failure – anticipate and recover from failure

  - Scale horizontally to increase system availability

  - Stop guessing capacity – don’t under provision or over provision

### Areas of Reliability

  - Foundations

  - Change Management

  - Failure Management

### Best Practices

  - Foundations

E.g. side of communication link between HQ and Data Center

AWS handles networking and compute resources. However, there are service limits to stop customers from overprovisioning. You can request increase

How are you managing AWS Service Limits?

How are you planning your network topology on AWS?

Do you have an escalation path to deal with technical issues?

  - Change Management

Aware of how software changes affect environments.

With AWS use CloudWatch to monitor your environment. Traditional IT Change control is not required in cloud.

How system adapts to change in demand?

How you monitor AWS resources?

How you execute change management.

  - Failure Management

Architect systems assuming failure will occur.

How are you backup up data?

How does system withstand component failure?

How are you planning for recovery?

### Key AWS Resources

  - Foundations – IAM, VPC

  - Change Management - CloudTrail

  - Failure Management - CloudFormation


3. Performance Efficiency

Focuses on how to use computing requirements efficiently to meet business needs. How to manage efficiency as demand changes and technology evolves. Constantly question current architecture vis-a-vi current available services

### Design Principles

  - Democratize advanced technologies. Team can consume advanced technologies as services instead of building expertise. E.g. DynamoDB, Machine Learning. Etc.

  - Go global in minutes.

  - Use server-less architecture

### Areas of Performance Efficiency

  - Compute

  - Storage

  - Database

  - Space-time trade off

### Best Practices

  - Compute – choose the right kind of server – CPU intensive or Memory intensive.

How do you select appropriate instance type?

How do you continue to use appropriate services / architectures with new instances types?

How do you monitor instances?

How to ensure quantity of instances matches demands?

  - Storage

Which storage solution to use depends on number of factors?

Access Method – Block, file or Object

Patterns of Access – Sequential or Random

Throughput Required

Frequency of Access – Online, offline or archival

Frequency of Update – Worm, Dynamic

Availability constrains

Durability constrains –

How do you use select appropriate storage solution?

How do you ensure that you have the most appropriate storage solutions with new instance types?

How do you monitor your storage solution to ensure performance?

  - Database

Do you need consistency, HA, DR needs, No-SQL

How do you selected appropriate solution for system?

How do you ensure that you have the most appropriate database solutions with new solutions launched?

How do you monitor your database solution to ensure performance?

How do you ensure capacity matches demand?

  - Space-time trade off

  - Use RDS to add read replicas

  - Use Direct Connect to provide predictable latency

  - Use global infrastructure to have multiple copies of your environment, closest to your users

  - Use caching services like ElasticCache or CloudFront

How do you selected appropriate proximity and caching solution for system?

How do you ensure that you have the most appropriate proximity and caching solutions with new solutions launched?

How do you monitor your proximity and caching solution to ensure performance?

How do you ensure proximity and caching capacity matches demand?

### Key AWS Resources

  - Compute – Auto scaling
  - Storage – EBS, S3, Glacier
  - Database – RDS, DynamoDB , Redshift
  - Space-time trade off – CloudFront, ElastiCache, Direct Connect, RDS Read Replicas, etc. – anything that will lower latency or time to access service.

  4. Cost Optimization

Use cost to minimum and use the savings in other parts of business.

### Design Principles

  - Transparently attribute expenditure – tag who spends how much and optimize accordingly

  - Use Managed services to reduce cost of ownership

  - Trade Capital Expense for Operating Expense.

  - Benefit from economies of scale

  - Stop spending money on data center operations

### Areas for Cost Optimization

  - Match supply and demand

  - Cost effective resources

  - Expenditure awareness

  - Optimizing over time

### Best Practices

  - Match supply and demand – don’t over or under provision. Use Auto scaling or Lambda for serverless. Pay only when used. Use Cloud Watch

How do you ensure capacity matches and does not substantially exceed your need?

How do you optimize your usage of AWS resources?

  - Cost effective resources

Use the correct instance type.  A well architected system will use the most cost efficient resources to reach the end business goal.

Have you selected appropriate resource type to match cost targets?

Have you selected the appropriate pricing model?

Are there managed services which can be used to improve ROI?

  - Expenditure awareness

Siloed AWS Accounts in the same organization. Need to be aware which team is spending where. Also use 3rd party tools and tags. Billing alerts.

Consolidated billing

What access controls are in place to govern AWS costs?

How are you monitoring usage and spending?

How are you decommissioning resources you don’t need or stop that are temporarily not needed?

How do you consider data transfer changes?

  - Optimizing over time

AWS Constantly changing. What is good today might not be so good next time around when newer changes are released.

Subscribe to AWS Blog

Use AWS Trusted Advisor

How do you manage and/or consider adoption of new services

### Key AWS Services

  - Match supply and demand – Auto scaling

  - Cost effective resources – EC2 (reserved instances), AWS Trusted Advisor

  - Expenditure awareness – CloudWatch alarms, SNS

  - Optimizing over time – AWS Blog, AWS Trusted Advisor

# Additional Exam Tips

Side Note - Difference between Object Store (Files) and Block Store (DB). Dropbox uses S3 to store the actual data and metadata is stored in their own data centers.

## AWS Exam Tips

1. Kinesis - process large streams of data. To process data - Amazon Redshift and Elastic Map Reduce

2. EBS Instance Store vs EC2 instance store - EBS - Block store, long term storage can be attached/detached to different EC2 instances. However, attached to only 1 instance at a time. Data on the EBS volume will persist even after the instance is stopped. EC2 instance store is ephemeral – can’t be attached to multiple EC2 instances.

3. OpsWorks - Orchestration service that uses Chef - keywords *Chef, Recipes, Cook Books*. Infrastructure as Code

4. Elastic Transcoder - Convert media files into formats for various formats optimized for devices on the cloud. Don’t need to guess settings for various devices. Pay for minutes you transcode and minutes you transcode.  

5. SWF Actors - workflow starters, deciders and activity workers.

6. EC2 - get public ip - it’s in instance meta-data and not user data. Access link [http://169.254.169.254/latest/meta-data](http://169.254.169.254/latest/meta-data/local-ipv4)[/local-ipv4](http://169.254.169.254/latest/meta-data/local-ipv4)  - wget or curl.  User data is the shell script provided to the EC2 instance at startup. The user data is executed only once at boot time.

## Consolidated billing

  - Separate Paying Account and independent department / environment accounts.

  - Get granular control on expenditure per account.

  - Get volume discounts based on aggregate usage.

  - Current soft limit of 20 accounts to consolidate

## Cross Account Access.

  - Improve productivity for a multi account / multi role accounts on the AWS console, without the need to sign in again.

  - Grant access to different accounts for users

  - Need to explicitly set policies, roles accordingly.

## Resource Groups / Tagging

  - It is a collection of resources that share one or more tags.

  - Key value pairs attached to AWS resources. Tags can be inherited from other services that create them.

  - Once single dashboard for groups fulfilling a certain criterion on tags.

  - Can help track all the resources that you have spawned. And also learn about hidden resources – ones which you forgot that you created earlier.

  - Use tag editor to find resources that are not tagged.

## VPC Peering

  - Connection between 2 VPCs that allows you to route traffic between two VPCs using private addresses, without the need to traverse the internet or any gateway.

  - You can create VPC peering between own VPC or between another account *in the same region*

  - Ensure that the address space does not overlap.

  - Daisy chaining of VPC connections not possible. You need to setup individual connections between each VPC.

## Direct Connect

  - Establish dedicated network connection from your data center to AWS.

  - You can avoid using regular internet route. This is a dedicated, private network connection.

  - VPN connections are routed over internet. Can be setup in minutes.

  - AWS Direct Connect lets you establish a dedicated network connection between your network and one of the AWS Direct Connect locations. 

  - Direct Connect takes weeks/ months to setup

  - Helps reduce bandwidth cost. Consistent network performance and private connectivity to AWS VPC.

## Active Directory Integration

  - AD Connector – interface to your internal AD implementation on premise

  - You can authenticate to AWS console using AD credentials via SAML

  - After you authenticate to AD, then temporary token credentials are generated to allow you to login to the console.

## Workspaces.

  - VDI on the cloud. Replacement for physical desktop.

  - Access the desktop by workspace clients or browsers

  - Don’t need an AWS account to access workspaces. Administrators can setup authentication via existing AD domain.

  - Runs Windows 7 experience

  - Provides local administrator access.

  - Workspaces are persistent

  - All D: / data is backed up every 12 hours.

Q&A which I got incorrect.

1. What does an AWS Region consist of? - A distinct location within a geographic area designed to provide high availability to a specific geography.

2. Which AWS service is effectively a NAS in the cloud, allowing you to connect it to multiple EC2 instances at once? - EFS (Elastic File System). Note difference from EBS which is directly attached to an EC2 Instance. 

3. You need a service that will aggregate your data from multiple data sources (S3, DynamoDB, RDS, etc.) and provide business intelligence based on this data. Which AWS service should you use? - Quick Sight
