## Week 2 — Compute & Networking

### 1. EC2 Basics

Amazon EC2 (Elastic Compute Cloud) provides scalable virtual servers in the cloud. It allows users to run applications on virtual machines without managing physical hardware.

Key features include on-demand scalability, flexible instance sizes, and integration with other AWS services.

Example: Hosting a web application on an EC2 instance running Linux and a web server such as Nginx or Apache.

---

### 2. EC2 Instance Types

EC2 instances come in different types optimized for specific workloads such as compute, memory, storage, or networking performance.

Common categories include:

* **General Purpose** – Balanced compute, memory, and networking.
* **Compute Optimized** – High-performance processors for compute-intensive tasks.
* **Memory Optimized** – Large memory capacity for databases.
* **Storage Optimized** – High disk throughput for large data workloads.

Example: A general-purpose instance can host a web application, while a memory-optimized instance may run a large database.

---

### 3. EC2 Lifecycle

The EC2 lifecycle refers to the different states an instance goes through during its operation.

Common states include:

* **Pending** – Instance is launching.
* **Running** – Instance is active and processing workloads.
* **Stopped** – Instance is shut down but can be restarted.
* **Terminated** – Instance is permanently deleted.

Example: A developer may stop an instance when not in use to reduce costs and start it again later.

---

### 4. Amazon Machine Images (AMI)

An Amazon Machine Image (AMI) is a template used to launch EC2 instances. It contains the operating system, application server, and preconfigured software.

AMIs allow users to quickly replicate environments.

Example: Creating an AMI from a configured server allows multiple identical EC2 instances to be launched for scaling a web application.

---

### 5. Elastic Block Store (EBS)

Amazon EBS provides persistent block-level storage for EC2 instances. The data stored on EBS volumes remains even if the instance is stopped.

EBS is commonly used for operating systems, databases, and applications requiring persistent storage.

Example: A database server running on EC2 stores its data on an EBS volume to ensure durability.

---

### 6. Elastic IPs

An Elastic IP is a static public IPv4 address designed for dynamic cloud computing.

It allows users to maintain a consistent public IP address even if the underlying EC2 instance changes.

Example: If a server fails, the Elastic IP can be quickly reassigned to another EC2 instance to restore service.

---

### 7. VPC Basics

A Virtual Private Cloud (VPC) is a logically isolated network within AWS where users can launch and manage their resources.

It allows full control over IP addressing, routing, and network configuration.

Example: An organization may create a VPC to host its web servers, databases, and application services securely.

---

### 8. Subnets (Public / Private)

Subnets divide a VPC network into smaller segments.

* **Public Subnet** – Resources in this subnet can communicate directly with the internet.
* **Private Subnet** – Resources cannot be accessed directly from the internet.

Example: A web server can be placed in a public subnet while the database server remains in a private subnet for security.

---

### 9. Route Tables

Route tables control how network traffic flows within a VPC.

They contain rules that determine where traffic should be directed based on destination IP addresses.

Example: A route table may direct internet-bound traffic from a public subnet to an internet gateway.

---

### 10. Security Groups

Security groups act as **virtual firewalls** for EC2 instances.

They control inbound and outbound traffic at the instance level using allow rules.

Key characteristics:

* Stateful firewall
* Only allow rules (no explicit deny)

Example: Allowing HTTP (port 80) traffic from the internet to a web server.

---

### 11. Network ACLs (NACL vs Security Groups)

Network Access Control Lists (NACLs) operate at the subnet level and provide an additional layer of security.

Key differences:

| Feature | Security Group | Network ACL    |
| ------- | -------------- | -------------- |
| Level   | Instance       | Subnet         |
| Rules   | Allow only     | Allow and Deny |
| State   | Stateful       | Stateless      |

Example: A NACL may block a specific IP range from accessing a subnet, while security groups control traffic to individual instances.

---

### 12. Application Load Balancer (ALB) Basics

An Application Load Balancer distributes incoming application traffic across multiple EC2 instances.

It operates at the application layer (Layer 7) and supports intelligent routing based on request content such as URL paths or hostnames.

Benefits include high availability, fault tolerance, and improved scalability.

Example: Incoming web traffic is distributed across multiple EC2 servers to ensure the application remains available during high demand.
