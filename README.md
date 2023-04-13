# Module 1
Cloud computing is the on-demand delivery of IT resources via the internet with a "pay-as-you-go" pricing. \
Almost enything you can implement with traditional IT can be implemented as an AWS cloud computing service.

## Cloud service models
* "Infrastructure as a service" IaaS \
	networking featrues, Hw or VMs and data storage space
* "Platform as a service" PaaS \
	no need to manage the underlying infrastructure Hw or Sw
* "Software as a service" SaaS \
	products that we can use (end-user applications)

## Cloud computing deployment models
* Cloud \
	all the parts of the application run in the cloud, can be built using low-level infrastructure pieces or higher-level services that provide abstaction from management, architecting and scaling requirements of core infrastructure
* Hybrid \
	allows organizations to extend and grow their infrastructure into the cloud while connecting cloud resources to internal systems
	"ususally between the cloud and existing on-premises infra"
* On-Premises \
	"private cloud", provides dedicated resources using virtualization ans resource management tools

### Similarities between AWS and traditional IT
* AWS security groups, network ACLs, AWS identity and IAM <-> firewalls, ACLs and administrators
* Elastic load balancing, Amazon VPC <-> routers, network pipelines and switches
* AMIs and Amazon EC2 <-> On-Premises servers
* Amazon EBS, Amazon EFS, Amazon S3 and Amazon RDS <-> DAS, SAN, NAS and RDBMS  
 
-------------------------------------------

## What's AWS?
AWS is a "secure cloud platform" that offers a broad set of global cloud-based products, offers flexibility, provides on-demand access to many IT resources and management tools.

### Simple example of a database application
Costumers send data to Amazon EC2 instances. \
EC2 servers batch the data and add an object per costumer to Amazon S3. \
To build an index we can use a simple nonrelational database like Amazon DynamoDB. \
We can run these services inside an Amazon Virtual Private Cloud (VPC).
