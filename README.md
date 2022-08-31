## Push-to-Deploy Example Using GitHub Actions for DigitalOcean
This repository contains an example workflow using the [GitHub Action for DigitalOcean](https://github.com/digitalocean/action-doctl) to build, tag, push a container image to your DigitalOcean container registry and deploy to a DigitalOcean Kubernetes cluster.

To make this process possible I follow the next doc: https://docs.digitalocean.com/tutorials/enable-push-to-deploy/ 

## Notes:
Is necesary get/create the next things:

  - A Container Registry in Digital Ocean, after that is necesary associate it a Kubernetes cluster.
    - The Container Registry module is free if it have size 500MB or least
    - Also, in free version we just have a one repository image
  - A Personal Access Token to use to Login in Container Registry module and set an enviroment secret in GitHub
 

##### The workflow creates in the default Kubernetes's namespace the service and deployment. If you will check this, you will put load balancer IP in browser. The message you will get is "Hello there!! You requested /"
