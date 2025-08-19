# Ansible Case Study: Apache Tomcat & Maven Setup

## 📌 Objective
Provision a production-like environment for deploying applications by automating **Apache Tomcat** and **Apache Maven** installation using **Ansible**.

---

## 🛠 Steps Performed

### 1. Setup
- Created **3 Amazon EC2 instances**:
  - 1 Ansible Controller
  - 2 Node Instances
- Installed Ansible on the controller.
- Configured SSH connectivity between controller and nodes.

### 2. Tomcat Installation Role
- Created a role `testrole` for Apache Tomcat.
- Defined tasks in `tasks/main.yml`.
- Configured handlers for Tomcat service management.
- Referenced role in the `rolesdemo.yml` playbook.
- Successfully installed and configured Tomcat on both nodes.

### 3. Maven Installation Role
- Created a role `mavenrole` for Maven installation.
- Defined tasks in `tasks/main.yml`.
- Integrated both Tomcat and Maven roles into the `rolesdemo.yml` playbook.
- Ran the playbook to install both on target nodes.

---

## ✅ Outcome
- Reduced manual setup time from **45 minutes to under 5 minutes**.  
- Roles are **reusable** and **scalable** for deploying across **5+ VMs**.  
- Enabled **CI/CD pipelines**:
  - **Maven** → for application build.  
  - **Tomcat** → for deployment target.  

---

## 🔧 Tools & Technologies
- **Ansible** (roles, playbooks, handlers)  
- **Amazon EC2** (Controller & Nodes)  
- **Apache Tomcat**  
- **Apache Maven**  

