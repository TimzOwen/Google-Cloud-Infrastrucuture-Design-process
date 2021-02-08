
### Deploying to the CLoud:

### Deploying

#### Google Cloud (IaaS: Infrastructure as a Service):

__Compute engiene__:

    Apps are not containerized
    self-hosted database
    complete control over OS

allows creating instance templates

used as a backend for load balancers


#### Deployment platforms

GKE: (Google Kuberbetes Engine):

    Automate the creation and management of Compute infrastrucure:
    services deployed into pods
    mutiple services deployment on one cluster

Cloud Run:

    allows you to deploy containters to Google managed kubernetes engine clusters.
    apps must be stateless
    Need to deploy apps using Docker images in Container Registry
    Automate deployment to your own GKE cluster.

App Engine:

    Designed for Microservices
    each Google project can contain 1 app Engine
    app has 1.more service
    each service has 1/more versions
    version have 1/more instances
    Automatic traffic splitting for switching versions.

Cloud Functions:

    Create loosly coupled, event driven miscroservices
    Can be triggered by changes in a storage bucket ], Pub/Sub messages or web request.
    Completely managed, scalable and inexpensive
    
