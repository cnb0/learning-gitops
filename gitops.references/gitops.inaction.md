

Part 1. Background
    
1 Why GitOps?
    
            1.1 Evolution to GitOps
            1.1.1 Traditional Ops
            1.1.2 DevOps
            1.1.3 GitOps
            1.2 Developer benefits of GitOps
            1.2.1 Infrastructure as code
            1.2.2 Self-service
            1.2.3 Code reviews
            1.2.4 Git pull requests
            1.3 Operational benefits of GitOps
            1.3.1 Declarative
            1.3.2 Observability
            1.3.3 Auditability and compliance
            1.3.4 Disaster recovery

2 Kubernetes And GitOps
    
            2.1 Kubernetes introduction
            2.1.1 What is Kubernetes?
            2.1.2 Other container orchestrators
            2.1.3 Kubernetes architecture
            2.1.4 Deploying to Kubernetes
            2.2 Declarative vs. imperative object management
            2.2.1 How declarative configuration works
            2.3 Controller architecture
            2.3.1 Controller delegation
            2.3.2 Controller pattern
            2.3.3 NGINX operator
            2.4 Kubernetes + GitOps
            2.5 Getting started with CI/CD
            2.5.1 Basic GitOps operator
            2.5.2 Continuous integration pipeline
      
Part 2. Patterns And Processes
    
3 Environment Management
    
            3.1 Introduction to environment management
            3.1.1 Components of an environment
            3.1.2 Namespace management
            3.1.3 Network isolation
            3.1.4 Preprod and prod clusters
            3.2 Git strategies
            3.2.1 Single branch (multiple directories)
            3.2.2 Multiple branches
            3.2.3 Multirepo vs. monorepo
            3.3 Configuration management
            3.3.1 Helm
            3.3.2 Kustomize
            3.3.3 Jsonnet
            3.3.4 Configuration management       
            3.4 Durable vs. ephemeral environments
      
4 Pipelines
    
            4.1 Stages in CI/CD pipelines
            4.1.1 GitOps continuous integration
            4.1.2 GitOps continuous delivery
            4.2 Driving promotions
            4.2.1 Code vs. manifest vs. app config
            4.2.2 Code and image promotion
            4.2.3 Environment promotion
            4.2.4 Putting it all together
            4.3 Other pipelines
            4.3.1 Rollback
            4.3.2 Compliance pipeline
      
5 Deployment Strategies
    
            5.1 Deployment basics
            5.1.1 Why ReplicaSet is not a good fit for GitOps
            5.1.2 How Deployment works with ReplicaSets
            5.1.3 Traffic routing
            5.1.4 Configuring minikube for other strategies
            5.2 Blue-green
            5.2.1 Blue-green with Deployment
            5.2.2 Blue-green with Argo Rollouts
            5.3 Canary
            5.3.1 Canary with Deployment
            5.3.2 Canary with Argo Rollouts
            5.4 Progressive delivery
            5.4.1 Progressive delivery with Argo Rollouts
      
6 Access Control And Security
    
            6.1 Introduction to access control
            6.1.1 What is access control?
            6.1.2 What to secure
            6.1.3 Access control in GitOps
            6.2 Access limitations
            6.2.1 Git repository access
            6.2.2 Kubernetes RBAC
            6.2.3 Image registry access
            6.3 Patterns
            6.3.1 Full access
            6.3.2 Deployment repo access
            6.3.3 Code access only
            6.4 Security concerns
            6.4.1 Preventing image pull from untrusted registries
            6.4.2 Cluster-level resources in a Git repository
      
7 Secrets
    
            7.1 Kubernetes Secrets
            7.1.1 Why use Secrets?
            7.1.2 How to use Secrets
            7.2 GitOps and Secrets
            7.2.1 No encryption
            7.2.2 Distributed Git repos
            7.2.3 No granular (file-level) access control
            7.2.4 Insecure storage
            7.2.5 Full commit history
            7.3 Secrets management strategies
            7.3.1 Storing Secrets in Git
            7.3.2 Baking Secrets into the container image
            7.3.3 Out-of-band management
            7.3.4 External Secrets management systems
            7.3.5 Encrypting Secrets in Git
            7.3.6 Comparison of strategies
            7.4 Tooling
            7.4.1 HashiCorp Vault
            7.4.2 Vault Agent Sidecar Injector
            7.4.3 Sealed Secrets
            7.4.4 Kustomize Secret generator plugin
                
8 Observability
    
 
            8.1 What is observability?
            8.1.1 Event logging
            8.1.2 Metrics
            8.1.3 Tracing
            8.1.4 Visualization
            8.1.5 Importance of observability in GitOps
            8.2 Application health
            8.2.1 Resource status
            8.2.2 Readiness and liveness
            8.2.3 Application monitoring and alerting
            8.3 GitOps observability
            8.3.1 GitOps metrics
            8.3.2 Application sync status
            8.3.3 Configuration drift
            8.3.4 GitOps change log
                
Part 3. Tools
    
9 Argo CD
    
            9.1 What is Argo CD?
            9.1.1 Main use cases
            9.1.2 Core concepts
            9.1.3 Sync and health statuses
            9.1.4 Architecture
            9.2 Deploy your first application
            9.2.1 Deploying the first application
            9.2.2 Inspect the application using the user interface
            9.3 Deep dive into Argo CD features
            9.3.1 GitOps-driven deployment
            9.3.2 Resource hooks
            9.3.3 Postdeployment verification
            9.4 Enterprise features
            9.4.1 Single sign-on
            9.4.2 Access control
            9.4.3 Declarative management
                
10 Jenkins X
    
            10.1 What is Jenkins X?
            10.2 Exploring Prow, Jenkins X pipeline operator, and Tekton
            10.3 Importing projects into Jenkins X
            10.3.1 Importing a project
            10.3.2 Promoting a release to the production environment
      
11 Flux
                
            11.1 What is Flux?
            11.1.1 What Flux does
            11.1.2 Docker registry scanning
            11.1.Architecture
            11.2 Simple application deployment
            11.2.1 Deploying the first application
            11.2.2 Observing application state
            11.2.3 Upgrading the deployment image
            11.2.4 Using Kustomize for manifest generation
            11.2.5 Securing deployment using GPG
            11.3 Multitenancy with Flux
      
Appendix A. Setting Up A Test Kubernetes Cluster
    
            A.1 Prerequisites for working with Kubernetes
            A.1.1 Configure kubectl
            A.2 Installing minikube and creating a cluster
            A.2.1 Configuring minikube
            A.3 Creating a GKE cluster in GCP
            A.4 Creating an EKS cluster in AWS

Appendix B. Setting Up GitOps Tools

            B.1 Installing Argo CD
            B.2 Installing Jenkins X
            B.2.1 Prerequisites
            B.2.2 Installing Jenkins X in a Kubernetes cluster
            B.3 Installing Flux
            B.3.1 Installing CLI client
            Appendix C. Configuring GPG Key
                