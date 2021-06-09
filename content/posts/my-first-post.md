---
title: "My First Post"
date: 2021-06-10T00:46:48+05:30
draft: true
---
S3 101

S3 is a Simple Storage Service that is secure, durable and highly scalable.  Static files such as images, videos, text etc can be uploaded. You can't store databases as they are always changing. Files can be from 0 bytes to 5TB and S3 offers unlimited storage. Files are stored in something called a bucket. (In simple terms, a bucket is basically a folder in the cloud)

S3 is a universal namespace, that is, names of the buckets must be unique globally. When you upload a file to S3, you will receive a HTTP 200 code if your upload was successful.

Objects consist of the following:

- Key
- Value
- VersionID
- Subresources

How does data consistency work for S3?

- Read after Write consistency for PUTS of new objects.
- Eventual consistency for overwrite PUTS and DELETES (Can take time to propagate)

In other words, If you write a new file & read it immediately afterwards, you will be able to view that data.

If you update an existing file or delete a file & read it immediately, you may get the older version or you may not. Basically changes to the objects can take a while to propagate.

S3 has the following features:

- Tiered storage available
- Lifecycle management
- Versioning
- Encryption
- Secure your data using access control lists & bucket policies.

S3 Storage Classes

- S3 Standard
    - 99.99% availability
    - 99.999999999% durability
    - Designed to sustain the loss of 2 facilities concurrently
- S3 IA
    - Infrequently accessed
    - For data that is accessed less frequently but required rapid access when needed
    - Lower fee than S3, but charged a retrieval fee
- S3 Onezone IA
    - Used when we don't need in multiple availability zones.
    - Similar to S3 IA except with respect to the availability zones
- S3 Intelligent Tiering
    - Uses machine language.
    - Designated to minimise costs by automatically moving data to the most cost effective access tier without performance impact or operational overhead.
- S3 Glacier
    - Secure, durable, low cost for data archiving.
    - Usually cheaper than on-premise solutions
    - Retrieval times configurable from minutes to hours
- S3 Glacier Deep Archive
    - Lowest cost storage class
    - Retrieval time of 12 hour
- S3 Outposts
    - Has been introduced as a storage class to deliver object storage to on-premises AWS outpost environments

You are charged in the following ways:

- Storage
- Requests
- Storage management pricing
- Data transfer pricing
- Transfer acceleration
- Cross region replication pricing

Transfer acceleration enables fast, easy, secure transfer of your files over long distances between your end users & an S3 bucket.
Cross Region Replication is a feature that replicates the data from one bucket to another bucket which could be in a different region.

Hope you found this article useful! Thank you!
