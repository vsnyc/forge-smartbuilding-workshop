+++
title = "Deploy Quick Start"
chapter = false
weight = 10
+++

1. Copy the contents of your cloned repo with the sample demo Forge application to your demo bucket.
   
    ```bash  
    cd ~/environment  
    aws s3 sync quickstart-autodesk-forge s3://$AU_DEMO_BUCKET/quickstart-autodesk-forge/
    ```
2. Deploy the Quick Start with the default Forge application by running the command below. This will create a new CloudFormation stack in your account with the name: *Forge-Prod-Stack*.
  
    ```bash
    bash run_cfn.sh
    ```    
    The *run_cfn.sh* bash script contains a single AWS CLI command to create a CloudFormation stack.
   
       <pre>
         aws cloudformation --region us-west-2 create-stack --stack-name Forge-Prod-Stack \
         --template-url https://${AU_DEMO_BUCKET}.s3.us-west-2.amazonaws.com/quickstart-autodesk-forge/templates/autodesk-forge-main.template.yaml \
         --parameters file://forge-prod-cfn.json \
         --capabilities "CAPABILITY_IAM" --disable-rollback
        </pre>
3. This step will take approximately 15 minutes, we'll come back and verify that our base application has deployed correctly. To test your application, go to the AWS console and navigate to CloudFormation console and choose the `Forge-Prod-Stack`. In the Outputs section, go to the link provided as the value of `ForgeAppURL`.
![arch]({{< resource url="images/prod-stack-complete.png?height=60%&width=60%" >}})
4. Go to the *ForgeAppURL* to verify the default application. 
5. Download a [sample smart building](https://s3.amazonaws.com/aws-cfn-samples/forge-workshop/demo/rme_advanced_sample_project.rvt) model.
6. Follow these instructions to create a new bucket, upload the model file and translate it.
The view will differ based on what is stored in your buckets.
![arch]({{< resource url="images/run_sample_viewmodels.gif?height=60%&width=60%" >}})
7. Interact with the deployed sample and translated smart building model.
![arch]({{< resource url="images/sample-building-model.png?height=60%&width=60%" >}})
