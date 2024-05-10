# Ansible-Infrastructure-Setup-for-Jenkins-Nexus-and-Nginx 🛠️
## 📝 Overview
This Ansible project automates the setup of Jenkins, Nexus, and Nginx on localhost as well as on AWS instances. It includes playbooks for installing Jenkins and Nexus on localhost, creating two AWS instances (one with Nexus and another with Jenkins), installing Nginx on one of the instances, configuring Nginx to redirect to Jenkins using only the IP, creating DNS entries in /etc/hosts, and creating self-signed certificates for enabling HTTPS.

## 🚀 Features
1. **Install Jenkins on localhost:**
   - Playbook to install Jenkins on localhost.
2. **Install Nexus on localhost:**
   - Playbook to install Nexus on localhost.
3. **Setup AWS Instances:**
   - Create two AWS instances (one with Nexus and another with Jenkins) in aws console.
4. **Install Nginx on AWS Instance:**
   - Playbook to install Nginx on one of the AWS instances.
5. **Configure Nginx to Redirect to Jenkins:**
   - Modify Nginx configuration to redirect to Jenkins using only the IP.
6. **Create DNS Entries in /etc/hosts:**
   - Create DNS entries in /etc/hosts for easy access and configure it in nginx.
7. **Create Self-Signed Certificates for HTTPS:**
   - Create self-signed certificates for enabling HTTPS.

## 📁 Directory Structure
- **jenkins-role/:** Ansible role for Jenkins setup.
- **nexus-role/:** Ansible role for Nexus setup.
- **nginx-role/:** Ansible role for Nginx setup.
- **install_services.yml:** Main playbook for installing services.
- **inventory/:** Inventory file for defining hosts.

## 💻 Usage
1. Clone the repository:
   ```
   git clone https://github.com/Nada-Khater/Ansible-Infrastructure-Setup-for-Jenkins-Nexus-and-Nginx.git
   ```
   ```
   cd Ansible-Infrastructure-Setup-for-Jenkins-Nexus-and-Nginx
   ```
2. Update the inventory file with your AWS instance IPs.
3. Run the main playbook to install services:
   ```
   ansible-playbook -i inventory --private-key ~/path_to_your_key.pem install_services.yml
   ```
4. Access Jenkins using the IP address of the Nginx instance in your browser.

## 📹 Demo
https://github.com/Nada-Khater/Ansible-Infrastructure-Setup-for-Jenkins-Nexus-and-Nginx/assets/75952748/434783f2-2c95-4bb1-8c69-b29b0234111d

