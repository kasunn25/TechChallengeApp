# Servian Technical Challenge
Demonstrate devops skills by deploying a simple GTD application backed by a PostgreSQL database into the Azure cloud environment.

## Deploy Instructions
- Git clone https://github.com/kasunn25/TechChallengeApp.git
- Push the changes to _develop_ brach (pull request or direct push).
- Changes are deployed to here: https://20.120.93.130

## Achitecture Diagram
[![N|](https://user-images.githubusercontent.com/2141943/196047859-26e388be-222a-4187-9d66-7a4e2ccc4ce3.png)]()

## Assessment Requirements
- Solution is automated using Azure pipelines and deployments can be initiated from Github repository (public) commits.
- Git flow was implemented and pipelines are integrated to the _develop_ branch.
- Deployment related changes are included in the ~/k8s folder.
- Docker image versioning is maintained in the _azure-pipelines-variables.yml_ file, howerver image versioning can be handled in several ways based on the requirement.
- Azure Terraform can be used to automate the insfastructure (improvement), however postgres sql HA setup is deployed using helm charts.
- Front end and DB is highly available with k8s deployments (3 pods each), k8s will ensure the HA setup along with the traffic management.
- K8s secret management was used to ensure the data security.
- AKS is simple cluster with two nodes of 4GB ram.

## Improvements
- Automate insfastructure using Azure terraform.
- Inlcude postgres HA setup to release pipeline.
- Auto merge code to _master_ branch when deploy the image to production environment.
- Install reverse-proxy and API manager for data data security.
- Pipeline improvements are included as comments to _azure-pipelines.yml_.