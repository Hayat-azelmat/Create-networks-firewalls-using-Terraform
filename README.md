## Automate-network-infrastructure-using-Terraform

we used Terraform to automate the creation of network infrastructure.
we will create two VPCs, one for public service and one for the database server. we'll also create firewalls rules for each network.

1- Create a directory called terraform-networks and change to it

>> mkdir terraform-networks
>> cd terraform-networks

2- Create required Terraform files

3-  Initialize Terraform & build the Terraform plan

>>  terraform init
>>  terraform plan

4-  create the resources

>>  terraform apply -auto-approve

now we will peer the two networks. 
This allows communication between machines in those networks using internal IP addresses. 
This means that databases can be deployed on a private network without external IP addresses, and those databases will only be reachable from the peered network.

