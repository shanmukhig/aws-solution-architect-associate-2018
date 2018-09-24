  <code>

  These exam questions are collected from various sources and may not be exact questions that would come in the exam. Just for training purpose only!!!
  
  001 Qestion: You are a solutions architect working for a large pharmaceutical company who are involved in high performance computing to develop new drugs to treat arthritis. You are helping them to design a new application which will need to keep network traffic the lowest latency possible while leveraging very high CPU performance. They would like to place this solution on to the AWS platform and are looking for your recommendations. Which of the following do you suggest  ?
    A. CPU optimized EC2 instances deployed into placement groups
    B. Elastic High Performance Compute Services (EHPCS).
    C. Leverage Redshift to perform business intelligence analysis on your dataset.
    D. CPU optimized EC2 instances deployed across multiple availability zones for redundancy.
Answer: A
002 Question: You work for a automotive company which is migrating their production environment in to AWS. The company has 4 separate segments, Dev, Test, UAT & Production. They require each segment to be logically isolated from each other. What VPC configuration should you recommend?
    A. A separate subnet for each segment. Then create DENY routes to stop each subnet from being able to communicate to each other.
    B. A separate VPC for each segment. Then create VPN tunnels from your HQ to each VPC so the appropriate teams can each speak to their dedicated VPC. 
    C. Deploy the EC2 instances for each segment in to separate security groups inside the same subnet.
    D. Use 1 VPC and 2 subnets. Separate each segment using a combination of security groups and ACLs.
Answer: B    
003 Question: By default how many VPCs can you have per region in your AWS account?
    A. 1
    B. 2
    C. 5
    D. 10
Answer: C    
004 Question: Which of the following is not associated with Identity Access Management Service
    A. Users    
    B. Roles
    C. Groups
    D. Workspaces
Answer: D
005 Question: You are designing a new application for a financial company that will utilize spot EC2 instances as and when they meet a certain price point. These EC2 instances will analyse data and the output their analysis to the root volume. You need to store this data in a persistent form of storage so that if the spot instances are terminated by Amazon, you will not lose your data. You need to choose the lowest cost service. Where should you store your data?
    A. S3
    B. DynamoDB
    C. Oracle RDS with multiAZ
    D. Elasticache
Answer: A
006 Question: Which of the following is not a responsibility of Amazon’s under the shared responsibility model?
    A. Data center security
    B. Hypervisor patching
    C. OS level patching for RDS
    D. OS level patching for EC2
Answer: D
007 Question: In regards to EC2 which of the following is not a customers responsibility under the shared responsibility model?
    A. Antivirus
    B. Decommissioning and destruction of storage media
    C. OS level patches
    D. Applicaiton level patches
Answer: B
008 Question: Which of the following is true when writing to S3?
    A. All regions provide read-after-write consistency for PUTS of new objects in your Amazon S3 bucket and eventual consistency for overwrite PUTS and DELETES.
    B. All regions provide write-after-read consistency for PUTS of new objects in your Amazon S3 bucket and eventual consistency for overwrite PUTS and DELETES.
    C. All regions provide write-after-read consistency for PUTS of new objects in your Amazon S3 bucket and immediate consistency for overwrite PUTS and DELETES.
    D. All regions provide read-after-write consistency for PUTS of new objects in your Amazon S3 bucket and immediate consistency for overwrite PUTS and DELETES.
Answer: A    
009 Question: You are solutions architect working for a busy ecommerce store. Due to your organisations unique security requirements, you decide to utilize EC2 running a MySQL database, rather than using RDS. You need to architect this EC2 instance to maximise your disk IO. Which of the following would give you the best disk performance?
    A. Install your MySQL instance on your root device volume on your EC2 instance.
    B. Add 2 x additional General Purpose SSD volumes to your EC2 instance, create a RAID 1 and then install MySQL to the newly created RAID 1 partition.
    C. Add 3 x additional PIOPS SSD volumes and create a RAID 5. Install MySQL to this RAID 5 partition.
    D. Add 2 x additional PIOPS SSD volumes and create a RAID 0. Install MySQL to this RAID 0 partition.
Answer: D
010 Question: Which of the following services do you get OS level access to?
    A. RDS & EC2
    B. DynamoDB & RDS
    C. EC2 & Elastic Map Reduce
    D. EC2 & Redshift
Answer: C
011 Question: You are designing an AWS solution for a new customer and they want to use their active directory credentials in order to sign in to the AWS management console. What kind of authentication response is required in order for users to authenticate with the AWS security token service (STS).
    A. Security Assertion Markup Language 2.0 (SAML 2.0)
    B. OAuth
    C. HTTPS
    D. DB2
Answer: A
012 Question: You are designing a new VPC for a customer and you need to deploy your EC2 instances in to multiple availability zones. What is the minimum number of subnets that you require to achieve this objective?
    A. 1 Subnet stretched across 2 AZ’s
    B. 2 Subnets with each subnet in an independent AZ.
    C. 2 Subnets stretched across 3 AZ’s
    D. 3 subnets with each subnet in and independent AZ.
Answer: B
013 Question: You are creating a new VPC with 3 subnets in 3 separate availability zones. You require instances in each subnet to be able to communicate to each other by default. What additional steps should you take in order to achieve this objective.
    A. Create a route between each subnets in a new route table and then associate this with each subnet.
    B. You do not need to do anything, by default all subnets can communicate with each other using the main route table
    C. Create a route between each subnet in the main route table and then associate this main route table with each subnet.
    D. ensure that each subnet is associated with a security group that will contain your EC2 instances.
Answer: B
014 Question: You have an EC2 instance which needs to find out both its private IP address and its public IP address using a script. Which of the below should you include in the script to discover this information.
    A. Run IPCONFIG (Windows) or IFCONFIG (Linux)
    B. Retrieve the instance Metadata from http://169.254.169.254/latest/meta-data/
    C. Retrieve the instance Userdata from http://169.254.169.254/latest/user-data/
    D. Use the following command; AWS EC2 displayIP
Answer: B
015 Question: You are an AWS architect and you require encryption at rest for additional volumes attached to your EC2 instance. What is the quickest and most efficient way to achieve this?
    A. Configure encryption when creating the EBS volume
    B. Configure encryption using the appropriate Operating Systems file system
    C. Configure encryption using X.509 certificates
    D. Mount the EBS volume in to S3 and then encrypt the bucket using a bucket policy.
Answer: A
016 Question: You are designing a web application for a new social media start up and have recommended using DynamoDB for the database due to its superior performance. You need to ensure that your database has redundancy. What additional steps should you do?
    A. Nothing, DynamoDB all data is automatically replicated across multiple availability zones.
    B. Enable Multi-AZ when creating your Dynamodb instance
    C. Enable Read Replicas when creating your DynamoDB instance
    D. Enable snapshotting of DynamoDB and save these snapshots to S3
Answer: A
017 Question: What blocksize does Redshift use when storing it’s data in columnar storage?
    A. 2KB
    B. 4KB
    C. 32KB
    D. 1024KB
Answer: D
018 Question: You are designing an application for a furniture retailer. A component of the application takes pictures of the furniture for sale and generates thumb nail images which then need to be stored persistently. The business can tolerate it if some images are lost as they can be regenerated. The thumbnails will need to be retrieved immediately when the application requests them. What is the cheapest option to do this?
    A. Using S3
    B. Using S3 RRS
    C. Using RDS
    D. Using Glacierr
Answer: B
019 Question: You run a website which hosts videos and you have two types of members, premium fee paying members and free members. All videos uploaded by both your premium members and free members are processed by a fleet of EC2 instances which will poll SQS as videos are uploaded. However you need to ensure that your premium fee paying members videos have a higher priority than your free members. How should you design your application.
    A. SQS allows you to set priorities on individual items within the queue, so simply set the fee paying members at a higher priority than your free members.
    B. Create two SQS queues, one for premium members and one for free members. Program your EC2 fleet to poll the premium queue first and if empty, to then poll your free members SQS queue.
    C. SQS would not be suitable for this scenario. It would be much better to use SNS to encode the videos.
    D. SQS operates on a First In, First Out process. Design your application so that premium members are sent to the SQS queue first.
Answer: B
020 Question: You are designing an image sharing website that will distribute images across the world. You need maximise performance so that your end users can download frequently accessed images as fast as possible. What AWS technology should you implement?
    A. Glacierr
    B. Global Load Balancing (GLB)
    C. CloudFront
    D. Autoscaling
Answer: C
021 Question: You are putting together a wordpress site for a local charity and you are using a combination of Route53, Elastic Load Balancers, EC2 & RDS. You launch your EC2 instance, download wordpress and setup the configuration files connection string so that it can communicate to RDS. When you browse to your URL however, nothing happens. Which of the following could NOT be the cause of this.
    A. You have forgotten to open port 80/443 on your security group in which the EC2 instance is placed
    B. Your elastic load balancer has a health check which is checking a webpage that does not exist, therefore your EC2 instance is not in service.
    C. You have not configured an ALIAS for your A record to point to your elastic load balancer
    D. You have locked port 22 down to your specific IP address therefore users cannot access your site using HTTP/HTTPS.
Answer: D
022 Question: You have uploaded a file to S3, what HTTP code would indicate that the upload was successful?
    A. HTTP 404
    B. HTTP 500
    C. HTTP 200
    D. HTTP 301
Answer: C
023 Question: You have created a custom VPC with 3 subnets, 2 private, 1 public. You deploy 3 EC2 instances in to your public subnet and attach Elastic IP addresses to these instances. You then deploy an EC2 instance in to your private subnet and then attempt to apply security patches to this instance, however it has no internet connectivity. What can you do to give this instance internet access?
    A. Deploy a NAT to the public subnet and then update the main route table to send traffic via the NAT to the private subnet.
    B. Deploy your instance to a public subnet instead
    C. Attach a public IP address to your EC2 instance in the private subnet.
    D. Attach an additional internet gateway to your EC2 instance in the private subnet.
Answer: A
024 Question: Amazon SWF is designed to help users to do which of the following?
    A. Manage user identification and authorisation
    B. Coordinate synchronous and asynchronous tasks
    C. Store files securely in the cloud
    D. Replicate an organizations email from one region to another
Answer: B
025 Question: What service can you use to audit user access & API calls across your AWS environment?
    A. CloudWatch
    B. CloudTrail
    C. CloudAudit
    D. CloudPolice
Answer: B
026 Question: Under the shared responsibility model for S3 which of the following is NOT a responsibility of Amazons.
    A. Maintaining video surveillance of the data halls
    B. Destruction of end of life magnatic disks
    C. Restricting access to the data center
    D. Configuration of individual bucket policies
Answer: D
027 Question: Under the shared responsibility model for DynamoDB which of the following is NOT a responsibility of Amazons.
    A. Patching the Xen Hypervisor.
    B. Destruction of magnetic storage media on decommissioning of disks. 
    C. Patching the underlying DynamoDB operating system.
    D. Restricting access of DynamoDB so that only the customers web application in EC2 can write data to it.
Answer: D
028 Question: You are a Solutions Architect working for a major European oil company. You are designing a new web application which will need to access data stored in DynamoDB. You need to do this as securely as possible, without storing any credentials on a long term basis. How would you achieve this?
    A. Store the Access Key ID & Secret Access Key on an encrypted S3 bucket.
    B. Create a new group in AWS Identity and Access Management and assign the EC2 instance to the group.
    C. Use AWS Identity and Access Management roles for the EC2 Instances that need to make the API calls.
    D. Store the Access Key Id & Secret Access Key in a PHP file in the application.
Answer: C
029 Question: You are a solutions architect working for a large cell phone company in the US. Your CSO has engaged a third party security company to conduct a security audit of your company to make sure it is not liable to hacking. The third party security company would like to conduct a penetration test on your AWS estate. Would this be allowed by AWS?
    A. Yes. They can do this straight away with no prior permission necessary.
    B. Only in the default VPC. 
    C. Not under any circumstances.
    D. Yes, however you need to get permission from Amazon first by raising a ticket.
Answer: D
030 Question: AWS help provide protection against some forms of traditional network attacks. Which of the following is not protected against by AWS?
    A. Social Engineering
    B. Port scanning
    C. IP spoofing
    D. Man in the Middle Attact
Answer: A
031 Question: Placement Groups can be created across 2 or more Availability Zones.
    A. True
    B. False
Answer: B
032 Question: You have three AWS accounts (A, B & C) which share data.  In an attempt to maximize performance between the accounts, you deploy the instances owned by these three accounts in "eu-west-1b".  During testing, you find inconsistent results in transfer latency between the instances. Transfer between accounts A and B is excellent, but transfers between accounts B and C, and C and A, are slower.  What could be the problem?
    A. The names of the AZs are randomly applied, so 'eu-west-1b' is not necessarily the same physical location for all three accounts
    B. You have incorrectly configured the cross-account authentication policies in Account C, adding latency to those instances.
    C. Account C has been allocated to an older section of the Data Hall with slower networking.
    D. The instances for Account C are on an overloaded Host.  Stop all the Account C instances  and then start them together so that they run an a new host.
    E. You have accidentally set up Account C in "us-west-1b".
Answer: A
033 Question: Your company has hired a young and enthusiastic accountant. After reviewing the AWS documentation and usage graphs, he announces that you are wasting vast amounts of money running servers for a full hour instead of spinning them up only when they are needed and down again as soon as they are idle for 1 minute. He cites the AWS claim that you only pay for what you use, and that as a senior engineer, you should be more conscious of wasting company money.  How do you respond ?
    A. You leap across the meeting table and slap him for insulting you in front of your peers.
    B. Acknowledge the problem and propose that you could downsize the instances so that the workload over the hour consumes the full instance capacity for the full hour. You might also propose closer monitoring and automation to allow you to up-size and down-size the instance each hour over the day to match the instance performance to the anticipated workload. 
    C. You thank him for his concern, and advise him that he has misinterpreted the pricing document: Instances are billed by the full hour, and partial hours are billed as such.  Additionally, storage charges are incurred even if the Db instance sits idle. Taking into account productivity losses, stopping and restarting Db instances may actually result in additional costs. As such, your solution is fine as it now stands.
    D. You grudgingly acknowledge his point and change your scheduling and tuning settings.
