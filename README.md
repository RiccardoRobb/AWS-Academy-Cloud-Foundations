# Module 1

Cloud computing is the on-demand delivery of IT resources via the internet with a *"pay-as-you-go"* pricing.

Almost anything you can implement with traditional IT can be implemented as an AWS cloud computing service.

## Cloud service models

* <mark>IaaS</mark> **"Infrastructure as a service"** \
    networking features, Hw or VMs and data storage space
* <mark>PaaS</mark> **"Platform as a service"** \
    no need to manage the underlying infrastructure Hw or Sw
* <mark>SaaS</mark> **"Software as a service"** \
    products that we can use (end-user applications)

## Cloud computing deployment models

* **Cloud** \
    all the parts of the application run in the cloud, can be built using low-level infrastructure pieces or higher-level services that provide abstraction from management, architecting and scaling requirements of core infrastructure

* **Hybrid** \
    allows organizations to extend and grow their infrastructure into the cloud while connecting cloud resources to internal systems
    "usually between the cloud and existing on-premises infra"

* **On-Premises** \
    "private cloud", provides dedicated resources using virtualization ans resource management tools

---------------------------------

#### Similarities between AWS and traditional IT

* AWS security groups, network ACLs, AWS identity and IAM >< firewalls, ACLs and administrators
* Elastic load balancing, Amazon VPC >< routers, network pipelines and switches
* AMIs and Amazon EC2 >< On-Premises servers
* Amazon EBS, Amazon EFS, Amazon S3 and Amazon RDS >< DAS, SAN, NAS and RDBMS  

-------------------------------------------

## What's AWS?

**AWS** is a "secure cloud platform" that offers a broad set of global cloud-based products, offers <u>flexibility</u>, provides <u>on-demand access to many IT resources</u> and <u>management tools</u>.

### Simple example of a database application

Costumers send data to Amazon EC2 instances. \
EC2 servers batch the data and add an object per costumer to Amazon S3.  \
To build an index we can use a simple non-relational database like Amazon DynamoDB. \
We can run these services inside an Amazon Virtual Private Cloud (VPC).

### Services

* **EC2** , control over your AWS computing resources

* **Lambda**, run code without caring about servers maintenance

* **Elastic Beanstalk**, deploy, manage and scale web applications

* **Lightsail**, lightweight cloud platform for simple web applications

* **Batch**, manage and run hundred of thousands of batch workloads

* **Outposts**, run AWS infrastructure in your On-Premises data center

* **ECS**, "elastic *container* service"

* **EKS**, "elastic *kubernetes* service"

* **Fargate**, implement a containers or *microservice* architecture

* **VMware cloud**, migrate to AWS your On-Premises server virtualization platform

### 

### Interact with AWS

* **Management console**, graphical interface present on AWS

* **Command line interface**, command script that can be used locally

* **SDKs**, packages to access AWS

-------------------------------

## AWS Cloud Adoption Framework

**AWS CAF** provides guidance and best practices to help organizations build a cloud computing architecture across the organization and throughout the IT lifecycle.

### Perspectives

* **Business** \
  Stakeholder from the business perspective can use the CAF to create a strong business case for cloud adoption.

* **People** \
  CAF can be used to evaluate organizational structures and roles, new skills and process requirements and identify gaps.

* **Governance** \
  Focus on the skills and processes that are needed to align IT strategy and goals with business strategy and goals.

* **Platform** \
  CAF includes principles and patterns for implementing new solutions on the cloud, and for migrating On-Premises workload to the cloud.

* **Security** \
  CAF allows to structure the selection and implementation of security controls that meet the organization's needs.

* **Operations** \
  Define current operation procedures, in order to identify the process changes and training that are needed to implement successful cloud adoption.

-----------------------

--------------------

# Module 2

Pay only for the services that you consume, there are many ways to pay less, you can use **Reserved Instances** (bundle-like): *AURI, PURI and NURI*.

