# Terraform + Ansible Project: Apache Setup on AWS EC2

This is a beginner-friendly DevOps project that uses **Terraform** to provision an EC2 instance on AWS and **Ansible** to configure Apache web server on it.

---

## Project Structure

- `terraform/` — contains files to provision EC2 instance.
- `ansible/` — contains Ansible inventory and playbook for Apache setup.

---

## Tools Used

- **Terraform**: To create AWS infrastructure (EC2 instance).
- **Ansible**: To install and configure Apache server.
- **AWS EC2**: Ubuntu-based instance used for deployment.
- **MobaXterm**: SSH terminal to connect to EC2.

---

## How It Works

1. **Terraform** provisions a new EC2 instance on AWS.
2. You SSH into the EC2 instance using the `.pem` key.
3. **Ansible** installs Apache and starts the service.
4. You visit the EC2 public IP and see **“Hello from Ansible!”** in the browser.

---

## How to Run the Project

### Step 1: Terraform — Provision the EC2 Instance

```bash
cd terraform
terraform init
terraform apply

### step 2: Connect to instance with public IP address

ssh -i key.pem ubuntu@<your-ec2-public-ip>



### step 3: Ansible Apache Setup

## Files
- `inventory` – Contains the IP of the EC2 instance.
- `playbook.yml` – Ansible playbook that installs and starts Apache.


```bash
ansible-playbook -i inventory playbook.yml

### step 4: open browser

http:/// <IP>
