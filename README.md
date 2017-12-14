# bouker

## Microservices

All are hosted in organization on [Docker Hub](https://hub.docker.com/u/bouker/)

* [bouker/bouker-booking](https://hub.docker.com/r/bouker/bouker-booking/)
* [bouker/bouker-events](https://hub.docker.com/r/bouker/bouker-events/)
* [bouker/bouker-ui](https://hub.docker.com/r/bouker/bouker-ui/)


## How to setup the microservices on AWS (manually)

1. Choose VPC to use for the application.
2. Create ECS cluster and instances on that VPC. Make keypair to access instances on production.
3. Create Application Load Balancer with default target group. 
Prepare definition per container type. Register instances onto that ALB.
4. Create task definitions, if domain is needed in environment, use that of ALB.
5. Create separate services for task definitions. Create target groups for each service. 
You can configure routing paths and health checks (it can be also added later on). 
6. Configure security groups used. ALB should be reachable by HTTP from anywhere (0.0.0.0). 
