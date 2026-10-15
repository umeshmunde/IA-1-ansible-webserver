# DevOps Workflow and Architecture

## Real-world scenario
A small company needs to host its informational website on an Ubuntu server running on AWS EC2. Ansible automates Nginx installation and configuration, while Nginx serves the sample static webpage.

## Lifecycle
1. Plan — define hosting requirements.
2. Develop — create the HTML page and Ansible files.
3. Test — run the syntax check and verify connectivity.
4. Deploy — execute the Ansible playbook.
5. Operate — serve the page with Nginx.
6. Monitor — check Nginx status and webpage availability.

## Architecture
Developer → GitHub → Ansible control node → SSH → EC2 Ubuntu → Nginx → Browser

## Important implementation note
The inventory in this starter package uses `localhost ansible_connection=local`, matching the report's described setup where Ansible runs on the EC2 instance and configures that same instance. If you later run Ansible from a separate control machine, update the inventory and SSH settings accordingly.
