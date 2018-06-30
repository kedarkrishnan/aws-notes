# EC2

- on Demand
	- low cost and flexibility
	- pay by hour or by sec
	- applications with short term spikes, unpredictated workloads
	- application developed or tested on Amazon EC2 for first time

- Reserved Instances
	- offers significant discount on the hourly charge
	- contact 1 or 3 years
	- application with steady state or predicated usage
	- application that require reserved capacity
	
- Spot Instances
	- enables you to bid
		- Say you bid for 100 and price goes to 90 you are provisioned instances then the prices go back up to 150 the instances are terminated
		- if AWS terminated - you will not be charged for partial hour of usage
		- if you terminate it, you will be charged for full hour
	- flexible start and end time
	- users with urgent needs for large amount of addtional capacity

- Dedicated hosts
	- regulatory requirement
	- physical EC2 servers
	- licensing which does not support multi-tenancy 

	
### EBS - Elastic block storage 
-	Disk in cloud which is attached to EC2 instances
	
- EBS Volumne types
	- General purpose SSD (GP2)
		- 3 to 10,000 IOPS
	- Provisioned IOPS SSD (101)
		- more than 10,000 IOPS
		- I/O intensive apps RDBMS or NoSQL Db			
	- Magnetic
		- Throughput Optimized HDD (ST1)
			- Cannot be a boot volume
			- Sequential writes
			- Big data, data warehouse, log processing
		- Cold HDD (SC1)
			- lowest price, infrequent accessed workloads
			- File serverce 
			- Cannot be boot volume
		- Magnetic (Standard)
			- Legacy
			- lowest cost bootable volume	
- You cannot mount 1 EBS volume to multiple EC2 instances use EFS 
			
`Ec2 Instance Types: FIGHT DR MC PX`

- Termination protection is turned off by default
- on EBS-backed instances default action is for the root EBS volume to be deleted when instance is terminated
- EBS root volume 
	- Default AMI cannot be enrypted
	- You can use third party tools for encryption or can encrypt when creating a copy of AMI
- Additional volume can be encrypted			
