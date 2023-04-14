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

* AWS security groups, network ACLs, AWS identity and IAM <-> firewalls, ACLs and administrators
* Elastic load balancing, Amazon VPC <-> routers, network pipelines and switches
* AMIs and Amazon EC2 <-> On-Premises servers
* Amazon EBS, Amazon EFS, Amazon S3 and Amazon RDS <-> DAS, SAN, NAS and RDBMS  

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
