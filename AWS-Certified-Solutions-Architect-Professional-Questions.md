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

### Answer 3

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

### Answer 4

[AWS CloudFormation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/what-is-cfnstacksets.html) [StackSets](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/what-is-cfnstacksets.html) can deploy the IAM role across multiple accounts with a single operation. Option A is incorrect because credentials that are supplied by AWS Single Sign-On (AWS SSO) are temporary. The application would lose permissions and would have to log in again. Option B would grant access to the management account only. Option C is incorrect because when an account joins an organization, the account does not receive permissions to access the other accounts in the organization.

</p>
</details>











---

- [Sample questions .pdf](https://d1.awsstatic.com/training-and-certification/docs-sa-pro/AWS-Certified-Solutions-Architect-Professional_Sample-Questions.pdf)