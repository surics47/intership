                                                                    Documentation 

In this project, I deployed a simple web application using Minikube and managed its deployment with Argo CD. The web application, a "Hello World" example, was containerized using Docker and hosted on my GitHub repository (https://github.com/surics47/intership). The deployment was performed on an AWS t3.large EC2 instance.

Setup AWS EC2 Instance: I provisioned an AWS EC2 instance of type t3.large to host the Kubernetes cluster. 
Minikube Installation: Installed Minikube on the AWS EC2 instance to create a local Kubernetes cluster. 
Deploying the Web Application: With Minikube up and running, I deployed the "Hello World" web application onto the Kubernetes cluster. This involved creating Kubernetes manifests defining the deployment, service, and ingress resources necessary to expose the application to external traffic. 
Containerization with Docker: To containerize the application, I Dockerized the application code and dependencies into a Docker image. This allowed for consistent deployment across different environments and simplified the packaging and distribution process. 
Setting Up Argo CD UI: Argo CD UI was then deployed onto the Minikube cluster to manage the application deployments. Argo CD provided a user-friendly interface for continuous delivery and GitOps workflows, streamlining the deployment process. 
Continuous Integration with GitHub: Leveraging GitHub, I set up continuous integration pipelines to automate the build and deployment process of the Docker image. This ensured that any changes to the application code triggered automated builds and updates to the Kubernetes cluster through Argo CD. 

 

                                                               Challenges Encountered and Resolutions
Network Connectivity Issues: Initially, I faced challenges with network connectivity between Minikube and the local machine. This was resolved by ensuring that Minikube was properly configured to communicate with the host machine. 
Integration with Argo CD UI: Integrating Argo CD UI with Minikube required careful configuration and setup to establish connectivity and authentication. Through troubleshooting and documentation referencing, I successfully configured Argo CD UI to manage deployments on Minikube. 
Port Forwarding Issues: Encountered issues with port conflicts while trying to access the Argo CD UI through port forwarding. Resolved by using a different port for port forwarding. 
Connectivity to Kubernetes API Server: Argo CD server pod was unable to connect to the Kubernetes API server. Resolved by verifying network connectivity and ensuring correct RBAC permissions. 
 

                                                                         Clean-Up Process 
Delete Argo CD and Argo Rollouts: Uninstall Argo CD and Argo Rollouts from the Kubernetes cluster using the respective manifests or Helm charts. 
Delete Application Deployments: Delete any application deployments managed by Argo CD or Argo Rollouts. 
Remove Docker Images: Remove the Docker images pushed to the registry, if any. 
Delete ConfigMaps and Secrets: Delete any ConfigMaps or Secrets created for application configuration. 
Remove Port Forwarding: Terminate any port forwarding sessions set up for accessing services. 

 

Clean Up Persistent Data: If any persistent data was created, remove it as needed. 

 

Delete Minikube Cluster: Delete the Minikube cluster to remove all associated resources. 
