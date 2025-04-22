Terraform
Terraform 
	Init
	Plan
	Apply
	destroy  
Terraform is an open-source Infrastructure as Code (IaC) tool developed by HashiCorp that allows users to define, provision, and manage cloud infrastructure using a declarative configuration language called HCL (HashiCorp Configuration Language).


CI/CD
Legacy one is not scalable
Conti Integration and Conti delivery
Say there are many things before it reaches consumer,
Like unit testing, vulnerability scans etc,.. automating these steps is the concept here
SOME STANDARD STEPS
	UNIT testing : checking code for that specific functionality
	Static code analysis : well formatted, declarations, etc…
	Code quality/ vulnerability : any security patches
	Automation testing : functional testing, E2E testing, add func doesn’t effect sub func 
	Reports: how many cases passed etc,
	Deployment: nginx etc
TOOLS in CI/CD
If v1 is final , push it to github, now deploy a cicd tool like JENKINS
And state that , watch that repo and whenever there is a new commit/branch , just tell me ,
Then jenkins will run those specific tasks
Jenkins acts as a tunnel/ orchestrate a lot of tools

Jenkins is an open-source automation server written in Java that helps automate parts of the software development process, such as building, testing, and deploying code. It supports Continuous Integration (CI) and Continuous Delivery (CD) and can be extended through a wide variety of plugins.
Like say JAVA , maven /JUNIT
SONAR for code quality
ALM for reporting
Devops engineer will include all these things in Jenkins so that they get run whenever changes in github are made
JENKINS called Orchestrator –integrates all of these tools (Jenkins pipelines)
THREE ENVIRONMENTS
	Dev, stage and prod(end user is using)
Jenkins -binary 
Deploy Jenkins on single lap and keeps on adding machines 

MODERN DAY 
Say there are 1000 of microservices running and u have 20-30 jenkins setup and 100 vms that might scale up and down based on traffic , when on 0 day usage all those 100 vms are not used properly, in this situation JENKINS not recommended	

So take github , the github actions thing , when ever any pull req/code changes occurs, it calls a k8 pod or a docker container that spins off the entire things and things executed
If we are not using servers, those’ll be used by some other projects(like a shared resource)

RUNNERs are worker nodes from Microsoft, those will create servers/pods

So, instead of creating multiple Jenkins instances, create github actions so that multiple projects can be exec on that


HANDS ON WITH JENKINS
Create an ec2 instance and copy public ip address
>ssh -i Users\medikondajyothi.s\Downloads\jenkins.pem ubuntu@54.242.177.37 like this in cmd
Install java -> Jenkins using commands from official site

Ps -ef | grep jenkins

In ec2
Goto security and inbound rules—all traffic 8080

AFTER FINISHING JENKINS SETUP
--jenkins master is used for scheduling purpose(to reduce load)

ISSUE WITH MASTER-WORKER:
Say there are 3 workers under one master(mac,linux, win)
But window’s worker is not getting any req, so that parti node resource is being wasted
Hence, in modern day env
Came up Jenkins with docker container (agents)
Light weight against containers 
Containers usage is good
Used docker containers as agents in our jenkins setup

Program:
Jenkins-Zero-To-Hero/my-first-pipeline at main · iam-veeramalla/Jenkins-Zero-To-Hero · GitHub

Jenkin requests docker to provide container to run pipeline and after exec , it terminates container

CAME ACROSS FEW WEB PAGES
Uses.tech/like
Fortinet sde3

OrgoCD is a modern day declarative continu deliv 
They are basically Kubernetes controller, ensures state is always the same


Docker run -it docker.file
Develop everything on jenkins pipeline and deploy it on Kubernetes cluster

Multi stage multi agent
Say an organization with 3 tier front,back and db architecture and each are of different things like backend on centos , frontend on someother thing

So when writing code, 
 
For db, any image with preinstalled db like oracle

JENKINS interview questions
1)	CICD pipelines

Kubernetes (also called K8s) is an open-source platform used to automate the deployment, scaling, and management of containerized applications (like apps running inside Docker).
🔧 In short:
Kubernetes = A system to manage containers (like Docker) across multiple machines.