Answer: C
034 Question: Your company is moving their 10TB data warehouse to the cloud. Taking into account your company's 100Mbps connection, which service would most quickly get your data into AWS?
    A. Amazon Import/Export Disk
    B. Amazon S3 multi-part upload
    C. Amazon Redshift Import
    D. Amazon snowball
Answer: D
035 Question: You have been monitoring a sensitive autoscaling group, and you expect it to scale-in as you enter a period of holiday downtime. The auto scaling group is distributed over three AZs ( AZ - A & -B have two instances each, and AZ -C has three instances). All instances have different CPU and Memory utilization, and all instances have been running for a different number of days. All instances come from different versions of a root AMI, and all instances have different numbers of sessions connected. Which instance will be the 1st to shut down?
    A. The Instance with the fewest current sessions will terminate first.
    B. The instance that has been running longest will terminate first.
    C. The instance in AZ -C that has the oldest launch configuration will terminate first.
    D. The instance in AZ -C that has been running the longest will terminate first.
Answer: C
036 Question: Auto Scaling is a tool used to create fault-tolerant and cost-effective architectures.
    A. True
    B. False
Answer: A
037 Question: What is the maximum VisibilityTimeout of an SQS message in a FIFO queue?
    A. 14 days
    B. 1 day
    C. 1 hour
    D. 12 hours
Answer: D
038 Question: A client who is using EC2 believes that someone other than approved administrators is trying to gain access to her Linux web app instances, and she asks what sort of network access logging can be added to the system. Which of the following might you recommend?
    A. Set up a traffic logging rule on the network firewall and direct the log to CloudWatch or S3.
    B. Set up a Flow Log for the group of instances and forward them to CloudWatch.
    C. Make use of an OS level logging tools such as iptables and log events to CloudWatch or S3.
    D. Use Event Log filters to trigger alerts that are forwarded to CloudWatch.
    E. Set up a Flow Log for the group of instances and forward them to S3.
Answer: C
039 Question: Your company likes the idea of storing files on AWS. However, low-latency service of the last few days of files is important to customer service. Which Storage Gateway configuration would you use to achieve both of these ends?
    A. Gateway-VTL
    B. Gateway-Snapshot
    C. Gateway-Cached
    D. Gateway-Stored
Answer: C
040 Question: You have a MySQl database running on an EC2 instance in a private subnet. You can connect via SSH, but you are unable to apply updates to the database server via the NAT instance. What might you do to remedy this problem?
    A. Ensure that "Source/Destination Checks" is disabled on the NAT instance.
    B. Ensure that the Security Group allows HTTP traffic. 
    C. Replace the NAT instance.
    D. Modify the Security Group to allow SSH traffic from anywhere.
Answer: A
041 Question: Amazon SQS keeps track of all tasks and events in an application.
    A. True
    B. False
Answer: B
042 Question: When editing permissions (policies and ACLs), to whom does the concept of the "Owner" refer?
    A. The Owner is the IAM user who created the object via the GUI, CLI, or API.
    B. The Owner is IAM Role used to create the object via the GUI, CLI, or API.
    C. The "Owner" refers to the identity and email address used to create the account AWS account.
    D. There is no special concept of \"Owner\" in AWS.
Answer: C
043 Question: Your company provides an online image recognition service and uses SQS to decouple system components. Your EC2 instances poll the image queue as often as possible to keep end-to-end throughput as high as possible, but you realize that all this polling is resulting in both a large number of CPU cycles and skyrocketing costs. How can you reduce cost without compromising service?
    A. Enable long polling by setting the ReceiveMessageWaitTimeSeconds to a number > 0.
    B. Enable short polling by setting the ReceiveMessageWaitTimeMinutes to a number > 0.
    C. Enable short polling by setting the ReceiveMessageWaitTimeSeconds to a number > 0.
    D. Enable long polling by setting the ReceiveMessageWaitTimeMinutes to a number > 0.
Answer: A
044 Question: You need to store some easily-replaceable objects on S3. With quick retrieval times and and cost effectiveness in mind, which S3 storage class should you consider.
    A. S3
    B. S3-RRS
    C. Glacier
    D. Snowball
    E. S3-Provisioned IOPS
Answer: B
045 Question: You are a solutions architect working for a busy media company with offices in Japan and the United States. Your production environment is hosted both in US-EAST-1 and AP-NORTHEAST-1. Your European users have been connecting to the production environment in Japan, and are seeing the site in Japanese rather than in English. You need to ensure that they view the English language version. Which of the routing policies below could help you achieve this?
    A. Weighted Routing
    B. Simple Routing
    C. Geolocation
    D. Failover Routing
Answer: C
046 Question: Although your application customarily runs at 30% usage, you have identified a recurring usage spike (>90%) between 8pm and midnight daily. What is the most cost effective way to scale your application to meet this increased need?
    A. Manually deploy Reactive Event-based Scaling each night at 7:45.
    B. Use Proactive Cyclic Scaling to boost your capacity at a fixed interval.
    C. Deploy additional EC2 instances to meet the demand. 
    D. Increase the size of the Resource Group to meet demand. 
Answer: B
047 Question: You work for a popular media outlet about to release a story that is expected to go viral. During load testing on the website, you discover that there is read contention on the database tier of your application. Your RDS instance consists of a MySQL database on an extra large instance. Which two of the following approaches would be best to further scale this instance to meet the anticipated increase in traffic your viral story will generate?
    A. Use Elasticache to cache the frequently read, static data. 
    B. Shard the MySQL database into multiple copies.
    C. Provision a larger instance size with provisioned IOPS.
    D. Add an RDS Multi-AZ for increased read performance.
Answer: A
048 Question: Following advice from your consultant, you have configured your VPC to use Dedicated hosting tenancy. A subsequent change to your application has rendered the performance gains from dedicated tenancy superfluous, and you would now like to recoup some of these greater costs. How do you revert to Default hosting tenancy?
    A. Create AMIs of all your instances and use them to create new instances using Default hosting.
    B. Stop each instance and change the hosting attribute and restart.
    C. Create AMIs of all your instances. Create a new VPC with Default as the hosting tenancy attribute, and use them to create new instances using Default tenancy.
    D. Change the hosting attribute and then restart the instance.
Answer: C
049 Question: Which URL format does S3 support in pointing to bucket "mynewbucket"?
    A. http://mynewbucket.s3-aws-region.amazonaws.com
    B. http://mynewbucket.s3-aws-region.amazon.com
    C. http://mynewbucket.s3-aws-region.aws.com
    D. http://mynewbucket.s3.aws-region.amazonaws.com
Answer: A
050 Question: You are developing a web application, and you are maintaining separate sets of resources for your alpha, beta, and release environments. Each version runs on Amazon EC2 with an EBS volume. You use Elastic Load Balancing to manage traffic and Amazon Route 53 to manage your domain. What's the best way to check the health and status of all three groups of services simultaneously?
    A. Access CloudTrail audits for each set or resources.
    B. Maintain an open console for each set of resources.
    C. Create a resource group containing each set of resources and view all three environments from a single, group dashboard. 
    D. Use CLoudWatch to proactively monitor each environment.
Answer: C
051 Question: Your company has just purchased another company. As part of the merger, your team has been instructed to cross connect the corporate networks. You run all your confidential corporate services and Internal DNS in a VPC. The merged company has all their confidential corporate services and Internal DNS on-premises. After establishing a Direct-Connect service between your VPC and their on-premise network, and confirming all the routing, firewalls, and authentication, you find that while you can resolve names against their DNS, the other company services is unable to resolve names against your DNS servers. Why might this be?
    A. AWS Route53 is an Internet service, and the other company needs to do lookups and zone transfers via the Internet, not the Direct-Connect link.
    B. You cannot use DNS in this way. You need to merge the zones under a parent zone registered with ICANN.
    C. By design, AWS DNS does not respond to requests originating from outside the VPC. 
    D. Route53 is not an industry standard DNS service, and zone transfers and name resolution must be done via a proprietary API.
Answer: C
052 Question: How is the Public IP address managed in an instance session via the instance GUI/RDP or Terminal/SSH session?
    A. The Public IP address can be managed via the instance MetaData at http://169.254.169.254/latest/meta-data/local-ipv4.
    B. The Public IP address can be managed via the instance MetaData at http://169.254.169.254/latest/meta-data/public-ipv4.
    C. The Public IP address is not managed on the instance: It is, instead, an alias applied as a network address translation of the Private IP address.
    D. For security reasons, the Public IP address is a hidden value.
Answer: C
053 Question: You have been engaged by a company to design and lead a migration to an AWS environment. The team is concerned about the capabilities of the new environment, especially when it comes to avoiding bottlenecks. The design calls for about 20 instances (C3.2xLarge) pulling jobs/messages from SQS. Network traffic per instance is estimated to be around 500 Mbps at the beginning and end of each job. Which network configuration should you plan on deploying?
    A. Deploy as a Placement Group as the aggregated burst traffic could be around 10 Gbps.
    B. Activate EBS-Optimization on the instance to maximize network throughput.
    C. Spread the Instances over multiple AZs to minimize the traffic concentration and maximise the fault tolerance.
    D. Choose a different instance type that better matched the traffic demand. 
Answer: C
054 Question: You are a consultant planning to deploy DynamoDB across three AZs. Your lead DBA is concerned about data consistency. Which of the following do you advise the lead DBA to do?
    A. To ask the development team to implement a checksum algorithm to confirm that the data is consistent across all the AZs.
    B. To ask the development team to code for strongly consistent reads. As the consultant, you will advise the CTO of the increased cost.
    C. To ask the development team to code a Lambda function to check data consistency after each write.
    D. To ask the development team to code to check for a successful completion code (200) at the completion of every write.
    E. To ask the development team to code an maintenance task to run on a schedule to check consistency.
Answer: B
055 Question: You successfully configure VPC Peering between VPC-A  and VPC-B. You then establish an IGW and a Direct-Connect connection in VPC-B. Can instances in VPC-A connect to your corporate office via the Direct-Connect service, and connect to the Internet via the IGW?
    A. You successfully configure VPC Peering between VPC-A  and VPC-B. You then establish an IGW and a Direct-Connect connection in VPC-B. Can instances in VPC-A connect to your corporate office via the Direct-Connect service, and connect to the Internet via the IGW?
    B. Instances in VPC-A will be able to access the Internet, but not the corporate office.
    C. VPC peering does not support edge to edge routing.
    D. Instances in VPC-A will be able to access the corporate office, but not the Internet.
Answer: C
056 Question: You are reviewing Change Control requests, and you note that there is a change designed to reduce wasted CPU cycles by increasing the value of VisibilityTimeout attribute. What does this mean?
    A. When the consumer instance polls for new work the SQS service will allow it to wait a certain time for a message to be available before closing the connection.
    B. When a new message is added to the SQS queue, it will be hidden from consumer instances for a fixed period. 
    C. When the consumer instance polls for new work, the consumer instance will wait a certain time until it has a full workload before closing the connection.
    D. While processing a message, a consumer instance can reset the message visibility by restarting the preset timeout counter.
    E. When a consumer instance retrieves a message, that message will be hidden from other consumer instances for a fixed period. 
Answer: E
057 Question: You manage a Ruby on Rails application that lives on a cluster of EC2 instances. Your website occasionally experiences brief, strong, and entirely unpredictable spikes in traffic that overwhelm your EC2 instances’ resources and freeze the application. As a result, you're losing recently submitted requests from end users. You use Auto Scaling to deploy additional resources to handle the load during spikes, but the new instances don't spin-up fast enough to prevent the existing application servers from freezing. Which of the following will provide the most cost-effective solution in preventing the loss of recently submitted requests?
    A. Ask AWS support to pre-warm the Elastic Load Balancer.
    B. Use Amazon SQS to decouple the application components and keep the requests in queue until the extra Auto-Scaling instances are available.
    C. Increase the size of your existing EC2 instances.
    D. Keep a large EC2 instance on standby.
Answer: B
058 Question: You're building out a single-region application in us-west-2. However, disaster recovery is a strong consideration, and you need to build the application so that if us-west-2 becomes unavailable, you can fail-over to us-west-1. Your application relies exclusively on pre-built AMI's. In order to share those AMI's with the region you're using as a backup, which process would you follow?
    A. Create a new instance in us-west-1, making certain the instance in the failover region shares a security group with the instance in the default region.
    B. Copy the AMI from us-west-2, manually apply launch permissions, user-defined tags, and Amazon S3 bucket permissions of the default AMI to the new instance, and launch the instance.
    C. Copy the AMI from us-west-2 to us-west-1 and launch as-is.
    D. Nothing: AMIs are specific to an account, and they can be used anywhere.
Answer: B
059 Question: At the monthly product meeting, one of the Product Owners proposes an idea to address an immediate shortcoming of the product system: storing a copy of the customer price schedule in the customer record in the database. You know that you can store large text or binary objects in DynamoDB. You give a tentative OK to do a Minimal Viable Product test, but stipulate that it must comply with the size limitation on the Attribute Name & Value. Which is the correct limitation?
    A. The Name must not exceed 64 KB and the Value must not exceed 500 KB. 
    B. The Name must not exceed 64 KB and the Value must not exceed 400 KB. 
    C. The combined Value and Name combined must not exceed 400 KB. 
    D. The Name must not exceed 64 KB and the Value must not exceed 255 KB. 
    E. The combined Value and Name combined must not exceed 255 KB. 
