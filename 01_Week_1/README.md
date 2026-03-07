## Week 1 — Cloud Foundations & IAM

### 1. Cloud Computing Models

Cloud computing provides on-demand computing resources over the internet. The three primary service models define how much infrastructure is managed by the provider versus the user.

**IaaS (Infrastructure as a Service)**
Provides virtualized computing resources such as servers, storage, and networking. Users manage the OS and applications.

Example: Launching a virtual server in **EC2** where you install and manage your own software.

**PaaS (Platform as a Service)**
Provides a managed platform for building and deploying applications without managing the underlying infrastructure.

Example: Deploying an application using **Elastic Beanstalk**, where AWS manages the infrastructure and runtime environment.

**SaaS (Software as a Service)**
Fully managed applications delivered over the internet. Users only interact with the software.

Example: Using **Gmail** or **Google Docs** without managing any servers or infrastructure.

---

### 2. Shared Responsibility Model

The shared responsibility model defines how security and operational responsibilities are divided between the cloud provider and the customer.

* **Cloud Provider Responsibility:** Security **of** the cloud (data centers, physical hardware, networking infrastructure).
* **Customer Responsibility:** Security **in** the cloud (applications, operating systems, configurations, and data).

Example: AWS secures the physical data centers, while the customer must configure firewall rules and manage user access.

---

### 3. AWS Global Infrastructure

AWS operates a global network of data centers designed for high availability, fault tolerance, and low latency. This infrastructure enables applications to run reliably across different geographic locations.

The main components include **Regions**, **Availability Zones**, and networking infrastructure connecting them.

Example: Deploying an application close to users in Asia to reduce latency.

---

### 4. Regions

A **Region** is a geographical area that contains multiple isolated data centers.

Each region operates independently and allows organizations to deploy applications closer to their users.

Example:

* Asia Pacific (Singapore)
* US East (N. Virginia)

Using multiple regions can improve global availability and disaster recovery.

---

### 5. Availability Zones (AZs)

Availability Zones are **separate data centers within a region** that are isolated from each other but connected through high-speed networking.

They provide fault tolerance and high availability.

Example:
Deploying application servers in **two different Availability Zones** ensures the application remains available even if one data center fails.

---

### 6. AWS Accounts & Billing Basics

An AWS account provides access to AWS services and resources. Each account has its own billing, security settings, and resource management.

Key concepts:

* **Root User:** The primary account owner with full permissions.
* **IAM Users:** Individual identities created for users within the account.
* **Billing Dashboard:** Used to monitor costs, usage, and budgets.

Example: A company may create one AWS account and add IAM users for each team member.

---

### 7. AWS Pricing Overview

AWS follows a **pay-as-you-go pricing model**, meaning users only pay for the resources they consume.

Common pricing principles:

* **Pay for usage:** No upfront infrastructure cost.
* **Pay less when you use more:** Volume-based discounts.
* **Pay less as AWS grows:** Continuous price reductions.

Example: An EC2 instance running for 10 hours is billed only for those 10 hours.

---

### 8. IAM Concepts (Identity and Access Management)

IAM is a service used to securely control access to AWS resources.

It allows administrators to define **who can access which resources and what actions they can perform**.

IAM uses users, groups, roles, and policies to manage permissions.

Example: Restricting developers so they can launch EC2 instances but cannot delete databases.

---

### 9. IAM Users

An IAM user represents an individual person or application that needs access to AWS.

Each user has unique credentials such as a password or access keys.

Example: Creating a separate IAM user account for each developer instead of sharing the root account.

---

### 10. IAM Groups

IAM groups are collections of IAM users that share the same permissions.

Permissions are assigned once to the group and automatically apply to all users in that group.

Example:
A **Developers** group may have permission to create EC2 instances, while a **Finance** group may only access billing information.

---

### 11. IAM Roles

IAM roles provide **temporary access permissions** to AWS services or users without requiring long-term credentials.

Roles are commonly used when AWS services need to interact with other AWS resources.

Example:
An EC2 instance can assume an IAM role to access an S3 bucket without storing access keys on the server.

---

### 12. IAM Policies

IAM policies are JSON documents that define permissions.

They specify:

* **Who** can access resources
* **What actions** they can perform
* **Which resources** they can access

Example: A policy allowing a user to upload files to a specific S3 bucket.

---

### 13. Principle of Least Privilege

The principle of least privilege means granting users **only the minimum permissions required to perform their tasks**.

This reduces the risk of accidental or malicious misuse of resources.

Example:
A developer who only needs to read data from an S3 bucket should be given **read-only access**, not full administrative privileges.

