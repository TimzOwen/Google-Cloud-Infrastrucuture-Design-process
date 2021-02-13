
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
    
#### Designing Reliable systems

Consider __Reliability__  , __Scalability__ and __Durability__

Avoid single point of Failure:

    Define your unit of deployment 
    Each unit can handle extra load
    Don't make single unit large

Be ware of corelation failure 

Avoid corelated failures:

    Decouple server and use microservices distributed among multiple failures

Beware of cascading

    occurs when one system fails causing others to be overloaded

Query of death overload:

    condition where a request made to the server causes a failure
    caused by over consuption  of resources

positive feedback cycle overload failure:

    Making a system more reliable by adding retries in event of failure BUT creates a potential for overload
