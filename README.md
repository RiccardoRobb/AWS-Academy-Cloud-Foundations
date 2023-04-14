# Module 1

Cloud computing is the on-demand delivery of IT resources via the internet with a *"pay-as-you-go"* pricing.

Almost enything you can implement with traditional IT can be implemented as an AWS cloud computing service.

## Cloud service models

* <mark>IaaS</mark> **"Infrastructure as a service"** \
    networking featrues, Hw or VMs and data storage space
* <mark>PaaS</mark> **"Platform as a service"** \
    no need to manage the underlying infrastructure Hw or Sw
* <mark>SaaS</mark> **"Software as a service"** \
    products that we can use (end-user applications)

## Cloud computing deployment models

* **Cloud** \
    all the parts of the application run in the cloud, can be built using low-level infrastructure pieces or higher-level services that provide abstaction from management, architecting and scaling requirements of core infrastructure

* **Hybrid** \
    allows organizations to extend and grow their infrastructure into the cloud while connecting cloud resources to internal systems
    "ususally between the cloud and existing on-premises infra"

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
To build an index we can use a simple nonrelational database like Amazon DynamoDB. \
We can run these services inside an Amazon Virtual Private Cloud (VPC).

### Services

* **EC2** , control over your AWS computing resources

* **Lambda**, run code without caring about servers maintance

* **Elastic Beanstalk**, deploy, manage and scale web applications

* **Lightsail**, lightweight cloud platform for simple web applications

* **Batch**, manage and run hundread of thousands of batch workloads

* **Outposts**, run AWS infrastructure in your On-Premises data center

* **ECS**, "elastic *container* service"

* **EKS**, "elastic *kubernetes* service"

* **Fargate**, implement a containers or *microservice* architecture

* **VMware cloud**, migrate to AWS your On-Premises server virtualization platform

### 

### Interact with AWS

* **Management console**, graphical interface prensent on AWS

* **Command line interface**, command script that can be used locally

* **SDKs**, packages to access AWS

-------------------------------

## AWS Cloud Adoption Framework

**AWS CAF** provides guidance and best practices to help organizations build a cloud computing architecture across the organization and throughout the IT lifecycle.

### Perspectives

* **Business** \
  Stakeholder from the business perspective can use the CAF to create a stong business case for cloud adoption.

* **People** \
  CAF can be used to evaluate organizational structures and roles, new skills and process requirememnts and identify gaps.

* **Governance** \
  Focus on the skills and processes that are needed to align IT strategy and goals with business strategy and goals.

* **Platform** \
  CAF includes principles and patterns for implementing new solutions on the cloud, and for migrating On-Premises workload to the cloud.

* **Security** \
  CAF allows to structure the selection and implementation of security controls that meet the organization's needs.

* **Operations** \
  Define current operationg procedures, in order to identify the process changes and training that are needed to implement successful cloud adoption.

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

Can be a good indicator to **budget** and build the bussiness case for moving to the cloud.

##### Parameters:

* **Server costs**

* **Storage costs**

* **Network costs**

* **IT labor costs**

----------------

### AWS pricing calculator

Helps you to estimate a <u>monthly</u> AWS bill, identify opportunity for cost reduction, model your solution befor building them and explore price points and calculations.

https://calculator.aws/#/



#### Cloud total cost of Ownership (<mark>CTCO</mark>)

Defines what will be spent on the technology after adoption, or what it costs to run the solution. Different from TCO, because Total cost of Ownership is used for On-Premises solutions.

##### Parameters:

* **soft saving**, reuse service or applications, increase developer productivity, *Agile* bussiness processes and increase global reach

* **hard savings**, reduce server costs, storage costs, network costs and personnel

------------------------



## AWS organizations

Is a free account management service that enables you to consolidate multiple AWS accounts into an **organization** that you create and manage.

#### Teminology

* **Organization units** (OU), are containers for accounts that can contain other OUs. We can define different <u>policies</u> for OUs or Accounts, each policy will affect all the children.



#### Organization utilities

* **Service control policies** (SCPs), allows to control AWS servicies across multiple AWS accounts, **<u>this does not replace IAM</u>**

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

* <mark>compute</mark>
  
  - **EC2**, acts as virtual machines in the cloud.
  
  - **EC2 autoscaling**, allows to create or remove EC2 instances.
  
  - **ECS**, is a powerful *container-orchestation* service that supports Docker containers.
  
  - **ECR**, is a *Docker container registry*, to easly store, manage and deploy Docker container images.
  
  - **Ekastic beanstalk**, allows to deploy ans scale web applications ans services, using *Apache* and *Microsoft IIS*.
  
  - **Lambda**, allows to *run code* without managing servers, you pay only for the compute time.
  
  - **EKS**, make it easy to deploy, manage and scale, containerized applications that use *Kubernetes*.
  
  - **Fargate**, allows to run containers (ECS) without having to manage servers or clusters.

* <mark>networking</mark>

* <mark>storage</mark>
  
  - **S3**, used for any amount of data, usally for websites, mobile apps, backup and restore, archive, enterprise applications, IoT and big data analytics
  
  - **EBS**, used for relational and non-realtional databases, containers, big data analytics engines, file systems and media workflows.
  
  - **EFS**, used to scale demand to *petabytes*, provides an *elastic network file system* (NFS) to use with AWS cloud services and On-Premises  resources.
  
  - **Simple storage service Glacier**, for archiving *long-term backups*.

* <mark>database</mark>
  
  * 
