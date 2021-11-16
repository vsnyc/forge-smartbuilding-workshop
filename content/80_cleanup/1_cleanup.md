+++
title = "Cleanup"
chapter = false
weight = 1
+++

{{% notice tip %}}
<p><strong>
If you are doing this as part of a workshop using the Event Engine, you can skip this page.
</strong></p>
{{% /notice %}}

### Clean up steps

{{% notice warning %}}
<p>
The order below is important to remove resources cleanly.
</p>
{{% /notice %}}

1. Go to AWS CloudFormation console in US West (N. Virginia) Region and delete the root (non-nested) stack that starts with the name *tCaT-forge-*. We had setup the CI/CD pipeline to not auto-delete the test stack to save testing time.
2. Go to AWS CloudFormation console in US West (Oregon) Region and first delete the *Forge-Prod-Stack*
3. Once *Forge-Prod-Stack* is deleted, delete the *Forge-App-CICD* stack.
4. Go to Amazon S3 console and delete the demo bucket, you can search for `au-demo` to list the buckets. You can also get the full bucket name from the files: *au-demo-bucket.txt*.
5. Go to AWS Cloud9 console and delete the Cloud9 workspace you created.