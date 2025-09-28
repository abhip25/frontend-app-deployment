# Front End Application Deployment on ECS.

## Step 1 : Start with Setting up ECR for Storing the Docker

Amazon ECR (Elastic Container Registry) is a fully managed AWS service to store, manage, and share Docker container images.
Think of it as AWS’s own “DockerHub,” but integrated with IAM, ECS, EKS, and CodeBuild/CodePipeline for secure and seamless deployments.
point to be noted:
if you use immutable while creating ECR: use sha hash while push images or else if you use latest tag you use mutable or else you will face error.
<img width="958" height="240" alt="ecr_repo" src="https://github.com/user-attachments/assets/432d6874-0454-40f6-b620-fb423521ba1d" />

## Step 2: Building pushing the code to Repo

Here is the File structure of our Front end Code.
<img width="1840" height="920" alt="image" src="https://github.com/user-attachments/assets/bbad7193-795c-47a9-9c1a-034ca96749e8" />

## Step 3 : Setting up BuildProject

Buildproject will help us to building the Docker Image and pushing it to ECR Repo
<img width="824" height="475" alt="buildspec_file" src="https://github.com/user-attachments/assets/5ae4b02e-7d1e-44af-ae4d-2eb01d468dd8" />

## Step 4: Setting up Cluster and Load Balancers.
<img width="955" height="184" alt="ecs_cluster" src="https://github.com/user-attachments/assets/72a324da-a5c8-4859-abfc-814cc0c93441" />

<img width="937" height="430" alt="lb" src="https://github.com/user-attachments/assets/68fd6c1d-6f90-4b57-ac6d-4d7a30834455" />


## Step 5: Setting up Pipeline

<img width="947" height="407" alt="pipeline" src="https://github.com/user-attachments/assets/2ebf12a6-7441-4aff-9ad8-7b7db7a3d519" />

# Step 6: Validating

<img width="937" height="430" alt="health_tg" src="https://github.com/user-attachments/assets/c03f2d96-42af-466e-af4c-d518f5f9d566" />
<img width="939" height="428" alt="running_tasks" src="https://github.com/user-attachments/assets/d498999e-0933-403e-9b20-2faa31b35d13" />
<img width="953" height="447" alt="website-post-deployment" src="https://github.com/user-attachments/assets/31c97675-99d6-4ae0-941e-3421abef4cf1" />





