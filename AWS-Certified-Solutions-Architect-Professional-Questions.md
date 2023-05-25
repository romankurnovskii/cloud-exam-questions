<div align="center">
  <img height="128" src="https://d1.awsstatic.com/training-and-certification/certification-badges/AWS-Certified-Solutions-Architect-Professional_badge.69d82ff1b2861e1089539ebba906c70b011b928a.png"> 
  <h1>AWS Certified Solutions Architect Professional Practice Questions - SAP-C02</h1>
  <span>This is a list of AWS Certified Solutions Architect Professional questions and their answers ✨
  
  <a href="https://aws.amazon.com/certification/certified-solutions-architect-professional/">Exam Info</a> | <a href="http://www.cloud-exam-prepare.com/">Quizz App</a>
</div>

---

#### 1. A company has many AWS accounts that individual business groups own. One of the accounts was recently compromised. The attacker launched a large number of instances, resulting in a high bill for that account.

#### The company addressed the security breach, but a solutions architect needs to develop a solution to prevent excessive spending in all accounts. Each business group wants to retain full control of its AWS account.

#### Which solution should the solutions architect recommend to meet these requirements?

1. Use AWS Organizations. Add each AWS account to the management account. Create an SCP that uses the `ec2:instanceType` condition key to prevent the launch of high-cost instance types in each account.
1. Attach a new customer-managed IAM policy to an IAM group in each account. Configure the policy to use the `ec2:instanceType` condition key to prevent the launch of high-cost instance types. Place all the existing IAM users in each group.
1. Turn on billing alerts for each AWS account. Create Amazon CloudWatch alarms that send an Amazon Simple Notification Service (Amazon SNS) notification to the account administrator whenever the account exceeds a designated spending threshold.
1. Turn on AWS Cost Explorer in each account. Review the Cost Explorer reports for each account on a regular basis to ensure that spending does not exceed the desired amount.

<details><summary><b>Answer</b></summary>
<p>

#### Answer 3

[Billing alarms](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/monitor_estimated_charges_with_cloudwatch.html) will provide the company with alerts about excessive spending without taking away control from any of the business groups. Options A and B are incorrect because each business group wants to retain control of its account. These options would not prevent the launch of a large number of instances. Option D is a manual process that would not provide immediate alerts about excessive spending.

</p>
</details>


---

#### 2. A company has multiple AWS accounts in an organization in AWS Organizations. The company has integrated its on-premises Active Directory with AWS Single Sign-On (AWS SSO) to grant Active Directory users least privilege permissions to manage infrastructure across all the accounts.

#### A solutions architect must integrate a third-party monitoring solution that requires read-only access across all AWS accounts. The monitoring solution will run in its own AWS account.

#### What should the solutions architect do to provide the monitoring solution with the required permissions?

1. Create a user in an AWS SSO directory. Assign a read-only permissions set to the user. Assign all AWS accounts that need monitoring to the user. Provide the third-party monitoring solution with the user name and password.
1. Create an IAM role in the organization's management account. Allow the AWS account of the third-party monitoring solution to assume the role.
1. Invite the AWS account of the third-party monitoring solution to join the organization. Enable all features.
1. Create an AWS CloudFormation template that defines a new IAM role for the third-party monitoring solution. Specify the AWS account of the third-party monitoring solution in the trust policy. Create the IAM role across all linked AWS accounts by using a stack set.

<details><summary><b>Answer</b></summary>
<p>

#### Answer 4

[AWS CloudFormation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/what-is-cfnstacksets.html) [StackSets](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/what-is-cfnstacksets.html) can deploy the IAM role across multiple accounts with a single operation. Option A is incorrect because credentials that are supplied by AWS Single Sign-On (AWS SSO) are temporary. The application would lose permissions and would have to log in again. Option B would grant access to the management account only. Option C is incorrect because when an account joins an organization, the account does not receive permissions to access the other accounts in the organization.

</p>
</details>


---
#### 3.  Your company policies require encryption of sensitive data at rest. You are considering the possible options for protecting data while storing it at rest on an EBS data volume, attached to an EC2 instance.
#### Which of these options would allow you to encrypt your data at rest? (Choose three.)


1. Implement third party volume encryption tools
1. Implement SSL/TLS for all services running on the server
1. Encrypt data inside your applications before storing it on EBS
1. Encrypt data using native data encryption drivers at the file system level
1. Do nothing as EBS volumes are encrypted by default

<details><summary><b>Answer</b></summary>
<p>

#### Answer 1 3 4

</p>
</details>


---
#### 4. A customer is deploying an SSL enabled web application to AWS and would like to implement a separation of roles between the EC2 service administrators that are entitled to login to instances as well as making API calls and the security officers who will maintain and have exclusive access to the application's X.509 certificate that contains the private key.

1. Upload the certificate on an S3 bucket owned by the security officers and accessible only by EC2 Role of the web servers.
1. Configure the web servers to retrieve the certificate upon boot from an CloudHSM is managed by the security officers.
1. Configure system permissions on the web servers to restrict access to the certificate only to the authority security officers.
1. Configure IAM policies authorizing access to the certificate store only to the security officers and terminate SSL on an ELB.

<details><summary><b>Answer</b></summary>
<p>

#### Answer 4

</p>
</details>


---
#### 5. A company has an application behind a load balancer with enough Amazon EC2 instances to satisfy peak demand. Scripts and third-party deployment solutions are used to configure EC2 instances when demand increases or an instance fails. The team must periodically evaluate the utilization of the instance types to ensure that the correct sizes are deployed.
#### How can this workload be optimized to meet these requirements?

1. Use CloudFormer to create AWS CloudFormation stacks from the current resources. Deploy that stack by using AWS CloudFormation in the same region. Use Amazon CloudWatch alarms to send notifications about underutilized resources to provide cost-savings suggestions.
1. Create an Auto Scaling group to scale the instances, and use AWS CodeDeploy to perform the configuration. Change from a load balancer to an Application Load Balancer. Purchase a third-party product that provides suggestions for cost savings on AWS resources.
1. Deploy the application by using AWS Elastic Beanstalk with default options. Register for an AWS Support Developer plan. Review the instance usage for the application by using Amazon CloudWatch, and identify less expensive instances that can handle the load. Hold monthly meetings to review new instance types and determine whether Reserved Instances should be purchased.
1. Deploy the application as a Docker image by using Amazon ECS. Set up Amazon EC2 Auto Scaling and Amazon ECS scaling. Register for AWS Business Support and use Trusted Advisor checks to provide suggestions on cost savings.

<details><summary><b>Answer</b></summary>
<p>

#### Answer 4

</p>
</details>


---

## Resources

- [examtopics](https://www.examtopics.com/exams/amazon/aws-certified-solutions-architect-professional/view/)
- [Sample questions .pdf](https://d1.awsstatic.com/training-and-certification/docs-sa-pro/AWS-Certified-Solutions-Architect-Professional_Sample-Questions.pdf)
