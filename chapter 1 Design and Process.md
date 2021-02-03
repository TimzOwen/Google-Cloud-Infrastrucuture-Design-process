
## Google Cloud Infrastructure:
### Design and Process

#### Microservices

Decomposing applications into smaller executed and managable units

Architectural style of developing applicaitons.

Each part has its own area of responsibility

### defining services:

require gathering information and measuring impact of the solution

Understanding KPI:

### Requirement, Design & analysis

qualitative requirements:
    who, what ,why when and How

__Roles__ define goal of a user at some point

__Personas__ : describes a typical person who plays a role

__user Stories:__ describe a feature from the user's point of view.

__Evaluating user stories:__ with INVEST creteria for a checklist
    Independent 
    Negotiable
    Valuable
    Estimatable
    Small

__Analyzing your case study__:
    Refine roles listed
    Write persona for each role
    Write user stories for main features


#### Measuring KPIs and SLIs:

__KPIs__: 
    Key metrics used to measure success
    Techniacal KPIs:
        page views
        user registration
        checkouts
        clickthroughs
    Business KPI:
        Return on investment
        employer turnover
        customer churn

__KPIs must me SMART__

    Specific
    Measurable
    Achievable
    Relevant
    Time-bound

__SLOs__: a target reliability you want your service to achieve


### Microservices Design and architecture:

#### Microservices

Divides large program into multiple smaller, independent sercices:

__Monolith__: all components are packaged and deployed together at deployment time

#### Googl's products for deploying microservices:

    App engine 
    Cloud Run
    GYVE
    Cloud Functions:

#### Architecturing microservices:

    Decompose applications by feature to minimize dependencies
    organize services by architetural layer
    Isolate services that provide shared funcitonality:

#### Microservices best practice

__12 Factors__:

    1.0 Codebase: 
         one codebase tracked in revision control, many deployments
    2.0 Dependencies:
         declare and Isolate dependencies
    3.0 Config: 
        store configuration in the environment
    4.0 Backing services:
        treat them as attched resources
    5.0 Build,Release & Run:
        Separate build & Run stages
    6.0 Processes:
        Execute the app as one or more stateless processes
    7.0 Port building:
        Export services via port building
    8.0 Concurency:
        Scale out via process model
    9.0 Disposibility:
        max robustness with fast startup and graceful shutdown
    10. Dev/prod parity:
        keep development, staging and production as similar as possible
    11. Logs:
        Treat logs as events streams 
    12 Admin process:
        Run admin/managemnent tasks as one-off process

#### REST Deployment with Microservices: (Representational  State Transfer)

REST is protocol independent

HTTP is the most common 

gRPC is also supported (supports __streaming__)

__RESTful__ are service points supporting REST

__client__ and __server__ communicate Request-Response processing


#### RESTful service Communication via web:
 
URIs (or endpoints) identify resources

REST apps provide consistent uniform interfaces

Caching of immutable representations is appropriate     

__Resource__ is an abstract notion of information

__Batch APIs__: Returns collection of items instead of single items

