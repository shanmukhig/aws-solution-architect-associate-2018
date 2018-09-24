# aws-solution-architect-associate

all the aws solution architect associate (2018) exam related materials will go here...

exam blue print
 - 65 questions
 - 130 minutes duration
 - once the timer started, can't stopped or paused
 - for me it took 80 mins to complete all the questions, and used rest of the time for rechecking answers (though i haven't changed any answers)
 - need to get 72% for passing the exam
 - questions are either multiple choice, or multiple answer (more than one answer correct)
 - need to carry 2 photo id cards to the exam center
 - the alternate answers of each question always confusing so be careful while picking the right answer
  - tip: read question carefully and multiple times before deciding answer
 - after completion of the exam, you will be told either pass or fail
 - details results will mailed with in 5 days of completing the exam
 - the same can be accessed from (http://certmetrics.com/amazon/default.aspx)
 - for me the exam stuck half the way, and had to contact aws support for fixing the issue (15-20mins were lost because of this)

i have attended following courses while preparing for the exam which may help you:

 - https://www.udemy.com/aws-certified-solutions-architect-associate/
 - https://www.udemy.com/linux-academy-aws-certified-solutions-architect-associate-free/
 - https://www.udemy.com/aws-certified-solutions-architect-associate-exam/


as aws releasing new features every day, the course contents will get outdated. While preparing for the exam it is always advisable to refer original documentation for the exat numbers. 

For examle, 
 - initially, S3-IA reliability is 99.9%, the latest is 99.99%
 - SQS now supports KMS encryption along with other encryption formats, ealier it is not the care
 - now any message published to SQS can trigger a lambda, earlier this year, it is not the case
 - and many more scenarios like this

now the course is re-designed to use following topics:

Define Operationally Excellent Architectures 6%
Define Performant Architectures 24%
Design Cost-Optimized Architectures 10%
Design Resilient Architectures 34%
Specify Secure Applications and Architectures 26%

my experience after writing the exam:

 - well architected framework
  - i memorized it like (srp co)
  - s - security
  - r - resilient systems
  - p - performance efficiency 
  - c - cost optimization
  - o - operational excellence
  - read and understand the concepts very well before going to the exam
  - the final score card also giving based on these topics only 
 - get as much hands on with aws components as possible. theoretical knowledge may not work always
 - vpc (important exam topic)
  - get good hands on experience on virtual private cloud (vpc) and related functionalities
  - it is very important concept in the exam, and probably don't attend the exam with learning vpc thoroughly
  - topics include vpc, cidr blocks, address ranges, limits, subnets, route tables, nat gateway, nat instance, etc.
  - should be able to draw any vpc on paper looking at the question. this helps a lot in the exam.
  - through knowledge on differences between:
    - nacl and security group,
    - nat instance and nat gateway
    - vpc peering is also important (pcx)
 - get good hands on knowledge on ec2
  - a through understanding of launch configurations, auto scaling, scale-in, scale-out logic (default, user defined),
  - default instance termination policies while scaling-in
 - though knowledge on load balancers:
  - classic load balancers
  - network load balancers
  - application load balancers
  - ssl termination policies
  - elb limitations
  - target groups
  - elb health monitoring
 - ec2 - the backbone of aws (very important exam topic) 
  - Amazon EC2 instances are grouped into 5 families: 
  - General Purpose - General Purpose Instances have memory to CPU ratios suitable for most general purpose applications and come with fixed performance (M5, M4) or burstable performance (T2);
  - Compute Optimized -  Compute Optimized instances (C5, C4) have proportionally more CPU resources than memory (RAM) and are well suited for scale out compute-intensive applications and High Performance Computing (HPC) workloads;
  - Memory Optimized - Memory Optimized Instances (X1e, X1, R4) offer larger memory sizes for memory-intensive applications, including database and memory caching applications;
  - Storage Optimized - Storage Optimized Instances (H1, I3, D2) that provide very high, low latency, I/O capacity using SSD-based local instance storage for I/O-intensive applications, with D2 or H1, the dense-storage and HDD-storage instances, provide local high storage density and sequential I/O performance for data warehousing, Hadoop and other data-intensive applications.
  - Accelerated Computing instances.    Accelerating Computing instances (P3, P2, G3, F1) take advantage of the parallel processing capabilities of NVIDIA Tesla GPUs for high performance computing and machine/deep learning; GPU Graphics instances (G3) offer high-performance 3D graphics capabilities for applications using OpenGL and DirectX; F1 instances deliver Xilinx FPGA-based reconfigurable computing; 
  - When choosing instance types, you should consider the characteristics of your application with regards to resource utilization (i.e. CPU, Memory, Storage) and select the optimal instance family and instance size.
  - instance types, creating, terminating, life cycle policies
  - different types of storage like:
    - instance storage, block storage, efs, ebs - cold hdd, hdd, general purpose ssd, provisioned IOPS etc
    - different storage type life cycles,
    - snapshots, volumes, images etc.
    - az, region specific limitations of volumes, snapshots
    - ebs volume backup and related to details 
      - snapshots are only accessible in the source region by default, 
      - volumes are accessible only in the source az, etc.
    - knowledge around raid levels (raid 0, raid 1, raid 10, aws doesn't recommend raid 5)
  - hands on knowledge on bootstrapping ec2 volumes during launch
  - different types of ec2 instance families (T, M, F, D, G etc)
  - ec2 limitations
 - route 53
  - routing policies
   - geo based
   - latency based
   - weightage based
   - failover (active - active, active - passive)
   - a, cname, alias record types
 - db
  - ebs hosted sql
  - rds mysql, mssql, aurora (now it is part of the exam)
  - dynamodb (now scenario based questions)
  - different options like snapshots, backup, limitation
  - dynamodb, 
   - global secondary index, local secondary index, 
   - read capacity units, write capacity units, 
   - fault tolerant, high availability concepts, 
   - replication (though aws takes care of it, but need to know, dynamo db automatically replicates tables to 3 distinct "data centers" not az/region)
   - message sizes, data types
 - s3 (very important exam topic)
  - bucket naming policies (names should be dns complaint and can be up 1024 chars long)
  - bucket name should be unique with in aws
  - s3 is global, not region specific, but buckets can be limited to local
  - different s3 tires (s3-ia, s3-rrs/s3-onezone, glacier)
  - min, max object sizes 
   - s3 - standard,
    - min size 0kb, max size 5tb, while uploading data over internet, max size of object is 5GB
    - objects bigger than 100MB should use multipart uploads
    - availability - 99.99%, reliability - 99.999999999% (eleven 9s)
   - s3 - ia
    - min object size 128KB,
    - same as s3 - standard, but cheaper
    - when a object is stored/pulled, billed for minimum of 30days
    - availability - 99.99%, reliability - 99.999999999% (eleven 9s)
    - suitable for less frequently used data (like patent records, monthly reports where data of previous months not required)
   - s3 - rrs/s3-one zone:
    - availability - 99.9%, reliability - 99.99%
    - should only store less important or reproducible data like thumbnails, logs files, etc.
    - low cost storage
   - glacier
    - archival vault
    - default retrieval time takes (3-5 hours), also called first byte latency
    - retrieval time can be accelerated (costs additional charges, can be in in minutes)
  - s3 lifecycle policies
  - 100 buckets per account
  - cross region replication (aws never initiates or moves data out of a user selected region, unless otherwise, user configures to replicate or move)
  - static web hosting, url redirection
  - ipv4, ipv6
  - versioning, mfa delets
  - eventual consistency
  - object naming constraints
  - cloud front (aws cdn) - for distributing static content
  - cloud front security policies etc.
 - sqs, sns, ses
  - sqs queue timimgs like 
   - default visibility timeout
   - default message validity periods (4 days, max 14 days)
   - message size limitations (256KB)
   - sql long polling/short polling
   - use sqs when ever the question sounds like de-coupling/loose coupling/bottleneck etc
   - sns topics, delivery options like email, email-json, sms, sqs, lambda
   - ses limitations (i didnt get any questions on ses, though it may be important)
 - security
  - data encryption at rest (SSE)
  - data encryption during transit (ssl/tls)
  - server side encryption
   - AES - 128bit, 198bit, 256bit encryption
   - SSE - KMS
    - aws manages the keys
    - keys can be rotated
    - master key and child keys
    - key rotation policies
    - usage of keys logged and can be audited
   - SSE - S3
    - same as above
   - SSE - C
    - customer provided keys, but managed by aws
    - customer is responsible for maintaining another copy of key in a safe place
    - customer may rotate keys on his own
   - cloud hsm and hardware hsm (good to know)
  - client side encryption
   - aws encryption library (same as below)
   - customer's own encryption/decryption library - 
    - customer is responsible for managing encryption keys, 
    - encrypting data before storing, 
    - decrypting after downloading
 - iam - identity and access management (must known topic for exam)
  - users
  - groups - logical grouping of users
  - roles - for assigning to aws resources
   - like create and assign a role to ec2 instance for storing data in s3, instead of storing the keys in ec2 instance
    - much secure as there is no management of keys
  - policies
   - can be attached to uses and roles
   - a json document
  - know different use cases like
   - using roles and policies instead of storing keys for accessing aws services
   - generating keys
   - password policies
   - customizing user url
 - lambad (serverless computing) (now aws serverless components are part of exam questions)
  - different use cases of lambda like
   - api gateway
   - sns targets
   - dynamodb stream targets
   - kinesis stream processing and analytics
   - pay as you go pricing
 - api gateway
  - elasticity, high availability, pay as you go restful services
  - you can build restful api backed by lambda
 - kinesis (now it is part of the exam, and expect complex scenarios)
  - kinesis stream,
  - kinesis firehose,
  - kinesis analytics
  - concepts like shards, kcl etc
 - cloud formation (now part of the exam and need to have hands on experience)
  - templates, nested templates
  - stacks, stack sets
  - understand how to create and at least how to read and understand a given template
 - elastic bean stack, containers, ecs etc
  - i got couple of questions in the exam on elastic bean stack
 - cloudwatch
  - know how to collect logs, log aggregation mechanisms
  - triggers
   - for backing up snapshots, or any other actions
  - monitors
  - rules
  - ec2 instance health monitoring and replacing/restarting unhealthy instances
  - events
 - cloud trail
  - used for monitoring and tracking changes to the aws environment setup
  - use it for statutory compliance (can be enabled or disabled optionally)
 - trusted advisor
  - scans a given aws account and suggests any security vulnerabilities
  - free tier has a limitation for features
 - elasticache
  - memcache (multi-threaded usage)
  - redis (supports, sort sets, supports auto increment, decrement options), a chose for game boards etc

last but not least, read **faq** of all the above mentioned topics before taking the exam
