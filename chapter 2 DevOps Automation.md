
### DevOps Automation

#### Continous Integration Pipelines

Automating building Applications:

    Developers check in code
    Run unit test 
    Build deployment package
    Deploy

#### Googl'e CI pipelines:

    Cloud source Repositories
        Devs push to a common/ Central repository for collaboration
    Cloud build:
        executes steps required to make deployment package/ Docker image
    Build Triggers:
        watches for changes in git repo and starts build
    Container registry:
        Store your docker images /Deployment packages in a central location fro deployment


#### Infrastructure as Code (IaC):

Allows automatic scaling

Cloud infrastructure needs to be disposable

Can automate using Scripts

__IaC__ allows provisioning and removal of infrastructure quickly

    Build and destroy infrastructure arcoding to needs
    cab be part of CI/CD Pipelines

#### IaC Tools:
    Deployment Manager
    Puppet 
    Packer
    Chef
    Terraform
    Ansible


### Cloud Storage & Data solutions

#### Cloud Managed Storage portfolio:

    Relatoional 
        Cloud SQL
        Cloud Spanner
    NoSQL
        Firestore
        CLoud Bigtable
    Object
        Cloud Storage
    Warehouse
        BigQuery
    In Memory
        Memorystore


#### Durability represent the odds of losing data.

Storage choice:
    
    Amount of data is important and also number of reads and writes.

    some scalling automatic and manual

Consistency: 

    strong consistency.
    Cloud SQL
    Spanner
    Firestore

Cost:

    cost per GB
    

#### Choosing Google Cloud Storage and Data solutions:

Includes:
    Relatoional 
    NoSQL
    Object
    Warehouse
    In-memory

Moving speed data depends on data.

### Google Cloud and Hybrid Network Architecture:

#### Designing Google Cloud Netwroks:

Design network based on:
    Location
    number of users
    scalability
    Fault tolerance
    company service requirement


#### VPC networks
    create subnets for regions
    choose close regions
    projects can have multiple regions 

#### Creating Network subnets:

    IP ranges cannot overlap
    Machines with same VPC can communicate with internal IP

Vms can have multiple network interfaces connecting to different networks

Shared VPc allows project sharing 

#### Designing Google cloud Laod balancers:

__Global Load balancers__ supported by __HTTP__ load balancer  and TCP and SSL proxies:

#### Single region laod balacing:

supported by __HTTP__, __TCP__ and __UDP__ load balancers

Can have public or private IP address

    for public secure them with SSL

Can use any TCP or UDP port

#### Achieve low latency by leveraging Cloud CDN.

Cache static web contents

cache static data from web servers

Enabled with starting HTTP Global

__Network Inteligence Center__:

    used to visualize netwrok topology

    Test network connectivity


#### Connecting Networks:

Use __VPC Peering__ to connect networks when they are both in Google Cloud

    Subnets cannot overlap

    Admins must approve each VPc request.

Use __Cloud VPN__ to connect networks __on-premise__ or in another cloud

    can configure static or dynamic configuration using (BGP)

__For high availability VPN__:

    2 Netwroks 
    2 IP address
    Multiple VPN support for each network

__For high speed between two networks__:

    use Cloud Interconnect 

    provide direct connection

    provide connection through service provider

