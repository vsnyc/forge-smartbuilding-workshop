+++
title = "Validating code update"
chapter = false
weight = 10
+++

1. After you have approved the change, the CodePipeline will execute the ChangeSet. Go to the CloudFormation console, you should see `Forge-Prod-Stack` being updated. 
![arch]({{< resource url="images/prod-stack-update-progress.png" >}})
2. In about 5 minutes, the stack will reach *UPDATE_COMPLETE* status.
![arch]({{< resource url="images/prod-stack-update-complete.png" >}})
3. Go to the `ForgeAppURL` again and verify that your application now shows a custom logo for the Forge app (Tested in Chrome browser)
![arch]({{< resource url="images/updated-app-with-custom-logo.png?height=60%&width=60%" >}})
