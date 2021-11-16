+++
title = "Updating the Quick Start"
chapter = false
weight = 10
+++

### Updating the Quick Start

We will now update our app and setup a CodePipeline to deploy our changes automatically. We'll replace the default app with an app that displays a custom logo for the deployed Forge web app. In the Cloud9 IDE:

1. In terminal, go to the repo packages directory: `cd ~/environment/quickstart-autodesk-forge/packages/`   
2. Download a new sample Forge app with a custom logo added. Look into the change we did to the forge-viewmodels-nodejs-aws-smartbuilding.zip app you had downloaded earlier to add a custom logo.
   
    ```bash
    curl -O https://aws-cfn-samples.s3.amazonaws.com/forge-workshop/demo/forge-viewmodels-nodejs-accent-athletics.zip
    ```
3. Update the contents of your demo bucket to include the modified Forge app with custom logo.

    ```bash  
    cd ~/environment  
    aws s3 sync quickstart-autodesk-forge s3://$AU_DEMO_BUCKET/quickstart-autodesk-forge/
    ```
4. open `~/environment/forge-prod-codepipeline.json`. Change the value of *ForgeAppName* in line 20 from `forge-viewmodels-nodejs-aws-smartbuilding` to `forge-viewmodels-nodejs-accent-athletics`. Save the file.
5. Update the CodePipeline configuration zip file `~/environment/quickstart-autodesk-forge.zip` with the modified `forge-prod-codepipeline.json`.
   
    ```bash
    cd ~/environment
    zip quickstart-autodesk-forge.zip forge-prod-codepipeline.json
    ```
6. In terminal, from the quickstart-autodesk-forge directory, add the files, commit and push. When asked for a password, use your GitHub personal access token created earlier (see [Create GitHub token] ( {{< relref "10_prerequisites/30_github_token" >}})).
           
    ```bash
    cd ~/environment/quickstart-autodesk-forge/
    git add -A
    git commit -m "Updated app to include a custom logo"
    git push
    ```