Answer: C
060 Question: To save money, you quickly stored some data on the root volume of an EC2 instance and shut it down for the weekend. When you returned on Monday and restarted your instance, you discovered that your data was gone. Why might that be?
    A. The root volume was ephemeral, block-level storage. Data on an instance store volume is lost if an instance terminates.
    B. The elastic block-level storage service failed over the weekend. 
    C. The instance failed to connect to the root volume on Monday.
    D. The EBS volume was not large enough to store your data. 
Answer: A
061 Question: In S3, what does RRS stand for?
  a. Relational Reduced Storage
  b. Reactive Replicating Storage
  c. Reduced Replication Storage
  d. Reduced Redundancy Storage
Answer: d
062 Question: An application requires OS privileges on a database host. Which one is best choice of High Available DB?
  a. Amazon EC2 instances in a replication configuration utilizing a single AZ
  b. A standalone Amazon EC2 instance
  c. Amazon EC2 instances in a replication configuration utilizing two different AZ
  d. Amazon RDS in a Multi-AZ configuration
Answer: c
063 Question: Amazon's EBS volumes are
  a. Object based storage
  b. Block based storage
  c. Encrypted by default
  d. Not suitable for databases
Answer: b
064 Question: A _____ is a document that provides a formal statement of one or more permissions.
  a. Policy
  b. User
  c. Group
  d. Role
Answer: a
065 Question: An auto-scaling group spans 3 AZs and has 4 running EC2 instances. When auto-scaling needs to terminate an instance by default, autoscaling will (select 2):
  a. Allow >= 5mins for Windows/Linux shutdown scripts to complete before terminating
  b. Terminate the instance with the least active network connections
  c. Send an SNS notification if configured to do so
  d. Terminate an instance in the AZ which currently has 2 running instances
  e. Randomly select one of the 3 AZs and terminate an instance
Answer: c, d
066 Question: Amazon's Glacier service is a Content Distribution Network which integrates with S3.
  a. true
  b. false
Answer: b
067 Question: How many copies of my data does RDS - Aurora store by default?
  a. 3
  b. 6
  c. 2
  d. 1
Answer: b
068 Question: In S3 RRS, the durability of my files is 
  a. 99.99%
  b. 99.99999999%
  c. 99%
  d. 100%
Answer: a
069 Question: A company is deploying a new two-tier web application in AWS. The company has limited staff and requires high availability, and the application requires complex queries and table joins. Which configuration provides the solution for the company's requirements?
  a. MySQL Installed on two Amazon EC2 Instances in a single Availability Zone
  b. Amazon RDS for MySQL with Multi-AZ
  c. Amazon ElastiCache
  d. Amazon DynamoDB
Answer: b
070 Question: When deploying databases on your own EC2 instances, it is recommended that you deploy these on magnetic storage rather than SSD as you get better performance.
  a. true
  b. false
Answer: b
071 Question: In RDS, you are responsible for maintaining OS & application security patching, antivirus, etc. 
  a. true
  b. false
  Answer: b
072 Question: If an Amazon EBS volume is an additional partition (ie. not the root volume), can I detach it without stopping the instance?
  a. Yes, but it may take some time
  b. No, you still need to stop the instance
Answer: a
073 Question: EC2 instances are launched from Amazon Machine Images (AMI). An AMI can
  a. Be used to launch EC2 instances in any AWS region
  b. Only launch EC2 instances in the same Country as the AMI is stored
  c. Only launch EC2 instances in the same AWS region as the AMI is stored
  d. Only launch EC2 instances in the same AWS AZ as the AMI is stored
Answer: c
074 Question: You have a VPC with 1 private subnet and 1 public subnet with a NAT server. You are creating a group of EC2 instances that configure themselves at startup via downloading a bootstrapping script from S3 that deploys an application via GIT. Which setup provides the highest level of security?
  a. EC2 instances in private subnet, no EIPs, route outgoing traffic via the NAT
  b. EC2 instances in public subnet, no EIPs, route outgoing traffic via the Internet Gateway (IGW)
  c. EC2 instances in private subnet, assign EIPs, route outgoing traffic via the Internet Gateway (IGW)
  d. EC2 instances in public subnet, assign EIPs, route outgoing traffic via the NAT
Answer: a
075 Question: The AWS platform is certified PCI DSS 1.0 compliant.
  a. true
  b. false
Answer: a
076 Question: Can I "force" a failover for any RDS instance that has Multi-AZ configured?
  a. Yes
  b. No
  c. Only for Oracle RDS instances
Answer: a
077 Question: What does EBS stand for?
  a. Energetic Block Storage
  b. Elastic Based Storage
  c. Equal Block Storage
  d. Elastic Block Storage
Answer: d
078 Question: Out of the stripping options available for the EBS volumes, which one has the following disadvantage : 'Doubles the amount of I/O required from the instance to EBS compared to RAID 0, because you're mirroring all writes to a pair of volumes, limiting how much you can stripe.' ?
  a. Raid 0
  b. RAID 1+0 (RAID 10) 
  c. Raid 1
  d. Raid 2
Answer: b
079 Question: You are working with a customer who has 10 TB of archival data that they want to migrate to Glacier. The customer has a 1-Mbps connection to the internet. Which service or feature provides the fastest method of getting data into Amazon Glacier?
  a. Glacier multipart upload
  b. AWS Storage Gateway
  c. VM Import/Export
  d. AWS Import/Export
Answer: d
000 Question: I can enable multi-factor authentication by using
  a. RDS
  b. IAM
  c. DynamoDB
  d. Account Settings
Answer: b
000 Question: Which 2 services provide Native encryption?
  a. Glacier
  b. EC2
  c. IAM
  d. Storage Gateway
Answer: a, d
000 Question: If you want your application to check whether a request generated an error, then you look for an ____ node in the response from the Amazon RDS API
  a. Incorrect
  b. Error
  c. False
  d. True
Answer: b
000 Question: The AWS platform consists of how many regions currently?
  a. 5
  b. 10
  c. 11
  d. 12
Answer: c
000 Question: In what circumstances would I choose provisioned IOPS in RDS over standard storage?
  a. If you use production online transaction processing
  b. If you have workloads that are not sensitive to latency/lag
  c. If your business was trying to save money
  d. If this was a test DB
Answer: a
000 Question: From what services I can block incoming/outgoing IPs?
  a. Security Groups
  b. DNS
  c. ELB?
  d. VPC subnet?
  e. IGW?
  f. NACL
Answer: f
000 Question: you can assign you own metadata in the form of
  a. Wildcards
  b. Certificates
  c. Tags
  d. Notes
Answer: c
000 Question: Auditing user access/API calls, etc. , across the entire AWS estate can be achieved using
  a. CloudFront
  b. CloudWatch
  c. CloudFlare
  d. CloudTrail
