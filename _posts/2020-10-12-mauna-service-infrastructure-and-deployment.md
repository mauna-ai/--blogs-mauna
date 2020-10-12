


**Infrastructure**

The Mauna server has a fully scalable architecture. The services are deployed on the Managed Kubernetes service on AWS (EKS - Elastic Kubernetes Service). EKS provides scalability, high availability across many Zones and security. The Identity and Access Management (IAM) is integrated with the EKS.


To provision the AWS EKS Cluster, we use Terraform to have a better control on the provisioning and de-provisioning. The declarative code is easier to understand and change. The Terraform gives us the ability to get the infrastructure as code. On every push  to the git repository, the changes are automatically deployed. Therefore, giving us the capability of version control for the deployment code.


The workflow for Terraform is depicted in the diagram below:

![Terraform Workflow](http://localhost:4000/assets/img/terraform.png)  

**Continuous deployment**


An integral part of DevOps is adopting the culture of continuous integration and continuous deployment (CI/CD). Every commit or change to code passes through various automated stage gates. It includes building and testing, then deploying applications to all the environments (Development to Production).


Our solution include following Services:

1.Github 

2.AWS CodePipeline

3.Aws codeBuild

4.Fluxcd


**Github** We are using  github as a version-control system for tracking changes in source code and commits.


**CodePipeline** is a fully managed continuous delivery service that helps you automate your release pipelines for fast and reliable application and infrastructure updates. 


We have integrated Github with codepipeline to trigger changes and deploy these changes on ECR.


**CodeBuild** is one of the stages in the CodePipeline. With the help of code build we are testing our build and building docker images.


**Flux (CD)** is a tool that automatically ensures that the state of a cluster matches the config in git. It uses an operator in the cluster to trigger deployments inside Kubernetes, which means you don't need a separate CD tool. It monitors all relevant image repositories, detects new images, triggers deployments and updates the desired running configuration based on that (and a configurable policy).




**Deployment flows**


1. The basic idea is to manage resources on Kubernetes solely by committing changes to Git.


2. Write the Kubernetes manifests and push them to the Github repository.


3. Memcached is used to store the container image tags. Flux scans your cluster for container images and fetches the tags from our Private Container Registry. This allows Flux to automate the image tag update.


4. Detection of an image change (running container image tag vs container registry image tag) triggers k8s manifest update, which is committed to the user git repository, then deployed to the Kubernetes cluster.


5. In our scenarios, we are leveraging the AWS code build to build image and then Pushing images to private Elastic Container Registry




The Deployment process in described in the diagram below:


![Deployment Process](http://localhost:4000/assets/img/gitops.png)  




**Next Steps**

We are working continuously to improve the workflow and make the infrastructure more optimised and deployments to be more smoother. We are planning to integrate the monitoring of Application performance & logging as part of the pipeline. Continuous deployment will add quality gates to promote the code to the next stage.
