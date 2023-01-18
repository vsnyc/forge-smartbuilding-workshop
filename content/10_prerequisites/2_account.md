+++
title = "2. Create an AWS account"
chapter = false
weight = 2
+++

{{% notice tip %}}
<p><strong>
If you are doing this as part of a workshop using the Event Engine, you can skip this page. We will be providing an AWS account for you to use.
</strong></p>
{{% /notice %}}

{{% notice tip %}}
<p>
If you already have an AWS account, and have IAM Administrator access, you can skip this page.
</p>
{{% /notice %}}

{{% notice warning %}}
<p>
Your account must have the ability to create new IAM roles and scope other IAM permissions.
</p>
{{% /notice %}}

1. **If you don't already have an AWS account with Administrator access**: [create
one now](https://aws.amazon.com/getting-started/)

2. Once you have an AWS account, ensure you are following the remaining workshop steps
as an **IAM user** with administrator access to the AWS account:
[Create a new IAM user to use for the workshop](https://console.aws.amazon.com/iam/home?region=us-east-1#/users$new)

3. Enter the user details:
![Create User]({{< resource url="images/iam-1-create-user.png" >}})

4. Attach the AdministratorAccess IAM Policy:
![Attach Policy]({{< resource url="images/iam-2-attach-policy.png" >}})

5. Click to create the new user:
![Confirm User]({{< resource url="images/iam-3-create-user.png" >}})

6. Take note of the login URL and save:
![Login URL]({{< resource url="images/iam-4-save-url.png" >}})