Answer: d
000 Question: When using a custom VPC and placing an EC2 instance into a public subnet, it will automatically be internet accessible (ie. you don't need to apply an elastic IP or ELB to the instance).
  a. true
  b. false
Answer: b
000 Question: In S3 the durability of my files is
  a. 99.99%
  b. 99.999999999%
  c. 99%
  d. 100%
Answer: b
000 Question: A company has an AWS account that contains 3 VPCs (dev, tst, prd) in the same region. Test is peered to both prd and dev. All VPCs have non-overlapping CIDR blocks. The company wants to push minor releases from dev to prd to speed up time to market. Which of the following options helps accomplish this?
  a. Create a new peering connection between prd and dev along with appropriate routes
  b. Create a new entry to prd in the dev route table using the peering connection as the target
  c. Attach a second gateway to dev. Add a new entry in the prd route table identifying the gateway as the target
  d. The VPCs have non-overlapping CIDR blocks in teh same account. The route tables contain local routes for all VPCs
Answer: a
000 Question: If I want to run a database on an EC2 instance, which is the most recommended Amazon storage option?
  a. RDS
  b. S3
  c. Glacier
  d. EBS
Answer: d
000 Question: As the AWS is PCI DSS 1.00 compliant, I can immediately deploy a website to it that takes credit card details. I do not need any kind of delta accreditation from a QSA. 
  a. true
  b. false
Answer: b
000 Question: Every user you create in the IAM system starts with ____
  a. Full permissions
  b. Partial permissions
  c. No permissions
Answer: c
000 Question: You can RDP or SSH into an RDS instance to see what is going on with the operating system.
  a. true
  b. false
Answer: b
000 Question: A customer has a single 3-TB volume on-premises that is used to hold a large repository of images and print layout files. This repository is growing at 500 GB a year and must be presented as a single logical volume. The customer is becoming increasingly constrained with their local storage capacity and wants an off-site backup of this data, while maintaining low-latency access to their frequently accessed data. Which AWS Storage Gateway configuration meets the customer requirements?
  a. Gateway-Cached volumes with snapshots scheduled to Amazon S3
  b. Gateway-Stored volumes with snapshots scheduled to Amazon S3
  c. Gateway-Virtual Tape Library with snapshots to Amazon S3
  d. Gateway-Virtual Tape Library with snapshots to Amazon Glacier
Answer: a
000 Question: MySQL installations default to port number
  a. 1433
  b. 3306
  c. 3389
  d. 80
Answer: b
000 Question: Amazon SWF is designed to help users:
  a. Manage user identification and authorization
  b. Coordinate synchronous and asynchronous tasks
  c. Secure their VPCs
  d. Help users store file based objects
Answer: b
000 Question: EC2 EBS-backed (EBS root) instance is stopped, what happens to the data on any ephemeral store volumes?
  a. Data is automatically saved in an EBS volume.
  b. Data is unavailable until the instance is restarted. 
  c. Data will be deleted and will no longer be accessible.
  e. Data is automatically saved as an EBS snapshot.
Answer: c
000 Question: Your customer is willing to consolidate their log streams (access logs application logs security logs etc. ) in one single system. Once consolidated, the customer wants to analyze these logs in real time based on heuristics. From time to time, the customer needs to validate heuristics, which requires going back to data samples extracted from the last 12 hours? What is the best approach to meet your customer's requirements?
  a. Send all the log events to Amazon SQS. Setup an Auto Scaling group of EC2 servers to consume the logs and apply the heuristics.
  b. Send all the log events to Amazon Kinesis develop a client process to apply heuristics on the logs
  c. Configure Amazon Cloud Trail to receive custom logs, use EMR to apply heuristics the logs
  d. Setup an Auto Scaling group of EC2 syslogd servers, store the logs on S3 use EMR to apply heuristics on the logs
Answer: b
000 Question: What is the underlying Hypervisor for EC2?
  a. Hyper-V
  b. ESX
  c. Xen
  d. OVM
Answer: a
000 Question: Instance 1 and 2 are running in two different subnets (A and B) of a VPC. Instance 1 is not able to ping instance 2. What are 2 possible reasons?
  a. The routing table of subnet A has no target route to subnet B
  b. The security group attached to instance 2 does not allow inbound ICMP traffic
  c. The policy linked to the IAM role on instance 1 is not configured correctly
  d. The NACL on subnet B doesn't allow outbound ICMP traffic
Answer: b, d
000 Question: AWS recommends providing EC2 instances with credentials so they can access other resources (such as S3 buckets) instead of assigning roles.
  a. true
  b. false
Answer: b
000 Question: Which of the following approaches provides the lowest cost for Amazon Elastic Block Store snapshots while giving you the ability to fully restore data?
  a. Maintain two snapshots: the original snapshot and the latest incremental snapshot.
  b. Maintain a volume snapshot; subsequent snapshots will overwrite one another
  c. Maintain a single snapshot the latest snapshot is both Incremental and complete.
  d. Maintain the most current snapshot, archive the original and incremental to Amazon Glacier.
000 Question: Answer: c
A company is building software on AWS that requires access to various AWS services. Which configuration should be used to ensure that AWS credentials (i.e.,Access Key ID/Secret Access Key combination) are not compromised?
  a. Enable Multi-Factor Authentication for your AWS root account.
  b. Assign an IAM role to the Amazon EC2 instance.
  c. Store the AWS Access Key ID/Secret Access Key combination in software comments.
  d. Assign an IAM user to the Amazon EC2 Instance.
Answer: b
000 Question: Can I move a reserved instance from one region to another?
  a. Yes
  b. Only in the US
  c. No
  d. Depends on the region
Answer: c
000 Question: What types of RDS databases are currently available
  a. Aurora, MySQL, MSSQL, Cassandra
  b. PostGres, Cassandra, MongoDB, Aurora
  c. Oracle, MSSQL, MySQL, Cassandra
  d. Oracle, MSSQL, MySQL, Postgres
Answer: d
000 Question: Which statement best describes Availability Zones
  a. Content distribution network which is used to distribute content to users
  b. A restricted area designed specifically for creating VPCs
  c. Two zones containing compute resources that are designed to maintain synchronized copies of data within each other
  d. Distinct locations from within an AWS region that are engineered to be isolated from failures
Answer: d
000 Question: What is the maximum response time for a Business Level Premium support case?
  a. 1 day
  b. 12 hrs
  c. 15 mins
  d. 1 hr
Answer : d
000 Question: You have a load balancer configured for VPC, and all back-end EC2 instances are in service. Your web browser is timing out when connecting to the load balancers' DNS name. Which options are probable causes of this behavior? Choose 2
  a. Load balancer was not configured to use a public subnet with an internet gateway configured
  b. EC2 instances do not have a dynamically allocated private IP address
  c. Security groups or network ACLs are not properly configured for web traffic
  d. Load balancer is not configured in a private subnet with a NAT instance
  e. VPC does not have a VGW configured
Answer: a, c
000 Question: Reserved instances are available for multi-AZ deployments.
  a. true
  b. false
Answer: a
000 Question: Automated backups are enabled by default for new DB Instance?
  a. true
  b. false
Answer: a
000 Question: AWS DNS service is known as
  a. CloudDNS
  b. CloudFront
  c. CloudTrail
  d. Route53
Answer: d
000 Question: Which DNS name can only be resolved within amazon EC2?
  a. Internal DNS Name
  b. External DNS Name
  c. Global DNS Name
  d. Private DNS Name
Answer: a
000 Question: Which feature support optimize performance for a compute cluster that requires low inter-node latency?
  a. Multiple Availability Zones
  b. AWS Direct Connect
  c. EC2 Dedicated Instances
  d. Placement Groups
  e. VPC private subnets
Answer: d
000 Question: How can the domain's zone apex, for example, "myzoneapexdomain.com", be pointed towards an Elastic Load Balancer?
  a. By using an Amazon Route 53 Alias record
  b. By using an AAAA record
  c. By using an Amazon Route 53 CNAME record
  d. By using an A record
Answer: a
000 Question: For the EBS volumes, which has the following disadvantage : 'Doubles the amount of I/O required from the instance to EBS compared to RAID 0, because you're mirroring all writes to a pair of volumes, limiting how much you can stripe.
  a. Raid 0
  b. Raid 1+0 [Raid 10]
  c. Raid 1
  d. Raid 5
Answer: d
000 Question: What are the 4 level of AWS premium support?
  a. It's an IAAS platform, there sis no support
  b. Free, Bronze, Silver, Gold
  c. Basic, Startup, Business, Enterprise
  d. Basic, Developer, Business, Enterprise
Answer: d
000 Question: Amazon RDS does not currently support increasing storage on a ___ DB instance.
  a. MySQL
  b. Aurora
  c. Oracle
  d. MSSQL
Answer: d
000 Question: You are deploying an application to collect votes for a very popular television show. Millions of users will submit votes using mobile devices. The votes must be collected into a durable, scalable, and highly available data store for real-time public tabulation. Which service should you use?
  a. Amazon DynamoDB
  b. Amazon Redshift
  c. Amazon Kinesis
  d. Amazon Simple Queue Service
Answer: a
000 Question: What is the difference between Elastic Beanstalk and CloudFormation?
  a. Elastic Beanstalk is a monitoring tool to view performance of your AWS resources. CloudFormation is an automated provisioning engine to deploy entire cloud environments via JSON.
  b. Elastic Beanstalk automatically handles the deployment, from capacity provisioning, load balancing, auto-scaling to application health monitoring based on the code you upload to it. CloudFormation is an automated provisioning engine to deploy entire cloud environments via JSON.
  c. There is no difference.
  d. Elastic Beanstalk automatically handles the deployment, from capacity provisioning, load balancing, auto-scaling to application health monitoring based on the code you upload to it. CloudFormation is a security service designed to harden your cloud against an attack, like a DDOS.
Answer: b
000 Question: To be prepared for a security assessment, an organization should implement which two configuration management practices? Choose 2 answers
  a. Determine whether remote administrative access is performed securely.
  b. Verify that all Amazon Simple Storage Service (S3) bucket policies and ACLs correctly implement your security policies.
  c. Determine whether unnecessary users and services have been identified on all Amazon-published AMIs.
  d. Verify that AWS Trusted Advisor has identified and disabled all unnecessary users and services on your Amazon Elastic Compute Cloud (EC2) instances.
Answer: c, d
000 Question: A customer has a web application that uses cookie-based sessions to track logged-in users. It is deployed on AWS using Elastic Load Balancing and Auto Scaling. When load increases, Auto Scaling launches new instances, but the load on the other instances does not decrease; this causes all existing users to have a slow experience. What could be the cause of the poor user experience?
  a. The ELB DNS record's TTL is set too high.
  b. The new instances are not being added to the ELB during the Auto Scaling cooldown period. 
  c. The website uses the dynamic content feature of Amazon CloudFront which is keeping connections alive to the ELB. 
  d. The ELB is continuing to send requests with previously established sessions to the same backend instances rather than spreading them out to the new instances.
answers: d
000 Question: When creating a new security group, all inbound traffic is allowed by default.
  a. true
  b. false
Answer: b
000 Question: Company "ABC" needs to deploy services to an AWS region which they have not previously used. The company currently has an AWS identity and Access Management (IAM) role for the Amazon EC2 instances, which permits the instance to have access to Amazon DynamoDB. The company wants their EC2 instances in the new region to have the same privileges. How should the company achieve this?
  a. Create a new IAM role and associated policies within the new region
  b. Assign the existing IAM role to the Amazon EC2 instances in the new region
  c. Copy the IAM role and associated policies to the new region and attach it to the instances
  d. Create an Amazon Machine Image (AMI) of the instance and copy it to the desired region using the AMI Copy feature
Answer: b
000 Question: If an Amazon EBS volume is the root device of an instance, can I detach it without stopping the instance?
  a. Yes
  b. No
Answer: b
000 Question: When an EC2 instance that is backed by an S3-based AMI is terminated, what happens to the data on the root volume?
  a. Data is automatically saved as an EBS snapshot.
  b. Data is automatically saved as an EBS volume.
  c. Data is unavailable until the instance is restarted. 
  d. Data is automatically deleted. 
Answer: d
000 Question: Which procedure for backing up a relational database on EC2 that is using a set of RAIDed EBS volumes for storage minimizes the time during which the database cannot be written to and results in a consistent backup?
  a. 1. Detach EBS volumes, 2. Start EBS snapshot of volumes, 3. Re-attach EBS volumes
  b. 1. Stop the EC2 Instance. 2. Snapshot the EBS volumes
  c. 1. Suspend disk I/O, 2. Create an image of the EC2 Instance, 3. Resume disk I/O
  d. 1. Suspend disk I/O, 2. Start EBS snapshot of volumes, 3. Resume disk I/O
  e. 1. Suspend disk I/O, 2. Start EBS snapshot of volumes, 3. Wait for snapshots to complete, 4. Resume disk I/O
Answer: d
000 Question: Which procedure for backing up a relational database on EC2 that is using a set of RAlDed EBS volumes for storage minimizes the time during which the database cannot be written to and results in a consistent backup?
  a. 1. Detach EBS volumes, 2. Start EBS snapshot of volumes, 3. Re-attach EBS volumes
  b. 1. Stop the EC2 Instance. 2. Snapshot the EBS volumes
  c. 1. Suspend disk I/O, 2. Create an image of the EC2 Instance, 3. Resume disk I/O
  d. 1. Suspend disk I/O, 2. Start EBS snapshot of volumes, 3. Resume disk I/O
  e. 1. Suspend disk I/O, 2. Start EBS snapshot of volumes, 3. Wait for snapshots to complete, 4. Resume disk I/O
Answer: d
000 Question: You have a video transcoding application running on Amazon EC2. Each instance polls a queue to find out which video should be transcoded, and then runs a transcoding process. If this process is interrupted, the video will be transcoded by another instance based on the queuing system. You have a large backlog of videos which need to be transcoded and would like to reduce this backlog by adding more instances. You will need these instances only until the backlog is reduced. Which type of Amazon EC2 instances should you use to reduce the backlog in the most cost efficient way?
  a. Reserved instances
  b. Spot instances
  c. Dedicated instances
  d. On-demand instances
Answer: b
000 Question: Which of the following is part of the failover process for a Multi-Availability Zone Amazon Relational Database Service (RDS) instance?
  a. The failed RDS DB instance reboots.
  b. The IP of the primary DB instance is switched to the standby DB instance.
  c. The DNS record for the RDS endpoint is changed from primary to standby.
  d. A new DB instance is created in the standby availability zone.
Answer: c
000 Question: An organization is planning to use AWS for their production roll out. The organization wants to implement automation for deployment such that it will automatically create a LAMP stack, download the latest PHP installable from S3 and setup the ELB. Which of the below mentioned AWS services meets the requirement for making an orderly deployment of the software?
  a. AWS Elastic Beanstalk
  b. AWS Cloudfront
  c. AWS Cloudformation
  d. AWS DevOps
Answer: a
000 Question: As an application has increased in popularity, reports of performance issues have grown. The current configuration initiates scaling actions based on Avg CPU utilization; however during reports of slowness, CloudWatch graphs have shown that Avg CPU remains steady at 40 percent. This is well below the alarm threshold of 60 percent. Your developers have discovered that, due to the unique design of the application, performance degradation occurs on an instance when it is processing more than 200 threads. What is the best way to ensure that your application scales to match demand?
  a. Launch two to six additional instances outside of the AutoScaling group to handle the additional load. 
  b. Populate a custom CloudWatch metric for concurrent sessions and initiate scaling actions based on that metric instead of on CPU use.
  c. Empirically determine the expected CPU use for 200 concurrent sessions and adjust the CloudWatch alarm threshold to be that CPU use.
  d. Add a script to each instance to detect the number of concurrent sessions. If the number of sessions remains over 200 for five minutes, have the instance increase the desired capacity of the AutoScaling group by one.
Answer: b
000 Question: As an application has increased in popularity, reports of performance issues have grown. The current configuration initiates scaling actions based on Avg CPU utilization; however during reports of slowness, CloudWatch graphs have shown that Avg CPU remains steady at 40 percent. This is well below the alarm threshold of 60 percent. Your developers have discovered that, due to the unique design of the application, performance degradation occurs on an instance when it is processing more than 200 threads. What is the best way to ensure that your application scales to match demand?
  a. Launch two to six additional instances outside of the AutoScaling group to handle the additional load. 
  b. Populate a custom CloudWatch metric for concurrent sessions and initiate scaling actions based on that metric instead of on CPU use.
  c. Empirically determine the expected CPU use for 200 concurrent sessions and adjust the CloudWatch alarm threshold to be that CPU use.
  d. Add a script to each instance to detect the number of concurrent sessions. If the number of sessions remains over 200 for five minutes, have the instance increase the desired capacity of the AutoScaling group by one.
Answer: b
000 Question: You need to design a VPC for a web-application consisting of an ELB a fleet of web application servers, and an RDS DB. The entire infrastructure must be distributed over 2 AZ. Which VPC configuration works while assuring the DB is not available from the internet?
  a. One Public Subnet for ELB one Public Subnet for the web-servers, and one private subnet for the DB
  b. One Public Subnet for ELB two Private Subnets for the web-servers, and two private subnets for the RDS
  c. Two Public Subnets for ELB two private Subnet for the web-servers, and two private subnet for the RDS
  d. Two Public Subnets for ELB two Public Subnet for the web-servers, and two public subnets for the RDS
Answer: b
000 Question: You are tasked with moving a legacy application from a virtual machine running inside your datacenter to an Amazon VPC unfortunately this app requires access to a number of on-premises services and no one who configured the app still works for your company. even worse there is no documentation for it. what will allow the application running inside the VPC to reach back and access its internal dependencies without being reconfigured? Choose 3 answers
  a. An AWS Direct connect link between the VPC and the network housing the internal services.
  b. An Internet gateway to allow a VPN Connection
  c. AN Elastic IP address on the VPC Instance
  d. AN IP Address space that does not conflict with the one on-premises
  e. Entries in Amazon Route 53 that allow the instance to resolve its dependencies IP address
  f. A VM Import of the current Virtual Machine
Answer: a, d, f
000 Question: Your company is getting ready to do a major public announcement of a social media site on AWS. The website is running on EC2 instances deployed across multiple Availability Zones with a Multi-AZ RDS MySQL Extra Large DB Instance. The site performs a high number of small reads and writes per second and relies on an eventual consistency model. After comprehensive tests you discover that there is read contention on RDS MySQL. Which are the best approaches to meet these requirements? (Choose 2 answers)
  a. Deploy ElasticCache in-memory cache running in each availability zone
  b. Implement sharding to distribute load to multiple RDS MySQL instances
  c. Increase the RDS MySQL Instance size and Implement provisioned IOPS
  d. Add an RDS MySQL read replica in each availability zone
Answer: a, d
000 Question: In RDS, what is the maximum value I can set for my backup retention period?
  a. 15 days
  b. 30 days
  c. 35 days
  d. 45 days
Answer: c
000 Question: Individual instances are provisioned in 
  a. Regions only, you cannot choose anything below this
  b. Availability Zones
  c. Global
Answer: b
000 Question: Amazon S3 is
  a. Object Based Storage
  b. Block Based Storage
  c. A Data Warehouse Solution
  d. Suitable for data archival, not frequently used files.
Answer: a
000 Question: An organization has established an Internet-based VPN connection between their on-premises data center and AWS. They are considering migrating from VPN to AWS DirectConnect. Which operational concern should drive an organization to consider switching from an Internet-based VPN connection to AWS DirectConnect?
  a. AWS DirectConnect provides greater redundancy than an Internet-based VPN connection.
  b. AWS DirectConnect provides greater resiliency than an Internet-based VPN connection.
  c. AWS DirectConnect provides greater bandwidth than an Internet-based VPN connection.
  d. AWS DirectConnect provides greater control of network provider selection than an Internet-based VPN connection.
Answer: c
000 Question: Amazon recommends that you leave all security groups in web facing subnets open on port 22 to 0.0.0.0/0 CIDR, that way you can connect wherever you are in the world. 
  a. true
  b. false
Answer: b
000 Question: A_____is the concept of allowing (or disallowing) an entity such as a user, group, or role some type of access to one or more resources
  a. user
  b. AWS Account
  c. resource
  d. Permission
Answer: d
000 Question: When I create a new security group, all outbound traffic is allowed by default.
  a. true
  b. false
Answer: a
000 Question: You are putting together a wordpress site for a local charity and you are using a combination of Route53, Elastic Load Balancers, EC2 & RDS. You launch your EC2 instance, download wordpress and setup the configuration files connection string so that it can communicate to RDS. When you browse to your URL however, nothing happens. Which of the following could NOT be the cause of this.
  a. You have forgotten to open port 80/443 on your security group in which the EC2 instance is placed. 
  b. Your elastic load balancer has a health check which is checking a webpage that does not exist, therefore your EC2 instance is not in service.
  c. You have not configured an ALIAS for your A record to point to your elastic load balancer
  d. You have locked port 22 down to your specific IP address therefore users cannot access your site using HTTP/HTTPS
Answer: d
000 Question: In a default VPC, all Amazon EC2 instances are assigned 2 IP addresses at launch, what are these?
  a. Private IP and Public IP
  b. Public IP and Secret IP
  c. Elastic IP and Public IP
  d. IPv6 and Elastic IP
Answer: a
000 Question: In S3 with RRS the availability is
  a. 99.999999999%
  b. 100%
  c. 99%
  d. 99.99%
Answer: d
000 Question: You can conduct your own vulnerability scans within your own VPC without alerting AWS first.
  a. true
  b. false
Answer: b
000 Question: In RDS, changes to the backup window take effect
  a. After 30 mins
  b. The next day
  c. Immediately
  d. you cannot back up in RDS
Answer: c
000 Question: Can you access Amazon EBS Snapshots?
  a. Yes, through the AWS APIs/CLI & AWS Console
  b. No
  c. Depends on the region
  d. EBS does not have snapshot functionality
Answer: a
000 Question: The service to allow Big Data Processing on the AWS platform is known as AWS "Elastic Big Data".
  a. true
  b. false
Answer: b
000 Question: In RDS, what is the maximum size for a Microsoft SQL Server DB Instance with SQL server Express edition?
  a. 10GB/db
  b. 100GB/db
  c. 1TB/db
  d. 2TB/db
Answer: a
000 Question: What action is required to establish an Amazon Virtual Private Cloud (VPC) VPN?
  a. Assign a static internet-routable IP address to an Amazon VPC customer gateway
  b. Use a dedicated network address translation instance in the pubic subnet
  c. Modify the main route table to allow traffic to a network address translation instance
Answer: a
Question 1: You work in the security industry for a large consultancy. A new customer of yours runs a production environment in AWS and they require a log of all API calls made to their Elastic Load Balancer. How can you achieve this?
  a. Enable Clo¸udWatch on the ELB
  b. Enable Cloud Trail on the ELB
  c. Enable Detailed Monitoring on the ELB when first creating the instance
  d. Enable Cloud Audit on the ELB when first creating the instance
answer: b
Question 2: True or False: Amazon will always have root level SSH access in to your EC2 instances.
  a. true
  b. false
answer: b
Question 3: You have a static HTML website that requires inexpensive, highly available hosting solution that scales automatically to meet traffic demands. Which AWS service would best suit this requirement?
  a. EC2 with EBS behind and Autoscaling Group with a minimum configuration of 2
  b. EC2 with EBS behind and Autoscaling Group with a minimum configuration of 1
  c. S3 - Static Website Hosting
  d. cloudfront
answer: c
Question 4: True or False: You should expect the same latency and throughput performance as Amazon S3 Standard when using Standard - IA. 
  a. true
  b. false
answer: a
Question 5: You have a website that allows users in third world countries to store their important documents safely and securely online. Internet connectivity in these countries is unreliable, so you implement multipart uploads to improve the success rate of uploading files. This works well, however you notice that when an object is not uploaded successfully, incomplete parts of that object are still being stored in S3 and you are still being charged for those objects. What S3 service can you implement to expire incomplete multipart uploads?
  a. S3 Lifecycle Policies
  b. Reduced Redundancy
  c. Cloud Watch which triggers a Lambda function to delete the data
  d. Data Pipeline with auto-delete
answer: a
Question 6: What is the durability of S3 - IA?
  a. 99%
  b. 99.99%
  c. 99.999999999%
  d. 95%
answer: c
Question 7: What is the minimum time interval granularity for the data that Amazon CloudWatch receives and aggregates?
  a. 30 seconds
  b. 1 minute
  c. 5 minutes
  d. 10 minutes
answer: b
Question 8: True or False: S3 does not support website redirects.
  a. true
  b. false
answer: b
Question 9: You need to automatically migrate objects from one S3 storage class to another based on the age of the data. What S3 service can you use to achieve this?
  a. infrequent access
  b. life cycle management
  c. reduced redundency
  d. glacier
answer: b
Question 10: You work for an electric car company that has its front end website on EC2. Company policy dictates that you must retain a history of all EC2 API calls made on your account for security analysis and operational troubleshooting purposes. What AWS service can assist you with this?
  a. cloud watch
  b. cloud front
  c. cloud trial
  d. cloud tracker
answer: c
Question 11: True or False: An Amazon Cluster Placement Group can be stretched across multiple availability zones?
  a. true
  b. false
answer: b
Question 12: Your three AWS accounts (A, B and C) share data.  In an attempt to maximize performance between the accounts, you place all the instances for these accounts in 'eu-west-1b'.  During testing, you find almost no transfer latency between accounts A and B, but significant latency between accounts B and C, and accounts C and A.  Which of the following possibilities is the most likely source of the problem?
  a. The names of the AZs are randomly applied, so 'eu-west-1b' is not the same location for all three accounts
  b. You have incorrectly configured the cross account authentication policies in account C adding latency to those instances.
  c. Account C has been allocated to an older section of the Data Hall with slower networking. 
  d. The instances for account C are on an overloaded Host.  Stop all the Account C instances  and then start them together so that they run an a new host.
answer: a
Question 13: True or False: You can use S3 Transfer Acceleration with multipart uploads.
  a. true
  b. false
answer: a
Question 14: You have built an online dating application that allows users to send and receive photos as they court each other. You need to secure this data and you need to implement server-side encryption to protect this data. You decide that you want server-side encryption provided by Amazon. You will also need to have an audit trail so you can see who used your key to access which object and when, as well as view failed attempts to access data from users without permission to decrypt the data. What out of the box Amazon solution would enable you to achieve this?
  a. SSE-S3
  b. SSE-C
  c. SSE-KMS
  d. Amazon S3 Encryption client
answer: c
Question 15: Which of the following is NOT a valid EC2 instance type?
  a. D2
  b. C4
  c. M3
  d. Z2
answer: d
Question 16: You work for a large insurance company that has issued 10,000 insurance policies. These policies are stored as PDFs. You need these policies to be highly available and company policy says that the data must be able to survive the simultaneous loss of two facilities. What storage solution should you use?
  a. A single EC2 instance with an EBS volume provisioned as a secondary volume.
  b. S3
  c. Glacier
  d. Route53
answer: b
Question 17: You are a solutions architect working for a company that conducts surveys on specific industries. Each industry that you survey has its own EC2 fleet, separate from those of other industries. Company policy dictates that you should keep costs to a minimum, using only 1 load balancer, if possible. What type of load balancer should you use to suit this requirement?
  a. Classic Load balancer
  b. Application Load balancer
  c. Elastic load balancer with IDS
  d. Elastic load balancer with IPS
answer: b
Question 18: In the future, you will need to preserve, restore, and retrieve every version of every file that you have stored in AWS. Which service should you use?
  a. EC2 with an additional EBS volume, in conjunction with CloudWatch
  b. RDS
  c. Glacier
  d. S3 with version enabled
answer: d
Question 19: You need to restore an object from Glacier. What 2 ways can you accomplish this?
  a. Using the glacier API
  b. Using S3 API
  c. Using aws console
  d. Using the aws command line interface and the s3 subcommand
answer: b, c
Question 20: What is the Uptime SLA for Amazon EC2 and EBS within a given region?
  a. 99%
  b. 99.5%
  c. 99.95%
  d. 100%
answer: c
Question 21: What is the minimum object size for S3 - IA?
  a. 1KB
  b. 0 bytes
  c. 1 byte
  d. 128KB
answer: d
Question 22: You have designed an application that stores large videos in S3. These videos are usually larger than 100Mb in size. You need to maximize upload performance. Select two answers that will achieve this end. 
  a. Design the application to use multipart upload, so that the file is split in to multiple parts which are then uploaded simultaneously.
  b. Require the users to use Direct Connect in order to use to application so as to maximize the upload bandwidth.
  c. Utilize S3 Transfer Acceleration.
  d. Implement a third party CDN solution.
answer: a, c
Question 23: You have an application that uses S3 to store objects. Company policy dictates that certain objects (such as JPGs and PDF's) must be replicated to another region for redundancy. However, some objects (such as Word files) can stay in a single region. Company policy also dictates that you should use as few buckets as possible. How should you architect this solution?
  a. Two buckets, 1 with CRR enabled on it (for the word files) and the other bucket without.
  b. Two buckets 1 with CRR enabled on it (for the JPGs and PDF's) and the other without.
  c. One bucket and then enable CRR on just a subset of objects (such as JPGs and PDF's) uploaded by specifying prefixes.
  d. Three buckets. 1 with CRR enabled on it for the JPG's, 1 with CRR enabled on it for the PDF's and 1 bucket just for the word files with no CRR enabled on it.
answer: d
Question 24: You back the files that exist on an in-house SAN to S3. You need to minimize cost, however company policy states that objects must be instantly accessible. What S3 storage class should you use?
  a. S3-RRS
  b. S3-IA
  c. S3
  d. Glacier
answer: b
Question 25: You need to implement a new web application which allows users to store family photos online in such a way that only invited guests will be able to view the images. Which type of S3 encryption should you choose to  maintain full end-to-end control of the encryption/decryption of objects and assure that only encrypted objects are transmitted over the Internet to Amazon S3.
  a. SSE-S3
  b. SSE-C
  c. SSE-KMS
  d. Amazon S3 encryption client
answer: d
Question 26: True or False: Classic ELB's support IPv6 as well as IPv4.
  a. true
  b. false
answer: a
Question 27: Your company has a legacy SAN that has 75 TB's of data. Your company has decided that they want to migrate this data to AWS S3 in the quickest way possible. You company has a single comms line with a maximum pipe line of 50Mbps  Which service should you consider using?
  a. S3 transfer acceleration
  b. Snowball
  c. Direct Connect
  d. FTP
answer: b
Question 28: Which EC2 operating system is NOT supported by CloudWatch
  a. Amazon Linux
  b. Debian
  c. Ubuntu
  d. None of the above, all EC2 operating systems are supported by cloud watch
answer: d
Question 29: How can you securely upload ordownload your data to/from the S3 service?
  a. SSL endpoint using the HTTPS protocol
  b. SSL endpoint using the HTTP protocol
  c. HTTP endpoint using the HTTPS protocol
  d. HTTP endpoint using the HTTP protocol
answer: a, c
Question 30: Which types of server side encryption are available for S3? (Choose all that apply.)
  a. SSE-S3
  b. SSE-C
  c. CSE-AWS
  d. SSE-KMS
answer: a, b, c
Question 31: Your legal company is moving its production estate to AWS. They currently have a private cloud platform with VMDK files as their virtual machines. You need to move these files to AWS and create EC2 instances using the VMDK files. Which AWS service would help you achieve this goal?
  a. CloudMigration
  b. VM Import/Export
  c. VM Migrate
  d. Data Pipeline
answer: b
Question 32: You are running a Cassandra database that requires access to tens of thousands of low latency IOPS. What EC2 instance family would best suit your needs?
  a. Cluster GPU instances
  b. Hight I/O instances
  c. Dense storage instances
  d. Memory optimized instances
answer: b
Question 33: You are creating an application that will leverage EC2 for its webservers. The application data will be stored on the root device volume attached to the EC2 instance. Data on this volume must persist independently of the life of this particular instance. What EC2 volume should you choose?
  a. local instance storage
  b. EBS
  c. networked instance storage
  d. Lambda
answer: b
Question 34: What is the availability of S3 - IA
  a. 99.90%
  b. 99%
  c. 99.999999999%
  d. 95%
answer: a
Question 35: You run a security company which stores highly sensitive PDF's on S3 with versioning enabled. To ensure MAXIMUM protection of your objects to protect against accidental deletion, what further security measure should you consider using?
  a. Setup a cloud watch alarm so that if an object in S3 is deleted, this will trigger an alarm and send an SNS notification to your phone.
  b. S3-KMS
  c. Configure the application to use SSL endpoints using the HTTPS protocol.
  d. Enable versioning with MFA Delete on your S3 bucket.
answer: d
Question 36: You work for a security company that stores highly sensitive documents on S3. One of your customers has had a security breach and, as a precaution, they have asked you to remove a sensitive PDF from their S3 bucket. You log in to the AWS console using your account and attempt to delete the object. You notice that versioning is turned on, and when you dig a little deeper you discover that you cannot delete the object. What may be the cause of this?
  a. You can never permanently delete an object on S3 after versioning is enabled.
  b. You cannot delete the object because you are not the bucket owner.
  c. You must be logged in as a Super User to delete objects.
  d. S3 server-side encryption is preventing you from doing this.
answer: b
Question 37: True or False: You can use your existing Microsoft Windows Serverlicenses with anAmazon EC2 shared tenancy instance.
  a. true
  b. false
answer: b
Question 38: By default, how many Elastic IP addresses are you limited to per region?
  a. 5
  b. 10
  c. 15
  d. 20
answer: 5
Question 39: True or False: EBS Snapshots are versioned and you can read an older snapshot to do a point-in-time recovery?
  a. true
  b. false
answer: a
Question 40: You have an extremely high performance compute application that you need to deploy to AWS. You will need extremely low-latency network performance to allow node-to-node communication between your EC2 instances. You will also need a minimum network speed of 10 Gbps in order for your application to work. How should you deploy your instances?
  a. using a private VPC
  b. By creating a cluster placement group
  c. by deploying in multiple AZ
  d. By using CloudFront to cache static assets so as to increase performance
answer: b
Question 41: By default, how many S3 buckets can you have  with a new AWS account?
  a. 25
  b. 50
  c. 100
  d. 200
answer: c
Question 42: Which of the following operating systems is NOT supported by EC2
  a. Amazon Linux
  b. Ubuntu
  c. OSX
  d. Windows Server
answer: c
Question 43: You have developed a file-sharing website for a large corporate entity. They require that the site has regional redundancy. Which S3 service should you use to achieve this?
  a. S3 Standard
  b. S3-RRS with data pipeline to dynamoDB
  c. Configure a lambda function with a trigger of S3, so that when an object is uploaded to S3, it is automatically replicated to EBS.
  d. S3 - CRR
answer: d
Question 44: You have been load testing a customers new production environment. You create the environment using CloudFormation and you utilize CloudWatch to monitor the environment. After extensive load testing, you are ready to hand the cloudformation template over to your customer. You delete the environment and give your customer the CloudFormation template. However, they now want to see the results of the load test. How long does CloudWatch store the metrics for EC2 &amp; ELB after deleting those resources?
  a. 24 hours
  b. 48 hours
  c. 1 week
  d. 2 weeks
answer: d
Question 45: Which of the following statements is TRUE.
  a. You are able to attach multiple EBS volumes to an EC2 instance.
  b. You are able to attach multiple EC2 instances to an EBS Volume.
  c. It is possible to configure an Autoscaling Group to repair degraded EBS volumes, without the need to terminate the EC2 instances.
  d. It is possible to use Autoscaling with EBS, rather than EC2.
answer: a
Question 46: What are the two different types of virtualization available on AWS?
  a. Hardware Virtual Machine
  b. Physical Virtual Machine
  c. Paravirtual Machine
  d. Cloud Virtual Machine
answer: a, c
Question 47: You’ve been tasked with implementing a globally accessible storage solution that will scale from a few terabytes (now) to an unknown, but significantly greater, volume of data in three years time. Which AWS service would best meet your current and projected storage needs?
  a. EC2 with EBS
  b. S3
  c. RDS
  d. DynamoDB
answer: b
Question 48: Your large scientific organization needs to use a fleet of EC2 instances to perform high performance, CPU intensive calculations. Your boss asks you to choose an instance type that would best suit the needs of your organization. Which of the following instance types should you recommend?
  a. C4
  b. M3
  c. D2
  d. R3
answer: a
Question 49: You have an application that stores data in  S3, and you need to design an integrated solution providing encryption at rest. You want Amazon to handle key management and protection using multiple layers of security. Which S3 encryption option should you use?
  a. SSE-S3
  b. SSE-C
  c. SSE-KMS
  d. Aamzon S3 encryption client
answer: a
Question 50: You have an application that allows people in very remote locations to store their files safely and securely. You need to leverage Amazon CloudFront’s globally distributed AWS Edge Locations so that as data arrives at an AWS Edge Location the data is routed to your Amazon S3 bucket over an optimized network path. Which service should you use?
  a. CloudFront transfer acceleration
  b. S3 Transfer acceleration
  c. S3 multipart upload
  d. CloudFront multipart upload
answer: b
Question 51: Which of the following protocols is not supported with an Elastic Load Balancer
  a. HTTP
  b. HTTPS
  c. RDS
  d. SSH
answer: c, d
Question 52: CRR replicates every object-level upload that you make directly to your source bucket. Which of the following also forms a part of that replication?
  a. the object metadata
  b. The Object ACL's
  c. the object ssl certificate
  d. the object's checksum encryption data
answer: a, b
Question 53: Can you use IPv6 with Amazon S3?
  a. yes
  b. yes, however you need ipv4 to ipv6 translation software
  c. yes, however you need ipv6 to ipv4 translation software
  d. no
answer: a
Question 54: You work for a genetics company that has extremely large datasets stored in S3. You need to minimize storage costs, while maintaining mandated restore times that depend on the age of the data. Data 30-59 days old must be available immediately,  and data ≥ 60 days old must be available within 12 hours. Which two of the following options below should you consider?
  a. S3 - RRS
  b. S3-IA
  c. Glacier
  d. CloudFront
answer: b, c
Question 55: How quickly can objects be restored from Glacier?
  a. with in 30 minutes
  b. with in 1 hour
  c. with in 2 hours
  d. 3-5 hours
answer: d
Question 56: What is the minimum object size for S3 Standard?
  a. 1 KB
  b. 0 bytes
  c. 1 byte
  d. 128 KB
answer: b
Question 57: Your application stores your customers' sensitive passport information in S3. You are required by law to encrypt all data at rest. Company policy states that you must maintain control of your encryption keys. For ease of management however, you do not want to implement or maintain a client side encryption library. Which S3 encryption option should you use to secure your data at rest?
  a. SSE-S3
  b. SSE-C
  c. SSE-KMS
  d. Amazon S3 encryption client
answer: b
Question 58: Which of the following are compute services with AWS?
  a. EC2
  b. ECS
  c. Lambda
  d. Glacier
answer: a, b, c
Question 59: You are a system administrator and you need to take a consistent snapshot of your EC2 instance. Your application holds large amounts of data in cache that is not written to disk automatically. What would be the best approach to taking an application consistent snapshot?
  a. Take a snapshot in real time using the EC2 API.
  b. Shutdown the EC2 instance and detach the EBS volume, then take the snapshot.
  c. Take a snapshot using the AWS CLI.
  d. In the AWS console, take a snapshot and ensure that the "application consistent" check box is ticked.
answer: b
Question 60: Your application requires highly-available object storage, and must comply with EU privacy laws. As such, no data may be stored outside the EU. Which two of the following options should you consider?
  a. A single EC2 instance with an EBS volume provisioned in Eu-West-1. Put this EC2 instance behind an Autoscaling Group with a minimum target of 1.
  b. Use an S3 bucket in EU-West-1
  c. Multiple EC2 instances with an EBS volume provisioned in US-EAST-1. These EC2 instances will use Autoscaling Group with a minimum target of 3, 1 per availability zone.
  d. Use an S3 bucket in EU-Central-1
answer: b, d
Question: You are attempting to move data from one EBS volume to a duplicate volume in a separate region. Which of the following methods will do this best?
  a. Take a snapshot of the EBS volume and copy it to the desired region.
  b. Allow a VPC peering connection to pull the data over.
  c. Move the data to S3 and enable cross-region replication.
  d. Use a Linux tool like rsync to sync the volume to the other region.
answer: a
Question: You have suggested moving your company's web servers to AWS, but your supervisor is concerned about cost. Which of the following deployments will give you the most scalable and cost-effective solution?
  a. An EC2 auto-scaling group that will expand and contract with demand 
  b. A solution that's built to run 24/7 at 100% capacity, using a fixed number of T2 Micro instances
  c. A hybrid solution that leverages on-premise resources
  d. none of the above
answer: a
Question: You have an IO intensive database in your production environment that requires regular backups. You need to configure them in such a way so that when an automated backup is taken, it does not impact your production environment. What RDS option should you choose to help you accomplish this? 
  a. multi-az
  b. read replicas
  c. use redshift for your backup environment
  d. cross region failover
answer: a
Question: Your company needs to run several monthly workloads that will each take several hours to complete. Although critical, these workloads can be stopped and restarted without adversely affecting the outcome of the job. Which pricing model would you use to deliver the most economical solution?
  a. on-demand instances
  b. reserved instances
  c. spot instances
  d. free-tier instances
answer: c
Question: Your fleet of EC2 instances is running 100% of the time, and there is no reason to believe that the demand will decrease. What pricing model could you use to reduce costs?
  a. special instances
  b. spot instances
  c. on-demand instances
  d. reserved instances
answer: d
Question: Your existing on-premise servers rely on Memcached to provide memory object caching. If you were to move to AWS, how might you preserve this functionality?
  a. install memcached on EC2
  b. elastic mapreduce (EMR)
  c. elasticache
  d. noen of the above
answer: c
Question: True or False: there is a cost associated with transferring from Amazon S3 to an EC2 instance in the same Region.
  a. true
  b. false
answer: b
Question: You have heavy load on your RDS database which is now the maximum available size possible. Which two of the following AWS technologies should you use to further ease the load?
  a. RDS read replica
  b. RDS multi-az
  c. elasticache
  d. cloudformation
answer: a, c
Question: You have a small database workloads with infrequent I/O. Which storage medium would the most cost-effective way to meet these requirements?
  a. Amazon RDS Provisioned IOPS (SSD) Storage
  b. Amazon RDS General Purpose (SSD) Storage
  c. Amazon RDS Magnetic Storage
  d. Amazon RDS Cold Storage
answer: c
Question: You have a very heavily-trafficked Wordpress blog that has approximately 95% read traffic and 5% write traffic. You notice that the blog is getting slower and slower. You discover that the bottleneck is in your RDS instance. Which two of the following answers can improve your Wordpress blog's performance?
  a. Create a number of read replicas and update the connection string on your EC2 instances so that traffic is evenly shared amongst these new RDS instances.
  b. Use Elasticache to cache the most commonly read posts of your Wordpress blog.
  c. Create a secondary Multi-AZ database and run the queries off the secondary Multi-AZ database.
  d. Export the database to DynamoDB which has push button scaleability.
answer: a, b
Question: True or False: You should store your Access Keys in an AMI.
  a. true
  b. false
answer: b
Question: You need to upgrade your RDS database to a larger instance class and you must minimize the amount of disruption to your business as much as possible. What should you do.
  a. Schedule the upgrade for a maintenance window during a time when you have the least customers possible. The production database should only be unavailable for a couple of minutes.
  b. You do not need to worry: when upgrading an instance class, your database will not go off line.
  c. Do the upgrade using the AWS console and ensure the "do not reboot" option is checked when upgrading.
  d. Do the upgrade using the AWS CLI using the option --NOREBOOT
answer: a
Question: Which of the following AWS services store data as key-value pairs?
  a. dynamodb
  b. ec2
  c. rds
  d. s3
answer: a, d
Question: You are running a production database using MySQL on RDS. From time to time, management asks you to run highly complex SQL queries with multiple table joins against the database. These queries often overwhelm your database, and the production environment is beginning to be affected. Which of the following would you recommend as a means of reducing the load on the database?
  a. Migrate the database to DynamoDB which will scale automatically in order to deal with the load.
  b. Use Route53 health checks to determine the current load on the database and if there is a minimum load , configure the health check to run the SQL queries.
  c. Create a secondary Multi-AZ database and run the queries off the secondary Multi-AZ database.
  d. Create a read replica of the database and run your reports against the read replica, rather than the production database.
answer: d
Question: Which of the following services allows you to have root level access to the underlying operating system
  a. EMR
  b. EC2
  c. RDS
  d. DynamoDB
answer: a, b
Question: You've been tasked with the implementation of an offsite backup/DR solution. You'll only be responsible only for flat files and server backup. Which of the following would you include in your proposed solution (select all that apply.)?
  a. EC2
  b. storage gateway
  c. snowball
  d. s3
answer: b, c, d
Question: You've enabled website hosting on a bucket called "aspiring-guru" in the us-west-2 Region. Which of the following is the URL that will be assigned to your website?
  a. aspiring-guru.s3-website-us-west-2.amazonaws.com
  b. s3-website-us-west-2.aspiring-guru.amazonaws.com
  c. s3-website.aspiring-guru-us-west-2.amazonaws.com
  d. none of the above
answer: a
Question: You are auditing your RDS estate and you discover an RDS production database that is not encrypted at rest. This violates company policy and you need to rectify this immediately. What should you do to encrypt the database as quickly and as easy as possible.
  a. Use the RDS Import/Export Wizard to migrate the unencrypted RDS instance across to a new encrypted database.
  b. Take a snapshot of your unencrypted DB Instance and then restore it making sure you select to encrypt the new copy.
  c. Use AWS Database Migration Service
  d. Create a new DB Instance with encryption enabled and then manually migrate your data into it.
answer: d
Question: You need to develop an infrastructure that can be replicated and deployed in another AWS Region in a matter of minutes. Which AWS service might you use to build a reproducible, version-controlled infrastructure? 
  a. EC2 AMIs with EBS snapshots
  b. Elastic Beanstalk
  c. CloudFormation
  d. Cloudwatch Template
answer: c
Question: Your on-premise servers are running low on disk storage space, but your company is not yet ready for a complete move to the public cloud. You've been tasked with finding an interim storage solution that also offers backup and archiving capabilities. Which AWS service would you recommend to meet this immediate need?
  a. snowball
  b. storage gateway with gateway cached volume
  c. directconnect
  d. storage gateway with gateway stored volume
answer: b
Question: Your AWS environment contains several reserved EC2 instances dedicated to a project that has just been cancelled. You need to recoup the cost of these reserved instances, and you need to preserve the data for future use. What can you do to minimize charges for these instances?
  a. Take snapshots of the EBS volumes and terminate the instances.
  b. Contact AWS and ask them to release you from your Reserved Instance purchase.
  c. Stop the instances and retain them for future use.
  d. Sell the unused instances on the AWS Reserved Instance Marketplace.
answer: a, d
Question: You must to encrypt all incoming and outgoing traffic between your servers and your customers. Your fleet of EC2 instances lives inside a public subnet and behind an elastic load balancer. Your application is very CPU intensive, and you want to minimize the processing load these EC2 instances must bear. What should you do?
  a. Install the SSL certificates on each EC2 instance and allow them to do the encryption/decryption with your customers.
  b. Install the SSL certificates on your ELB's so that there is less load on the EC2 instances.
  c. Use API Gateway to offload the SSL certificate, reducing the amount of load on both your ELB and EC2 instances.
  d. Configure a NAT and install the EC2 instance on that NAT so that you offload SSL termination to a third party EC2 instance and not your production environment.
answer: b
Question: The company you work for is considering a move to AWS, but they are concerned that their current, 50Mbps connection will not be able to handle the 100 TB of data that need to be migrated without causing unacceptable downtime. As their solutions architect, which AWS service would you recommend to move this data?
  a. snowball
  b. s3 with transfer acceleration
  c. aws direct connect
  d. aws storage gateway
answer: a
Question: One of your junior developers needs access to an Elastic Load Balancer in your custom VPC. This is the first and only time he will need access to AWS services. Which of the following choices is the most secure way to grant this access?
  a. Create a new IAM user with the required credentials.
  b. Let them log in with Admin credentials and change the Admin password when he is finished.
  c. Add that developer to a Group with the requisite access.
  d. none of the above
answer: a
Question: Which of the following are true about Amazon S3-RRS?
  a. S3-RRS offers 99.99% availability.
  b. S3-RRS offers 99.999999999 durability
  c. S3-RRS offers 99.99% durability.
  d. S3-RRS is most often used with reproducible objects.
answer: a, c, d
Question: The customer service organization at your company just told you that a client’s purchase from your website was processed twice. Your order process involves EC2 instances processing messages from an SQS queue. What changes might you make to ensure this does not happen again?
  a. Rewrite the order-processing workflow to use SWF, rather than SQS.
  b. Increase the visibility timeout on the SQS queue
  c. Switch to long-polling
  d. Manually delete the order after processing.
answer: a
Question: True or False: By default, Amazon RDS enables automated backups of your DB instance with a 1-day retention period.
  a. true
  b. false
answer: a
Question: It is best practice to use Access Keys whenever possible, rather than IAM Roles.
  a. true
  b. false
answer: b
Question: True or False: Availability Zones in a given Region are connected by low-latency links, facilitating the development of fault-tolerant, high-availability applications.
  a. true
  b. false
answer: a
Question: You have a custom VPC for your organization. You discover that one of your developers has created an RDS instance in the default VPC and this is in violation of company policy. You need to create this RDS instance inside your custom VPC with as little effort as possible. What should you do?
  a. Use the RDS Import/Export Wizard to Migrate the RDS instance across to the custom VPC
  b. Use AWS Database Migration Service
  c. Take a snapshot of your DB Instance in the default VPC and restore it to VPC by specifying the DB Subnet Group you want to use in your custom VPC.
  d. Use the command "aws rds mv dbname < VPC"
answer: c
Question: You are working for a real estate company and you need to be able to record configuration changes to Amazon RDS DB Instances, DB Subnet Groups, DB Snapshots, DB Security Groups, and Event Subscriptions. What AWS service should you use to achieve this?
  a. cloud trail
  b. cloud watch
  c. cloud audit
  d. aws config
answer: d
Question: Which AWS service should you use to host MySQL, MariaDB, Oracle, SQL Server, or PostgreSQL database where you do not need to manage the underlying operating system?
  a. dynamoDB
  b. RDS
  c. aurora
  d. EC2 with EBS
answer: b
Question: You have an RDS database that has moderate I/O requirements. Which storage medium would be best to accommodate these requirements?
  a. Amazon RDS Provisioned IOPS (SSD) Storage
  b. Amazon RDS General Purpose (SSD) Storage
  c. Amazon RDS Magnetic Storage
  d. Amazon RDS Cold Storage
answer: b
Question: The large manufacturing company you work for is interested in moving their production estate to AWS. They run a Joomla store which utilizes MySQL on the back end. Currently, they also use clustered MySQL databases in an active/passive configuration at a single site. By moving to AWS they want an active/passive configuration across 2 geographically distinct locations, with automatic failover between the two. As their solutions architect, which of the following RDS options should you recommend?
  a. multi-az
  b. read replicas
  c. cross region replication
  d. cross region failover
answer: a
Question: You have a production application that is on the largest RDS instance possible, and you are still approaching CPU utilization bottlenecks. You have implemented read replicas, ElastiCache and even CloudFront and S3 to cache static assets, but you are still bottlenecking. What should be your next step?
  a. You should implement database partitioning and spread your data across multiple DB Instances.
  b. You have reached the limits of public cloud. You should get a dedicated database server and host this locally within your own data center.
  c. You should consider using RDS Multi-AZ and using the secondary AZ nodes as read only nodes to further offset load.
  d. You should provision a secondary RDS instance and then implement and ELB to spread the load between the two RDS instances.
answer: a
Question: The insurance company you work for is implementing new IT security policies for all RDS instances. In the future, you will need to perform both security analyses and operational troubleshooting on your RDS estate. As such, you will need a history of all RDS API calls made on your account. What AWS service should you use to achieve this?
  a. cloud audit
  b. cloud watch
  c. cloud front
  d. cloud trail
answer: d
Question: What are the two different ways of automating your RDS backups?
  a. automated backups
  b. using s3
  c. automated snapshots
  d. using data pipeline
answer: a, c
Question: What type of replication is supported by read replica instances?
  a. synchronous replication
  b. asynchronous replication
  c. continuous replication
  d. sequencial replication
answer: b
Question: Which three of the following statements are not true?
  a. EBS Volumes can be attached to multiple instance simultaneously.
  b. EBS Volumes cannot be attached to an EC2 instance in another AZ.
  c. EBS Volumes are ephemeral.
  d. EBS Volumes can be attached to an EC2 instance in another AZ
answer: a, c, d
Question: You need to configure a new subnet in your VPC for a database cluster you are building. The subnet will never need more than six IP addresses. Which of the following is the best choice for this subnet?
  a. A /28 private subnet
  b. A /28 public subnet
  c. A /16 public subnet
  d. A /16 private subnet
answer: a
Question: An Availability Zone comprises multiple Regions
  a. true
  b. false
answer: b
Question: Which three of the following events would cause Amazon RDS to initiate a failover to the standby replica?
  a. Loss of availability in primary Availability Zone
  b. Loss of network connectivity to primary
  c. Compute unit failure on primary
  d. Storage failure on secondary
answer: a, b, c
Question: What is the minimum size of an SSD EBS Volume?
  a. 1 byte
  b. 1 GiB
  c. 1 MB
  d. 1 GB
answer: b
Question: True or False: An application designed for fault tolerance and high availability should almost always be built across multiple Availability Zones
  a. true
  b. false
answer: a
Question: You are auditing your company's RDS estate, and you discover a database that is in a single Availability Zone – a violation of company policy. You decide to convert this to a multi-AZ deployment. Which three of the following things will happen?
  a. A snapshot of your primary instance is taken
  b. Synchronous replication is configured between primary and standby instances
  c. A new standby instance is created in a different Availability Zone, from the snapshot
  d. asynchronous replication is configured between primary and standby instances
answer: a, b, c
Question: True or False: In addition to hosting domains, Route 53 serves as a domain registrar.
  a. true
  b. false
answer: a
Question: Your SQL server requires a specific type of collation and some unique third party tools installed on it. You will need access to the underlying operating system for management and monitoring of these third party tools. However, you'd like to keep the overall amount of management to a minimum. Which AWS service would best suit your needs?
  a. RDS with SQL Server
  b. dynamoDB
  c. SQL server installed on EC2 with EBS
  d. ElastiCache
answer: c
Question: True or False: It's possible to have a Multi-AZ copy of your read replica?
  a. true
  b. false
answer: b
Question: Your data warehousing company has a number of different RDS instances. You have a medium size instance with automated backups switched on and a retention period of 1 week. One of your staff carelessly deletes this database. Which two of the following apply.
  a. The automatic backups are deleted when the instance is deleted.
  b. The automated backups will be retained for 2 weeks and then deleted after the 2 weeks has expired.
  c. A final snapshot will be created upon deletion automatically.
  d. A final snapshot MAY have been created when the instance was deleted, depending on whether the 'SkipFinalSnapshot' parameter was set to 'False.'
answer: a, d
Question: True or False: A Region is another name for an Edge Location.
  a. true
  b. false
answer: b
Question: You've been tasked with replicating your production VPC in another region for disaster recovery purposes. Part of your environment relies on EC2 instances with preconfigured software. What steps would you take to configure the instances in another region?
  a. Create AMIs of the instances and deploy them in the new Region
  b. Create AMIs of the instances and copy them to the new Region for deployment.
  c. Write the IAM permissions for the new Region to use the AMIs from the original Region.
  d. None of the above
answer: b
Question: From the command line, which of the following should you run to get the public hostname of an EC2 instance?
  a. curl http://169.254.169.254/latest/meta-data/public-hostname
  b. curl http://254.169.254.169/latest/user-data/public-hostname
  c. curl http://254.169.254.169/latest/meta-data/public-hostname
  d. curl http://169.254.169.254/latest/user-data/public-hostname
answer: a
Question: Amazon RDS supports which of the following databases:
  a. MariaDB
  b. MySQL
  c. DB2
  d. Sybase
answer: a, b
Question: True or False: EBS Volumes are hard-disks in the cloud.
  a. true
  b. false
answer: a
Question: Which database engines support read replicas?
  a. SQL Server
  b. Oracle
  c. MySql
  d. PostgreSql
answer: c, d
Question: You've been tasked with setting up an S3 solution to store large amounts of critical data. With high availability and fault-tolerance in mind, what further safeguards should you implement to protect your data in the event that an entire AZ was lost to a natural (or similarly catastrophic) disaster?
  a. Nothing: S3 is a global service and is not affected by the loss of an availability zone.
  b. Use lifecycle policies to copy the data to Glacier.
  c. Deploy a gateway-stored AWS Storage Gateway.
  d. None of the above
answer: a
Question: What is the maximum retention period for RDS automated backups?
  a. 7 days
  b. 2 weeks
  c. 1 month
  d. 35 days
answer: d
Question: Which two of the following characterize a scalable and reliable solution on AWS?
  a. A scalable application will be resilient and operationally efficient
  b. A scalable solution applies elasticity at the expense of cost.
  c. A scalable solution will decrease in cost at scale.
  d. A scalable solution applies elasticity, but is cost-agnostic.
answer: a, c
Question: You have an RDS database that has high performance OLTP workloads. Which storage medium would be best to accommodate these requirements?
  a. Amazon RDS Provisioned IOPS (SSD) Storage
  b. Amazon RDS General Purpose (SSD) Storage
  c. Amazon RDS Magnetic Storage
  d. Amazon RDS Cold Storage
answer: a
Question: What type of replication is supported by Multi-AZ RDS instances?
  a. synchronous replication
  b. asynchronous replication
  c. continuous replication
  d. sequential replication
answer: a
Question: Using the AWS Server Migration Service, what's the maximum number of VMWare VMs that can be migrated concurrently?
  a. 10
  b. 25
  c. 50
  d. 100
answer: c
Question: True or False: S3 provides read-after-write consistency for overwrite PUTS and DELETES.
  a. true
  b. false
answer: b
Question: Which of the following is an invalid VPC pairing configuration?
  a. You have a VPC peering connection between VPCs A and B. They are in the same AWS account, and they do not have overlapping CIDR blocks.
  b. VPC A has peering connections to VPCs B and C. All three VPCs are in the same AWS account, and there are no overlapping CIDR blocks.
  c. You have a VPC peering connection between VPC A and VPC B. VPC A also has a VPN connection to a corporate network. You use VPC A to extend the peering relationship to exist between VPC B and the corporate network so that traffic from the corporate network can directly access VPC B by using the VPN connection to VPC A.
  d. You have peered three VPCs in a full-mesh configuration. The VPCs are in the same AWS account and do not overlapping CIDR blocks.
answer: c
Question: Your application's usage peaks at 90% during the hours of 9 AM and 10 AM everyday. All other hours require only 10% of the peak resources. What is the best way to scale your application so you're only paying for max resources during peak hours?
  a. Proactive event-based scaling
  b. Proactive cyclic scaling
  c. Reactive event-based scaling
  d. Reactive cyclic scaling
answer: b
Question: Your image manipulation application allows users take a picture, upload it to your app, and request filters to be added to the image. You need to decouple the application so your users are not waiting for the image processing to take place. How would you go about doing this?
  a. Use Lambda to process the images.
  b. Use S3 to store the images and EC2 to process the requests.
  c. Use Amazon SQS to store the requests using metadata and JSON in the message, use S3 to store the image, and Auto Scaling to determine when to fire off more worker instances based on queue size.
  d. Integrate with DynamoDB to allow messages to be sent back and forth between worker instances and EC2 instances.
answer: c
Question: True or False: For a successful cross-region replication of your S3 bucket, versioning must be enabled on both the source and target buckets.
  a. true
  b. false
answer: a
Question: Contractual requirements mandate the use of AWS CloudHSM as an encryption solution. Application performance is a secondary, but important, concern. Where within your AWS infrastructure should you place the HSM appliances?
  a. To increase security, you should place the CloudHSM appliances in their own, private subnet.
  b. To increase security, you should place the HSM appliances on your side of the VPN that connects to AWS.
  c. Locating HSM appliances near your EC2 instances decreases network latency, which improves application performance.
  d. To increase performance, you should locate the HSM as close to the majority of your customers as is possible.
answer: c
Question: An AWS VPC allows you to:
  a. Forget about security: AWS does it all for you.
  b. Provision unlimited S3 resources
  c. Connect your cloud resources to your own IPSec VPN connections.
  d. None of the above
answer: c
Question: True or False: Multifactor Authentication is required to delete objects from an S3 bucket.
  a. true
  b. false
answer: b
Question: True or False: you can write objects directly to an edge location.
  a. true
  b. false
answer: a
Question: Which of the following statements about Amazon SQS is true?
  a. SQS will deliver your message at least once, but cannot guarantee that it will not create duplicates of that message.
  b. SQS will deliver your message at least once in FIFO order.
  c. SQS will deliver your message at least once, and guarantees that it will not create duplicates of that message.
  d. SQS will deliver your message at least once, but cannot guarantee the order in which the messages will be delivered.
answer: a, d
Question: True or False: You can attach more than one EC2 instance to an AWS Elastic Block Store volume.
  a. true
  b. false
answer: b
Question: Which of the following statements is FALSE regarding the role of a bastion host?
  a. A bastion host should be protected in a private subnet.
  b. A bastion host is used to SSH into an EC2 instance.
  c. As a bastion host is exposed to the Internet, it should be hardened.
  d. A bastion host sits outside a private subnet and is used as a secure gateway to that internal network.
answer: a
Question: You've been tasked with the creation of a highly available website that serves static content from EC2 instances. Which of the following is not a requirement to accomplish this goal?
  a. Multiple subnets
  b. An auto-scaling group
  c. an SQS queue
  d. A multi-az deployment
answer: c
Question: True or False: you can use IAM policies to deny the Root account access to EC2 instances.
  a. true
  b. false
answer: b
Question: After setting up a VPC peering connection between your VPC and that of your clients, the client requests to be able to send traffic between instances in the peered VPCs using private IP addresses. What must you do to make this possible?
  a. Add a route to a Route Table that's associated with your VPC.
  b. Establish a private peering connection.
  c. Add your instance and the client's instance to a Placement Group.
  d. Use an IPSec tunnel
answer: a
Question: You are trying to establish a VPC peering connection with another VPC, and you discover that there seem to be a lot of limitations and rules when it comes to VPC peering. Which of the following is not a VPC pairing limitation or rule?
  a. You cannot have more than one VPC peering connection between the same VPCs at the same time.
  b. You cannot create a VPC pairing connection between VPCs in different regions.
  c. A placement group cannot span peered VPCs.
  d. You cannot create a VPC pairing connection between VPCs with matching or overlapping CIDR blocks.
answer: c
Question: Your customer is a healthcare company with strict compliance and auditing requirements. As you use AWS to architect the application environment, which of the following services might you use to ensure compliance with their strict requirements?
  a. S3 with versioning enabled
  b. Multi factor authentication
  c. SSE-S3
  d. CloudTrail
answer: d
Question: What determines the cost of using CloudFormation templates?
  a. The published rate of $.10 per template per month
  b. The resources the AWS infrastructure uses to build your environment
  c. There is a cost for CloudFormation only after you have exceeded the 20 free templates you are allowed per month.
  d. There is no cost to using CloudFormation, but you are charged for the resources the template builds.
answer: d
Question: To maintain compliance with HIPPA, all healthcare-related data being stored on Amazon S3 needs to be encrypted at rest. Assuming S3 is being used for storing the data, which two of the following are the preferred methods of encryption?
  a. Enable Server Side Encryption on your S3 bucket. S3 automatically applies AES-256 encryption.
  b. Encrypt the data locally using your own encryption keys and then transfer the encrypted data to S3.
  c. Store the data on encrypted EBS volumes.
  d. Store the data in S3 as EBS snapshots.
answer: a, b
Question: You create an SQS queue and test it by creating a simple application polls the queue for messages. After a message is retrieved, the application should delete it. You create three test messages in your SQS queue and discover that messages 1 and 3 are quickly deleted, but message 2 has remained in the queue. Which two of the following could account for your findings?
  a. Message 2 is invalid
  b. Your application used short-polling
  c. SQS cannot guarantee that messages are retrieved in first-in, first-out (FIFO) order.
  d. The permissions on message 2 were incorrectly written.
answer: b, c
Question: Your company is moving their entire 20 TB data warehouse to the cloud. With your current bandwidth, it would take 2 months to transfer the data. Which service would you use to quickly get your data into AWS?
  a. AWS snowball
  b. AWS direconnect
  c. Amazon S3 data store
  d. Amazon multipart upload
answer: a
Question: Your company provides an online image recognition service that uses SQS to decouple system components. Your application polls the image queue as often as possible to maximize end-to-end throughput. However, you notice that polling in tight loops is burning CPU cycles and increasing costs with empty responses. How can you reduce the number of empty responses?
  a. Enable long polling by setting the ReceiveMessageWaitTimeSeconds to a number > 0
  b. Enable short polling by setting ReceiveMessageWaitTime = 0.
  c. Enable short polling by setting ReceiveMessageWaitTime > 0.
  d. Use AutoScaling to increase the number of instances polling the queue.
answer: a
Question: Which two of the following AWS Services were introduced at re:Invent 2016
  a. Lex
  b. Dax
  c. Polly
  d. Molly
answer: a, c
Question: True or False: Amazon SQS guarantees that each message will be delivered at least once, but cannot guarantee that a message will not be delivered multiple times.
  a. true
  b. false
answer: a
Question: When reviewing Auto Scaling events, it is noticed that an application is scaling up and down multiple times per hour. What design change could you make to optimize cost while preserving elasticity?
  a. Add a Provisioned IOPS volume to the instance.
  b. Increase the number of instances in the Auto Scaling group.
  c. Change the Launch Configuration to use a larger instance type.
  d. Change the scale-down CloudWatch metric to a higher threshold.
answer: d
Question: You've been tasked with architecting a highly available application. After building the initial environment, you've discovered that your current security group configuration does not include a port you need for certain traffic. After adding the port to the appropriate security group, how long will it take for your changes to take effect, allowing your application to function correctly?
  a. It usually takes a couple of minutes for these changes to take effect.
  b. Changes to a security group take effect as soon as they are saved.
  c. Changes will take effect immediately upon reboot of the EC2 instance in question.
  d. 5 minutes
answer: b
Question: When selecting an EC2 instance type for your application, it's important to know which two of the following?
  a. The required number of I/O operations
  b. The memory requirements
  c. The location from which most traffic comes
  d. The peak expected usage
answer: a, b
Question: What is the maximum size of a general-purpose SSD EBS volume?
  a. 16TiB
  b. 2TiB
  c. 4TB
  d. 2TB
answer: a
Question: Your AWS environment contains several on-demand, EBS-backed EC2 instances dedicated to a project that has just been cancelled. Your supervisor does not want to incur charges for these on-demand instances, but also does not want to lose the data just yet because there is a chance the project may be revived in the next few days. What should you do to minimize charges for these instances in the meantime?
  a. Stop the instances as soon as possible
  b. Terminate the instances
  c. Take snapshots of the EBS volumes and sell the instances on the In-Demand Instance Marketplace.
  d. Explain your situation to AWS Support and ask them to hold your instances for you.
answer: a
Question: The AMI ID used in an AutoScaling policy is specified in the_____.
  a. Launch configuration
  b. Autoscaling group
  c. Autoscaling policy
  d. Security group
answer: a
Question: You are testing an application that uses EC2 instances to poll an SQS queue. At this stage of testing, you have verified that the EC2 instances can retrieve messages from the queue, but your coworkers are complaining about not being able to manually retrieve any messages from the queue from their on-premises workstations. What is the most likely source of this problem?
  a. SQS queues accept traffic only from within AWS.
  b. Your coworkers do not have permission to access the SQS queue.
  c. It's not possible to poll an SQS queue manually.
  d. Short polling is occasionally leaving messages behind.
answer: b
Question: You've been tasked with migrating an on-premise application architecture to AWS. During the design process, you give consideration to current on-premise security and identify the security attributes you are responsible for on AWS. Which of the following does AWS provide for you as part of the shared responsibility model?
  a. Virtualization infrastructure
  b. Physical network interface
  c. Instance security
  d. User access to the aws environment
answer: a, b
Question: You need to find both the Public and Private IP addresses of an instance. Which of the following URLs should you query?
  a. http://169.254.169.524/latest/user-data/
  b. http://169.254.169.254/latest/user-data/
  c. http://169.254.169.524/latest/meta-data/
  d. http://169.254.169.254/latest/meta-data/
answer: d
Question: Which of the following will transpire when an EC2 instance with an associated Elastic IP is stopped and started?
  a. The underlying host for the instance will be changed.
  b. All data on instance-store devices will be lost
  c. The Elastic Network Interface will be detached.
  d. The Elastic IP will be disassociated from the instance
answer: a, b
Question: What is the minimum size of an S3 object?
  a. 1 bit
  b. 1 byte
  c. 0 byte
  d. 1 KB
answer: c
Question: True or False: When a snapshot is being taken against an EBS volume, the volume becomes unavailable and the instance no longer has the ability to communicate with the EBS volume until the snapshot is complete.
  a. true
  b. false
answer: b
Question: Your company requires that all the data on your EBS-backed EC2 volumes be encrypted. How would you go about doing this?
  a. You cannot enable EBS encryption on a specific volume.
  b. AWS allows you to encrypt an EBS volume at the time of creation.
  c. Encryption is done at OS level
  d. None of the above
answer: b
Question: As CloudWatch monitors RDS, it provides which of the following metrics by default?
  a. Database-visible metrics such as the number of users
  b. Database-visible metrics such as memory usage
  c. The number of failed transaction requests
  d. The number of current connections to the database
answer: d
Question: If an instance belonging to an Elastic Load Balancer fails its health check, what will the ELB do?
  a. The ELB will de-register the instance and stop sending traffic to it.
  b. Unfortunately, the ELB will continue to send the unhealthy instance traffic until the instance is terminated.
  c. ELB will tell Auto Scaling to launch a new instance.
  d. The ELB will launch a new instance.
answer: a
Question: Elasticity is a fundamental property of the cloud. Which of the following best describes elasticity?
  a. The ability to deploy managed services into your environment.
  b. The power to increase the number of resources at your hands at the click of a mouse.
  c. The power to scale resources both up and down with changes in demand.
  d. The ability to manually deploy instances quickly in response to events.
answer: c
Question: True or False: AutoScaling is a tool used to build elastic, self-healing applications.
  a. true
  b. false
answer: a
Question: What is the Well Architected Framework?
  a. A set of questions that you can use to evaluate how well your architecture is aligned to AWS practices.
  b. A guide to passing your Solutions Architect - Associate exam.
  c. A guide to building an on-premise network compatible with AWS services.
  d. A checklist used to evaluate the availability of your applications
answer: a
Question: To protect S3 data from accidental overwrites and deletes, you should do which of the following?
  a. Allow only MFA access
  b. Use a bucket policy to disable deletes from S3
  c. Enable versioning on the bucket
  d. Acess S3 only from signed urls
answer: c
Question: You manage an application that uses EC2 instances and SQS to process requests from end users. There are no known issues with your application, but your supervisor is concerned about the cost of the AWS resources it uses. Which of the following would not help address that concern?
  a. Use AutoScaling to adjust the number of EC2 instances according to demand from SQS.
  b. Increase the visibility timeout for messages in the SQS queue.
  c. Decrease the size of SQS messages to 50KB.
  d. Switch from short polling to long polling.
answer: b
Question: You wonder why a SWF workflow you created has not made any progress in the last three weeks. What is the most likely explanation for the workflow’s behavior?
  a. The workflow has exceeded the maximum 90-day lifespan of an SWF  workflow.
  b. SWF does not support tasks located outside of AWS, so you will need to remove those tasks from your on-premise servers.
  c. SWF is awaiting human input from a task you assigned to a colleague.
  d. The last task has exceeded SWF's 14-day task execution time.
answer: c
Question: True or False: There is no cost associated with removing cached objects from a CDN Edge Location.
  a. true
  b. false
answer: b
Question: An EC2 instance retrieves a message from an SQS queue, begins processing the message, then crashes. What happens to the message?
  a. When the message visibility timeout expires, the message becomes available for processing by other EC2 instances.
  b. It remains in the queue in a locked state until the EC2 instance comes back online.
  c. When the message timeout expires, the message is duplicated, the original message is archived, and the duplicate becomes available for processing.
  d. To prevent corruption, the message is deleted.
answer: a
Question: True or False: You cannot attach more than one EC2 instance to an AWS Elastic Filesystem.
  a. true
  b. false
answer: b
Question: True or False: AutoScaling groups are not intended to handle sudden spikes in traffic. Rather, they are intended to allow your applications to grow elastically as load increases over a short period of time.
  a. true
  b. false
answer: a
Question: What is the "first-byte latency" when retrieving data from Glacier?
  a. 1 hour
  b. 2 hours
  c. 3-5 hours
  d. >5 hours
answer: c
Question: Which of the following is not a pillar of the AWS Well Architected Framework?
  a. Cost Optimization
  b. Performance Efficiency
  c. Availability
  d. Security
answer: c
Question: You've been tasked with the creation of a highly-available, decoupled web application. Which of the following will not aid in that effort?
  a. An Elastic Load Balancer that sends web traffic to instances with the least latency.
  b. An SQS queue that allows secondary EC2 instances to process jobs dropped by the primary instance.
  c. An AutoScaling group that ensures a self-healing application.
  d. IAM credentials on the primary EC2 instance that allow it to modify the SQS queue.
answer: d
Question: After migrating an application architecture from on-premise to AWS, you will not be responsible for the ongoing maintenance of which two of the following services.
  a. Elastic Beanstack
  b. EC2
  c. RDS
  d. DynamoDB
answer: c, d
Question: Your company wants to begin automated backups of the EBS volumes that back their EC2 instances. The durability of the backed-up data is key. Which of the following solutions would you implement and why?
  a. Set the lifecycle policy on the EBS Volume to back it up to Glacier
  b. Configure your Storage Gateway as "Gateway Stored" and store the backups on premise.
  c. Write a cron job that compresses the volume, and use the CLI to copy it to S3.
  d. Write a cron job that uses the AWS CLI to take a snapshot of production EBS volumes.
answer: d
Question: True or False: Data stored on EBS volumes is automatically and redundantly stored in multiple physical volumes in the same availability zone as part of the normal operations of the EBS service at no additional charge.
  a. true
  b. false
answer: a
Question: You have chosen to use S3-RRS with your cloud application. Which limitations have you considered in doing so?
  a. RRS requires supplementary Access Control Lists.
  b. RRS  is available only in the US-STANDARD region.
  c. RRS has a 4-hour data recovery time.
  d. RRS offers only 99.99% durability, so you have to design your application to re-create any objects that may be lost.
answer: d
Question: True or False: To prevent in-flight tampering, all requests sent with API keys over a REST or Query API should be sent via HTTPS.
  a. true
  b. false
answer: a
Question: Which of the following services allows you to access the service's underlying operating system?
  a. DynamoDB
  b. EMR
  c. RDS
  d. Elastic Beanstalk
answer: b, d
Question: Which of the following statements are true?
  a. S3-Standard provides 11-nines durability.
  b. S3-Standard provides 11-nines availability
  c. S3-RRS provides 99.99% durability
  d. S3-Standard provides 99.99% availability.
answer: a, c, d

</code>

