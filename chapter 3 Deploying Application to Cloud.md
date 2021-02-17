
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



### Disaster Planning:

Can be achieved by deploying to multiple Zones in a region

    Multiple servers

    distributed db link

    Orchestrate servers with a regional Managed instance

Also have __regional managed__ instance group

    multiple zones

Deploy kubernetes in multiple zones 

Create __health check__ to enable auto healing when creating vm instances

    Load balancers also use health check 

High availability can be achienved by using __multi-region__ storage buckets for hight 

    availabilty if latency impact id negligible

High availability in __ClousSQL__:

    create fail over replica

Deploying for high reliability increases cost


#### Disaster recovery:

__Cold standby__ creates snapshotsof the machine images

__Hot standby__  creates instance groups in multiple regions


#### Disaster planning:

__Recovery Point objective__ : Amount of data that would be acceptible to lose

__Recovery time Objective__ : Amount of time it can take to be back and running after a disaster


## Cloud and System's Security 

#### Security concept:

Google Cloud security is shared between Google and Clients.

Security implemented in layers:

    Hardware
    Boot
    OS + IPC
    Storage
    Application
    Deployment
    Operations
    Usage

Principle of least privilege:

    allows user to only access some certain permissions

Separation of duties:

    allows deployment or code review by multiple teams and not one
    different peopple different rights

Regular audit to Google Cloud logs to discover attacks

Security command Center 

    provide security configuration to different projects 
    


#### Securing People:

Login members and assign tasks based on their roles

Add member to groups for ease management

Use organizational folders and policy 

Cloud Identity-Aware Proxy  for ease authorization to GCP and VMs

Identity platforms as authentication services


#### Securing Machine access

Service accounts can be used for machines or applicaiton entities

Keys Cloud MS can be used to secure cloud Keys

Can use service account keys to configure the CLI

    useful for automation




### Network Security:


Remove __external Ips__ to prevent access to machines outside network

    use baston host for private machine
    SSH into internal machines
    CLous NAT to provide egress to internet from internal machines

All internet traffic should terminate at load balancers

__private access__ allows access to google cloud service using an internal address

    enable when creating subnets 

configure firewal rules to allows access to VMs

__Cloud Endpoints__ allows control over APIS

    valid evry call to json

Restric access to your services to TLS only 

    creates secure frontend

Leverage google cloud Cloud Armor to create network security


Cloud Armor provide 7 layer security



#### Encryption:

Google Cloud provides __server-side__ encryption of data at rest by default.


    Data encryption (DEK)
    Key encryption
    key rotation
    Key management Services (Personla key management in the cloud)

Customer supplied encryption are always created in user environment

__Data Loss Prevention API__ is used to protect sensitive data by finding it and redacting it

