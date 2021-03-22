# Terraform-Azure-LinxVM

Build and deploy the infrastructure wuth using Terraform. 

# With your Terraform template created, the first step is to initialize Terraform. This step ensures that Terraform has all the prerequisites to build your template in Azure.

terraform init

# The next step is to have Terraform review and validate the template. This step compares the requested resources to the state information saved by Terraform and then outputs the planned execution. The Azure resources aren't created at this point.

terraform plan

# In third step, you're ready to build the infrastructure in Azure, apply the template in Terraform:

terraform apply

# Once Terraform completes, your VM infrastructure is ready. Obtain the public IP address of your VM with az vm show:

az vm show --resource-group myResourceGroup --name myVM -d --query [publicIps] -o tsv

# You can then SSH to your VM:

ssh azureuser@<publicIps>
