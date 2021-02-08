
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


