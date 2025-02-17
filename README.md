#steps of this project architecture#

Create a vpc with 2 public subnets, route tables, 1 internet gateway, no NAT gateway required as we are targeting public subnets with terrafom code. if want to use NAT create it but before that create 2 private subnets and deploy 5 ec2, 2 for frontend and 2 for backend. now attach NAT gateway.

Configure all the tools like installations and configurations using bastion host/jump host server.
once the environment is ready. now hit endpoint of jenkins and install plugins and also configure tools. 

Now write jenkins pipelines stages and make environment ready like one for frontend and one for backend. also write a seperate pipeline for terraform stages so that we can automate the infra setup.

Now build the pipelines which undergos the sequential stages like checkout, sonar scanning, build, docker image, trivy, deploy to ECR and deploy to kubernetes.

Now hit the end point of load balancer check the webpage of both frontend and backend.
now integrate the backend with RDS by entering .env file and add details of RDS username and password. or by automate with pipeline. now hit the end point of load balancer and check the webpage and try to add a record if it's adding to backend RDS server. 

Now you can see the updated record.

