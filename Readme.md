# Deploy a static app on ec2 instance using Ansible.

This guide provides a step-by-step procedure to deploy a static webpage on an AWS EC2 instance using Ansible. The repository contains the following files:

- index.html: The static webpage content.
- inventory.ini: The Ansible inventory file containing the details of your EC2 instance.
- First_Playbook.yaml: The Ansible playbook to configure the EC2 instance and deploy the webpage.

# Prerequisites

- An AWS account with an EC2 instance running.
- Ansible installed on your local machine(control node).
- SSH access to your EC2 instance(manage node).
- Ensure the index.html, inventory.ini, and First_Playbook.yaml files are in your repository.

# Procedure

- Step 1: Create an Ansible Inventory File
Create an inventory.ini file to specify the EC2 instance details(public ip address of your manage node)

- Here, I have already given the inventory.ini file for you, if your trying this project by your end, then change the public ip addresses inside the inventory.ini file as per your ip addresses of your manage nodes.

- Step 2: Create the Static Webpage
Create an index.html file with your static webpage content. you can use the above index.html file. If you want to change anything according to your content. Feel free to do it.

- Step 3: Create an Ansible Playbook
Create a First_Playbook.yaml file to configure the EC2 instance and deploy the static webpage. The file  for this is given above. Feel free to change anything accordingly.

- Step 4: Run the Ansible Playbook
Use the following command to run the Ansible playbook and deploy the static webpage.

ansible-playbook -i inventory.ini First_Playbook.yaml

- Step 5: Access Your Webpage
Once the playbook execution is complete, open a web browser and navigate to http://your-ec2-instance-public-ip to view your static webpage. But make sure that you allow inbound traffic port 80. You can add a security group rule in the aws console under your particular ec2 instance.
