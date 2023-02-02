<div align="center">
  <img height="128" src="https://d1.awsstatic.com/training-and-certification/certification-badges/AWS-Certified-Cloud-Practitioner_badge.634f8a21af2e0e956ed8905a72366146ba22b74c.png"> 
  <h1>AWS Certified Cloud Practitioner Practice Questions</h1>
  <span>This is a list of AWS Certified Cloud Practitioner questions and their answers ✨
  
  <a href="https://aws.amazon.com/certification/certified-cloud-practitioner/">Exam Info</a> | <a href="http://www.cloud-exam-prepare.com/">Quizz App</a>
</div>

---

#### 1. Which AWS Route 53 routing policy would you use to route traffic to multiple resources and also choose how much traffic is routed to each resource?

1. Weighted routing policy
2. Latency routing policy
3. Failover routing policy
4. Simple routing policy

<details><summary><b>Answer</b></summary>
<p>

#### Answer 1

Knowledge Area: https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/routing-policy.html

Weighted routing lets you associate multiple resources with a single domain name (example.com) or subdomain name (acme.example.com) and choose how much traffic is routed to each resource. This can be useful for a variety of purposes, including load balancing and testing new versions of software. To configure weighted routing, you create records that have the same name and type for each of your resources. You assign each record a relative weight that corresponds with how much traffic you want to send to each resource. Amazon Route 53 sends traffic to a resource based on the weight that you assign to the record as a proportion of the total weight for all records in the group.

</p>
</details>


---

#### 2. A data analytics company is running a proprietary batch analytics application on AWS and wants to use a storage service which would be accessed by hundreds of EC2 instances simultaneously to append data to existing files. As a Cloud Practitioner, which AWS service would you suggest for this use-case?

1. EFS
2. EBS
3. S3
4. Instance Store

details><summary><b>Answer</b></summary>
<p>

#### Answer 1

Knowledge Area: https://aws.amazon.com/efs/

"EFS" - Amazon EFS is a file storage service for use with Amazon EC2. Amazon EFS provides a file system interface, file system access semantics, and concurrently-accessible storage for up to thousands of Amazon EC2 instances. Amazon EFS uses the Network File System protocol.

</p>
</details>