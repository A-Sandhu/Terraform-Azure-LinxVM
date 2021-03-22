# Build and deploy the infrastructure with using Terraform. 

1 - With your Terraform template created, the first step is to initialize Terraform. This step ensures that Terraform has all the prerequisites to build your template in Azure.

terraform init

2-  The next step is to have Terraform review and validate the template. This step compares the requested resources to the state information saved by Terraform and then outputs the planned execution. The Azure resources aren't created at this point.

terraform plan

3-  In third step, you're ready to build the infrastructure in Azure, apply the template in Terraform:

terraform apply

4-  Once Terraform completes, your VM infrastructure is ready. Obtain the public IP address of your VM with az vm show:

az vm show --resource-group myResourceGroup --name myVM -d --query [publicIps] -o tsv

5- You can then SSH to your VM:

ssh azureuser@<publicIps>
