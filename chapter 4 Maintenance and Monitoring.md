

### Managing versions

This is a service update from one version to another 

fro deploying breaking version be sure to iclude changes

Need to test versions before going live 


__rolling update__ allows you to deploy new version with no downtime

use __blue/green__ deployment when you dont want multiple version of service to run simultneously

    blue --> current
    green --> creating completly new environment

__Cananry update__ can be used prior to rolling update to reduce the risk.



### Cost planning

This is a continoud iterative cycle of 
    Deploy 
    approve
    allocate
    Forecast


__Optimize cost of compute:__

    start with small vms and see weather they work or not 
    consider small machines withiut auto scalling
    consider atleast some preentive instances

Optimzing disk cost 

Optimize network cost (keep machines close)

prevent overpositioning of kubernetes clusters (user GkE metering).

compare storage preferences

consider alternative services to save cost 

use Google cloud pricing calculator

use biling reports to provide details 

Export biling data to BigQuery 

Visual spend with Google Studio




### Monitoring Dashboard

Google unifies the tools you need to monitor your SLOs and SLAs

Monitoring dashboard monitor your service

__Cloud Monitoring__ creates default dashboards for your project

create __uptime check__ to monitor availability and latency

create alart when your service doesn't meet your SLOs



