# Active Deploy Service Plugin for Bluemix Delivery Pipeline Service

## Try me 
A simple Hello World Python application using Flask on Bluemix

Press this button, to get your own copy of the sample running in Bluemix! It clones the project, creates DevOps Services Project, generates multi-stage pipeline, deploys application to IBM Bluemix.

[![Deploy to Bluemix](https://bluemix.net/deploy/button.png)](https://bluemix.net/deploy?repository=https://github.com/Puquios/active-deploy.git)

## Let's Get Started
This simple pipeline demonstrates how active deploy capabilities can be used within Bluemix Delivery Pipeline services. Once you press the "Deploy to Bluemix" button and log in, you should see a set of steps run through:

![screenshot01](https://github.com/IBM-Bluemix/active-deploy/blob/master/sample-apps/pipeline/images/01_login.PNG)
![screenshot02](https://github.com/IBM-Bluemix/active-deploy/blob/master/sample-apps/pipeline/images/02_deploy.PNG)

Once completed, you can see your app running by clicking **"VIEW YOUR APP"**:

![screenshot03](https://github.com/IBM-Bluemix/active-deploy/blob/master/sample-apps/pipeline/images/03_deployed2BM.PNG)
![screenshot04](https://github.com/IBM-Bluemix/active-deploy/blob/master/sample-apps/pipeline/images/04_viewYourApp.PNG)

Also, you can click on the ***"EDIT CODE"*** button to access your own copy of the repository and ***"BUILD & DEPLOY"*** in the upper right hand corner to see and configure your pipeline:

![screenshot05](https://github.com/IBM-Bluemix/active-deploy/blob/master/sample-apps/pipeline/images/05_editCode.PNG)
![screenshot06](https://github.com/IBM-Bluemix/active-deploy/blob/master/sample-apps/pipeline/images/06_buildAndDeploy.PNG)

Here you will see a Build & Deploy pipeline - full info on this awesome DevOps capability can be found [here](https://hub.jazz.net/docs/deploy/).

  - Build stage
    - The first stage is the build stage - that is the standard build stage in Bluemix - however you create your application image in a pipeline is what would be done here. 
  - Deploy stage
    - The second stage is where the Active Deploy magic happens. The first time this project runs runs, Active Deploy won't run yet - but it will gave you a sample application running properly that you can now use to run Active Deploy to show you have the pipeline integration works. The Active Deploy pipeline stage information is fully described [here] (https://hub.jazz.net/docs/deploy_ext/#activedeploy).

1. The first time you run this pipeline:
  - Deploys the app as a Cloud Foundry application to Bluemix 
  - If you run ```cf apps``` from a command line (the labs to help get you acquainted with the command line can be found [here](https://github.com/IBM-Bluemix/active-deploy/blob/master/labs/README.md)) you will see this application running:  
  
  ![screenshot07](https://github.com/IBM-Bluemix/active-deploy/blob/master/sample-apps/pipeline/images/07_firstRun.PNG)
  
  or something similar - this is your initial sample application. Or you can look at the Bluemix console dashboard @ console.ng.bluemix.net to see your new application running.
  
  ![screenshot18](https://github.com/IBM-Bluemix/active-deploy/blob/master/sample-apps/pipeline/images/18_dashboard1.PNG)

2. The second time you run the pipeline:
  - If you execute the build stage again with the little arrow, it will re-execute the build, create a new image, and then re-run the Active Deploy Stage. This actually runs the Active Deploy this time through. 
  - You can see your deploy happening using these commands (adjusted for your results in command above):
    
  ![screenshot08](https://github.com/IBM-Bluemix/active-deploy/blob/master/sample-apps/pipeline/images/08_secondRun.PNG)
    
  Or you can look at the Active Deploy Console dashboard @ console.ng.bluemix.net => Services => Active Deploy.
  
  ![screenshot09](https://github.com/IBM-Bluemix/active-deploy/blob/master/sample-apps/pipeline/images/09_uiRunning.PNG)

You're Done!

![screenshot10](https://github.com/IBM-Bluemix/active-deploy/blob/master/sample-apps/pipeline/images/10_completed.PNG)
![screenshot11](https://github.com/IBM-Bluemix/active-deploy/blob/master/sample-apps/pipeline/images/11_uiCompleted.PNG)
![screenshot19](https://github.com/IBM-Bluemix/active-deploy/blob/master/sample-apps/pipeline/images/19_dashboard2.PNG)

That's it, you've now seen Active Deploy work in the Bluemix Build & Delivery Pipeline. The next step for you is to set it up in your own pipeline project.
    
## References 
* [Bluemix Active Deploy – Zero-Downtime Deployment](https://developer.ibm.com/bluemix/2015/10/09/bluemix-zero-downtime-deployment)
* [Diving into the Bluemix Active Deploy service](https://developer.ibm.com/bluemix/2015/10/19/getting-started-with-bluemix-active-deploy/)