There are also many "Volume-based" discounts, based on the usage increase.
For example S3 pricing is tiered, so you pay less per GB when you use more.

There are 3 fundamental drivers of cost with AWS:

* **compute** charged per hr/sec, varies by instance type

* **storage** charged per GB

* **data transfer** charged per GB

----------------

#### AWS Free tier

[Free AWS cloud services](https://aws.amazon.com/it/free/?all-free-tier.sort-by=item.additionalFields.SortRank&all-free-tier.sort-order=asc&awsf.Free%20Tier%20Types=*all&awsf.Free%20Tier%20Categories=*all)

-----------------

### Services with no charge

* **VPC**

* **IAM**

* **Automatic scaling**

* **Elastic beanstalk**

* **CloudFormation**

* **OpsWorks**

-----------------

### On-Premises Vs Cloud

The difference between these two is how they are deployed.

- *On-Premises* infrastructure is installed <u>_locally_</u> on a company's own computer and servers.
  
  * **fixed costs / capital expenses** like facilities, hardware, licenses and maintenance
  
  * **difficult to scale**
* *Cloud* infrastructure is purchased from a service provide, so there are <u>no capital expenses</u>  and there are costs only for new tools or upgrade (scaling).

#### Total cost of Ownership (<mark>TCO</mark>)

Is the financial estimate to help identify *direct* and *indirect* costs of a system.

It's useful to **compare** the costs of running an entire infrastructure environment or specific workload on AWS or using an On-Premises solution.

Can be a good indicator to **budget** and build the business case for moving to the cloud.

##### Parameters:

* **Server costs**

* **Storage costs**

* **Network costs**

* **IT labor costs**

----------------

### AWS pricing calculator

Helps you to estimate a <u>monthly</u> AWS bill, identify opportunity for cost reduction, model your solution before building them and explore price points and calculations.

https://calculator.aws/#/

#### Cloud total cost of Ownership (<mark>CTCO</mark>)

Defines what will be spent on the technology after adoption, or what it costs to run the solution. Different from TCO, because Total cost of Ownership is used for On-Premises solutions.

##### Parameters:

* **soft saving**, reuse service or applications, increase developer productivity, *Agile* business processes and increase global reach

* **hard savings**, reduce server costs, storage costs, network costs and personnel

------------------------

## AWS organizations

Is a free account management service that enables you to consolidate multiple AWS accounts into an **organization** that you create and manage.

#### Teminology

* **Organization units** (OU), are containers for accounts that can contain other OUs. We can define different <u>policies</u> for OUs or Accounts, each policy will affect all the children.

#### Organization utilities

* **Service control policies** (SCPs), allows to control AWS services across multiple AWS accounts, **<u>this does not replace IAM</u>**

* **Account groups**, OUs

* **Single payment system**, we can pay a single bill for all the accounts

* **API** to manage and control accounts

You can see more about "Setup an organization" and "IAM simulator" [here](https://docs.aws.amazon.com/IAM/latest/UserGuide/access_policies_testing-policies.html)

------

-----

# Module 3

AWS Cloud infrastructure is built around **Regions**, there are 22 regions worldwide. An AWS Region is a physical geographical location with one or more *Availability zone* (data centers).

A business can replicate data across Regions, this decision is based on data governance and legal requirements. It is important to consider the **latency**, you can use [this](https://www.cloudping.info/).

## AWS foundational services

* <mark>**compute**</mark>
  
  - **EC2**, acts as virtual machines in the cloud.
  
  - **EC2 autoscaling**, allows to create or remove EC2 instances.
  
  - **ECS**, is a powerful *container-orchestation* service that supports Docker containers.
  
  - **ECR**, is a *Docker container registry*, to easily store, manage and deploy Docker container images.
  
  - **Ekastic beanstalk**, allows to deploy ans scale web applications ans services, using *Apache* and *Microsoft IIS*.
  
  - **Lambda**, allows to *run code* without managing servers, you pay only for the compute time.
  
  - **EKS**, make it easy to deploy, manage and scale, containerized applications that use *Kubernetes*.
  
  - **Fargate**, allows to run containers (ECS) without having to manage servers or clusters.

* <mark>**networking**</mark>
  
  * **VPC**, enables you to provision logically isolated sections of the AWS Cloud.
  
  * **Elastic load balancing**, distribuites incoming application traffic across multiple targets.
  
  * **CloudFront**, is a fast *content delivery service* (CDN).
  
  * **Transit gateway**, allow to connect *VPCs with On-Premises networks*.
  
  * **Route 53**, is a *DNS* service.
  
  * **Direct connect**, allows to create a *dedicated private network connection* from your data center to AWS.
  
  * **VPN** from your network or device to the AWS global network. 

* **<mark>security, identity and compliance</mark>**
  
  * **IAM**, manages access to AWS services and resources securely, allows to *create and manage AWS users and groups*.
  
  * **Organizations**, restricts what services and actions are allowed in your accounts.
  
  * **Cognito**, *add sign-up sign-in* to your mobile or web applications.
  
  * **Artifact**, provides an on-demand access to AWS security and compliance reports.
  
  * **KMS**, create and manage keys. *Encryption* across AWS services.
  
  * **Shield**, is a managed *DDoS protection* for applications on AWS.

* <mark>**storage**</mark>
  
  - **S3**, used for any amount of data, usually for websites, mobile apps, backup and restore, archive, enterprise applications, IoT and big data analytics
  
  - **EBS**, used for relational and non-relational databases, containers, big data analytics engines, file systems and media workflows.
  
  - **EFS**, used to scale demand to *petabytes*, provides an *elastic network file system* (NFS) to use with AWS cloud services and On-Premises  resources.
  
  - **Simple storage service Glacier**, for archiving *long-term backups*.

* <mark>**database**</mark>
  
  * **RDS**, allows to create, operate and scale *relational databases*.
  
  * **Aurora**, is a *MySQL* and *PostgreQL* compatible relational database (more efficient and speedy).
  
  * **Redshift**, allows to run *analytic queries on petabytes of data* in Redshift, against *exabityes of data* on S3.
  
  * **DynamoDB**, is a *key-value* and *document* database, with backup and restore, and in-memory caching.

-----------------

----------------

# Module 4

### Service characteristics and security responsibility

Every service intended as **IaaS**, for example *EC2*, *<u>require the customer to perform all the necessary security configuration and management tasks</u>*. For every **PaaS** instead it is not required.

For best practices for running a *Oracle Database* see [this](https://docs.aws.amazon.com/whitepapers/latest/oracle-database-aws-best-practices/oracle-database-aws-best-practice.html).

In short we can say that AWS is responsible for security **of** the cloud, instead the user is responsible for the security **in** the cloud.

## AWS Identity and Access management (<mark>IAM</mark>)

Allows you to control access to compute, storage, database, and application services in the AWS Cloud. IAM can be used to *handle authentication*, and to specify or enforce *authorization policies*, in order to specify which user can access which service.

**Best practice:** <u>follow the principle of least privilege</u>

#### Fine-grained access rights

- **who** can access the resource

- **which** resource can be accessed and what can the user do whit it

- **how** resources can be accessed

#### Components

* **user**, person or application that can authenticate with an AWS account

* **group**, a collection of IAM users that are granted identical authorization

* **policy**, a document that defines *which resource can be accessed + level od access*

* **role**, mechanism to grant a set of permissions

#### Authenticate as a IAM user to gain access

When we define an IAM user, we define also the *types of access*.

A user can access using **Programmatic access** (API) using <u>access key ID</u> and <u>secret access key</u>. Or can access using a "login page" called **Management console access** using <u>12-digit account ID / alias</u> and <u>IAM username + IAM password</u>.

We can also add **IAM MFA** to increase the security.

#### Policies

* **Identity-based**, attach a policy to any IAM entity (user/group/role), listing all the actions an entity can or cannot perform; a single policy can be attached to multiple entities and every entity can have multiple policies.

* **Resource-based**, attached to a resource, for example S3 bucket.

You can access the IAM Policy simulator [here](https://policysim.aws.amazon.com/).

#### Securing a new AWS account

The ROOT account used to create and manage all the services used in AWS cannot be limited by policies, so we need to secure it in different ways. To secure the account, we must use it all if <u>strictly necessary</u>, allow the <u>MFA</u> for the account, activate <u>CloudTrail</u> to track user activity and keep an eye on the <u>billing reports</u>.

--------------

## AWS compliance programs

Provide information about the policies, processes and controls that are established and operand by AWS. We can use tools like **AWS config** to assess, audit and evaluate the configurations of AWS; also **AWS artifact** can be used to see security and compliance reports.

-------------------------------

---------------

# Module 5

## Networking basics

A computer network is composed by two or more clients machines that are connected together, can be logically partitioned into *subnets*.

Each machine in a network has a unique IP address, that can be *32-bit* long **IPv4** of *128-bit* long **IPv6**

#### Classless Inter-Domain routing (CIDR)

A CIDR address is composed by:

* **IP** address

* **/** "slash character"

* **number**, tells you how many bits of the routing prefix must be fixed or allocated for the network identifier

Is a way to express a group of IP addresses that are consecutive to each other. There are two special types:

* *Fixed IP addresses*, for example `192.0.2.0/32` represents a single IP address, this can be useful when you want to set up a firewall rule

* *The internet*, in which every byte is flexible `0.0.0.0/0`

#### Open System interconnection model (OSI)

Is a conceptual model used to explain <u>how data travels</u> over a network.

| Layer        | #   | Function                                                            | Protocol/Address         |
| ------------ | --- | ------------------------------------------------------------------- | ------------------------ |
| Application  | 7   | Means for an application to access a computer network               | HTTP(S), FTP, DHCP, LDAP |
| Presentation | 6   | Ensures that the application layer can read the data and Encryption | ASCI, ICA                |
| Session      | 5   | Enables orderly exchange of data                                    | NetBIOS, RPC             |
| Transport    | 4   | Protocols to support host-to-host communication                     | TCP, UDP                 |
| Network      | 3   | Routing and packet forwarding (routers)                             | IP                       |
| Data link    | 2   | Transfer data in the same LAN network                               | MAC                      |
| Physical     | 1   | Transmission and reception of raw bitstreams                        | Signals                  |

-------------------

## Amazon Virtual private cloud (<mark>VPC</mark>)

Lets you provision a logically isolated section of the AWS Cloud where you can launch your AWS resources. 

* Selection of *IP address range*

* Creation of *subnets*

* Configuration of *route tables* and *network gateways*

#### VPCs

Every VPC is *logically isolated* from other VPCs, it is dedicated to your AWS account and belongs to a single AWS Region and can span across multiple Availability Zones



#### Subnets

*Range of IP addresses* that divide a VPC, belong to a single Availability Zone and can be *public* or *private*



#### IP addressing

When you create a VPC, you assign it to an **IPv4 CIDR block** (<u>range of private IPv4</u> addresses), this range cannot be changed. Every CIDR block can have a **max** size of `/16` and a **min** size of `/28`. CIDR blocks of subnets cannot overlap.

Use this [reference](https://docs.aws.amazon.com/vpc/latest/userguide/what-is-amazon-vpc.html).

* **reserved IP addresses**, for every CIDR block created, AWS reserves:
  
  * `x.x.x.0` network address
  
  * `x.x.x.1` internal communication
  
  * `x.x.x.2` DNS resolution
  
  * `x.x.x.3`  Future use
  
  * `x.x.x.255` network broadcast address

* **Elastic IP address**
  
  Every Elastic IP address is associated with an AWS account, can be *allocated* and *remapped* anytime.
  
  Use this [reference](https://docs.aws.amazon.com/vpc/latest/userguide/vpc-eips.html).

* **public IP address**
  
  Can be *manually assigned* through an Elastic IP address or *automatically* assigned through the auto-assign public IP address settings at the subnet level.



### Elastic network interface

Is a *virtual network interface* that you can **attach** to an instance to redirect network traffic to it and **detach** it. Each instance in your VPC has a default network interface that is assigned a private IPv4 address from the IPv4 address range of your VPC.

Use this [reference](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-eni.html).



#### Route tables and routes

A route table contains a set of rules/routes that you can configure to direct network traffic from your subnet. Each rout specifies a destination and a target, by default every route table contains a *local route* for communication within the VPC. Each subnet must be associated with a route table (at most one).

Use this [reference](https://docs.aws.amazon.com/vpc/latest/userguide/VPC_Route_Tables.html).

--------------

#### Internet gateway

Is a scalable, redundant and highly available VPC components that allows communication between instances in your VPC and the internet. Allows to **provide a target** in yout VPC route table for internet-routable traffic and to perform **network address translation** for instances that were assigned IPv4 addresses.

Use this [reference](https://docs.aws.amazon.com/vpc/latest/userguide/VPC_Internet_Gateway.html).

### Network address translation (NAT) gateway

Enables instances in a private subnet to connect to the internet or other AWS services, but prevents the internet from initiating a connection with those instances. To create a NAT gateway, you must specify the *public subnet* in which the NAT gateway should reside. You must also specify an Elastic IP address to associate with the NAT gateway, after you must update the route table that is associated with one or more of your private subnets to point inter-bound traffic to the NAT gateway.

* NAT [gateways](https://docs.aws.amazon.com/vpc/latest/userguide/vpc-nat-gateway.html)

* NAT [instances](https://docs.aws.amazon.com/vpc/latest/userguide/VPC_NAT_Instance.html)

-----

## VPC sharing

The account that owns the VPC **(owner)** shares one or more subnets with other accounts **(participants)** that belong to the same organization, the participants can *view*, *create*, *modify* and *delete* their application resources in the subnets that are shared with them.

Pros:

* Separation of duties

* Security groups

## VPC peering

Is a networking connection between two VPCs that enables you to route traffic between them privately. Instances in either VPC <u>can communicate</u> with each other as if they are within the <u>same network</u>.

Restrictions:

* IP address ranges **cannot overlap**

* **transitive peering is not supported**

* **only one** peering resource between the same two VPCs

Use this for [reference](https://docs.aws.amazon.com/vpc/latest/userguide/vpc-peering.html).

--------

### AWS Site-to-Site VPN

By default, <u>instances that you launch into a VPC cannot communicate with remote network</u>.

To connect your VPC to your remote network we need to create a [VPN connection](https://docs.aws.amazon.com/vpc/latest/userguide/vpn-connections.html).

### AWS Direct connect

AWS offers this service to establish a dedicated, private network connection between your network and one of the [AWS Direct connect](https://aws.amazon.com/directconnect/) locations, so that we can reduce network costs, increase bandwidth throughput and provide a more consistent network experience than internet-based connections. 

This can be useful if your data center is located far away from your AWS Region.

### AWS Transit Gateway

For On-Premises connectivity you must attach your VPN to each individual VPC, this can be really hard and slow for many machines.

Using the transit gateqay we only need to *create* and *manage* a single connection from the central gateway into each VPC.

----

## VPC endpoints

Is a *virtual device* that enables you to privately connect your VPC to supported AWS services and VPC endpoint services that are powered by AWS PrivateLink.

* **interface VPC endpoint**, enables you to connect to services that are powered by [AWS PrivateLink](https://docs.aws.amazon.com/vpc/latest/privatelink/create-interface-endpoint.html)

* **gateway endpoint**

## VPC security

### Security group

Acts as a *virtual firewall* for your instance, and it controls **inbound** and **outbound** traffic.  ~"filter for traffic to your instances"~ 
