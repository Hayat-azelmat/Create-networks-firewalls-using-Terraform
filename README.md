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

switch to branch peering-networks (we need to add vpc-peering.tf)

In the branch deploy-vm Once the networks are peered, machines in the private network do not need a public IP address
we provision a Linux virtual machine in a private network to act as a database server. You also create a virtual machine that you can use as a bastion host to connect to the database server as an administrator

