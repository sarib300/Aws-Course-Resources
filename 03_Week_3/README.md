## Week 3 — Storage, Databases & Caching

### 1. Amazon S3 Basics

Amazon S3 (Simple Storage Service) is an object storage service designed for scalability, durability, and high availability. It stores data as objects within containers called **buckets**.

S3 is commonly used for storing files, backups, application assets, and large datasets.

Example: Hosting images, videos, or static website files in an S3 bucket.

---

### 2. S3 Features

Amazon S3 provides several features to manage and protect stored data.

Key features include:

* **High durability and availability**
* **Versioning** to maintain multiple versions of an object
* **Access control** using IAM policies and bucket policies
* **Static website hosting**
* **Event notifications**

Example: Enabling versioning allows recovery of previous versions of files if they are accidentally deleted or overwritten.

---

### 3. S3 Lifecycle Policies

Lifecycle policies automate the management of objects in S3 by moving them between storage classes or deleting them after a defined period.

This helps reduce storage costs and manage data efficiently.

Example: Automatically moving files older than 30 days from standard storage to cheaper archival storage.

---

### 4. S3 Encryption

S3 supports multiple encryption methods to protect data at rest and in transit.

Common encryption types include:

* **Server-Side Encryption (SSE)** – AWS encrypts the data after it is uploaded.
* **Client-Side Encryption** – Data is encrypted before uploading to S3.
* **AWS KMS Encryption** – Uses AWS Key Management Service for secure key management.

Example: Enabling server-side encryption to protect sensitive documents stored in an S3 bucket.

---

### 5. Presigned URLs (PUT / GET)

Presigned URLs provide temporary access to private S3 objects without exposing AWS credentials.

They allow users to upload or download objects for a limited time.

* **PUT URL** – Allows users to upload files to S3.
* **GET URL** – Allows users to download files from S3.

Example: A web application generates a presigned URL allowing a user to upload a file directly to S3.

---

### 6. Amazon RDS

Amazon RDS (Relational Database Service) is a managed service for running relational databases in the cloud.

It automates database management tasks such as backups, patching, scaling, and monitoring.

Supported database engines include MySQL, PostgreSQL, and others.

Example: Running a production database for a web application without managing server infrastructure.

---

### 7. Amazon DynamoDB Basics

Amazon DynamoDB is a fully managed NoSQL database designed for high performance and scalability.

It stores data in tables using key-value and document data models.

DynamoDB is commonly used for applications requiring fast and predictable performance.

Example: Storing user session data or application metadata.

---

### 8. DynamoDB Capacity Modes

DynamoDB provides two capacity modes to manage throughput:

**Provisioned Capacity**
Users define the number of read and write operations per second. Suitable for predictable workloads.

**On-Demand Capacity**
DynamoDB automatically scales based on request traffic. Suitable for unpredictable workloads.

Example: A startup application may use on-demand capacity until traffic patterns become stable.

---

### 9. Application Connection Patterns

Applications connect to AWS storage and databases using SDKs or APIs.

Common connection patterns include:

* Direct database connections from application servers
* Serverless architectures using managed services
* Secure access using IAM roles and authentication mechanisms

Example: A backend application storing metadata in DynamoDB while files are stored in S3.

---

### 10. Caching Strategies

Caching improves application performance by storing frequently accessed data in a fast storage layer.

Common caching strategies include:

* **Read-through caching** – Application reads from cache first.
* **Write-through caching** – Data is written to cache and database simultaneously.
* **Lazy caching** – Data is cached only when requested.

Example: Frequently accessed product data stored in cache to reduce database queries.

---

### 11. Amazon ElastiCache

Amazon ElastiCache is a fully managed in-memory caching service that supports Redis and Memcached.

It improves application performance by reducing database load and decreasing latency.

Example: A high-traffic web application uses ElastiCache to store session data and frequently accessed queries.

