

Part 1. Background
    
1 Why GitOps?
    
                1.1 Evolution to GitOps
                    - Traditional Ops
                    - DevOps
                    - GitOps
                1.2 Developer benefits of GitOps
                    - Infrastructure as code
                    - Self-service
                    - Code reviews
                    - Git pull requests
                1.3 Operational benefits of GitOps
                    - Declarative
                    - Observability
                    - Auditability and compliance
                    - Disaster recovery

2 Kubernetes And GitOps
    
                2.1 Kubernetes introduction
                    - What is Kubernetes?
                    - Other container orchestrators
                    - Kubernetes architecture
                    - Deploying to Kubernetes
                2.2 Declarative vs. imperative object management
                    - How declarative configuration works
                2.3 Controller architecture
                    - Controller delegation
                    - Controller pattern
                    - NGINX operator
                2.4 Kubernetes + GitOps
                2.5 Getting started with CI/CD
                    - Basic GitOps operator
                    - Continuous integration pipeline
        
Part 2. Patterns And Processes
    
3 Environment Management
    
                3.1 Introduction to environment management
                       - Components of an environment
                       - Namespace management
                       - Network isolation
                       - Preprod and prod clusters
                3.2 Git strategies
                       - Single branch (multiple directories)
                       - Multiple branches
                       - Multirepo vs. monorepo
                3.3 Configuration management
                        - Helm
                        - Kustomize
                        - Jsonnet
                3.3.4 Configuration management       
                3.4 Durable vs. ephemeral environments
      
4 Pipelines
    
                4.1 Stages in CI/CD pipelines
                       - GitOps continuous integration
                       - GitOps continuous delivery
                4.2 Driving promotions
                        - Code vs. manifest vs. app config
                        - Code and image promotion
                        - Environment promotion
                        - Putting it all together
                4.3 Other pipelines
                4.3.1 Rollback
                4.3.2 Compliance pipeline
      
5 Deployment Strategies
    
                5.1 Deployment basics
                        - Why ReplicaSet is not a good fit for GitOps
                        - How Deployment works with ReplicaSets
                        - Traffic routing
                        - Configuring minikube for other strategies
                5.2 Blue-green
                        - Blue-green with Deployment
                        - Blue-green with Argo Rollouts
                5.3 Canary
                        - Canary with Deployment
                        - Canary with Argo Rollouts
                5.4 Progressive delivery
                        - Progressive delivery with Argo Rollouts
      
6 Access Control And Security
    
                6.1 Introduction to access control
                       - What is access control?
                       - What to secure
                       - Access control in GitOps
                6.2 Access limitations
                        - Git repository access
                        - Kubernetes RBAC
                        - Image registry access
                6.3 Patterns
                        - Full access
                        - Deployment repo access
                        - Code access only
                6.4 Security concerns
                        - Preventing image pull from untrusted registries
                        - Cluster-level resources in a Git repository
      
7 Secrets
    
                7.1 Kubernetes Secrets
                        - Why use Secrets?
                        - How to use Secrets
                7.2 GitOps and Secrets
                        - No encryption
                        - Distributed Git repos
                        - No granular (file-level) access control
                        - Insecure storage
                        - Full commit history
                7.3 Secrets management strategies
                        - Storing Secrets in Git
                        - Baking Secrets into the container image
                        - Out-of-band management
                        - External Secrets management systems
                        - Encrypting Secrets in Git
                        - Comparison of strategies
                7.4 Tooling
                        - HashiCorp Vault
                        - Vault Agent Sidecar Injector
                        - Sealed Secrets
                        - Kustomize Secret generator plugin
                        
8 Observability
    
 
                8.1 What is observability?
                        - Event logging
                        - Metrics
                        - Tracing
                        - Visualization
                         - Importance of observability in GitOps
                8.2 Application health
                       - Resource status
                       - Readiness and liveness
                       - Application monitoring and alerting
                8.3 GitOps observability
                        - GitOps metrics
                        - Application sync status
                        - Configuration drift
                        - GitOps change log
                        
Part 3. Tools
    
9 Argo CD
    
                9.1 What is Argo CD?
                        - Main use cases
                        - Core concepts
                        - Sync and health statuses
                        - Architecture
                9.2 Deploy your first application
                        - Deploying the first application
                        - Inspect the application using the user interface
                9.3 Deep dive into Argo CD features
                        - GitOps-driven deployment
                        - Resource hooks
                        - Postdeployment verification
                9.4 Enterprise features
                        - Single sign-on
                        - Access control
                        - Declarative management
                        
10 Jenkins X
    
                10.1 What is Jenkins X?
                10.2 Exploring Prow, Jenkins X pipeline operator, and Tekton
                10.3 Importing projects into Jenkins X
                    - Importing a project
                    - Promoting a release to the production environment
        
11 Flux
                
                11.1 What is Flux?
                    - What Flux does
                    - Docker registry scanning
                11.1.Architecture
                11.2 Simple application deployment
                    - Deploying the first application
                    - Observing application state
                    - Upgrading the deployment image
                    - Using Kustomize for manifest generation
                    - Securing deployment using GPG
                11.3 Multitenancy with Flux
      
Appendix A. Setting Up A Test Kubernetes Cluster
    
                A.1 Prerequisites for working with Kubernetes
                    Configure kubectl
                    Installing minikube and creating a cluster
                    Configuring minikube
                    Creating a GKE cluster in GCP
                    Creating an EKS cluster in AWS

Appendix B. Setting Up GitOps Tools

                Installing Argo CD
                Installing Jenkins X
                    Prerequisites
                    Installing Jenkins X in a Kubernetes cluster
                Installing Flux
                    Installing CLI client
                
Appendix C. Configuring GPG Key
                