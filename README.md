# lab10-terraform-canary-release
Terraform-based CI/CD Canary Deployment Lab - Create and deploy an EC2 instance using Infrastructure as Code.
Lab 10: CI/CD Pipeline with Canary Releases

## 🔍 Project Title
**Lab 10: CI/CD Pipeline with Canary Releases using Terraform and GitHub Actions**

## 🎯 Aim
To implement a CI/CD pipeline that automates the provisioning and deployment of a canary release using Terraform and GitHub Actions on AWS.

## 🎯 Objectives
- Provision an EC2 instance with a canary deployment label.
- Define infrastructure-as-code using Terraform.
- Automate provisioning via GitHub Actions workflows.
- Validate EC2 creation and tag association.
- Document the CI/CD workflow visually and narratively.

## 🧰 Tools Used
- **Terraform** – For Infrastructure as Code (IaC) provisioning.
- **GitHub Actions** – For CI/CD automation workflow.
- **AWS EC2** – Compute service used for launching the canary instance.
- **Git Bash / VS Code Terminal** – CLI for Terraform operations.
- **Visual Studio Code (VS Code)** – Development environment.
- **GitHub** – Source code and pipeline host.

## 🔧 Configuration Summary
- Region: `eu-west-1`
- EC2 Instance Type: `t2.micro`
- AMI ID: `ami-061fa58ed1b23b2a7`
- Tag: `"canary-instance"`

## 📦 Files in Project
- `main.tf`: Terraform code to deploy EC2 instance.
- `.github/workflows/deploy.yml`: GitHub Actions workflow.
- `terraform.tfstate`: Terraform state file.
- `README.md`: This documentation.

## 📸 Screenshot Documentation
A total of **27 screenshots** were taken from the start to completion of the lab. These include:
- GitHub Actions setup
- Git clone, commit, and push to trigger workflow
- Terraform init, plan, and apply outputs
- Successful EC2 instance creation
- Validation of AMI and region
- GitHub repo setup and pipeline logs

## 🚀 Implementation Strategy
1. Create the Terraform code (`main.tf`) to define AWS resources.
2. Choose the correct AMI ID for the target region.
3. Create a GitHub Actions workflow under `.github/workflows/deploy.yml`.
4. Connect local repo to GitHub.
5. Run Terraform commands: `init`, `plan`, `apply`.
6. Monitor provisioning logs and pipeline output.
7. Verify resource creation on AWS Management Console.
8. Upload project folder and screenshots to GitHub.

## ✅ Results
- Terraform successfully created a tagged EC2 instance.
- AMI compatibility issue was resolved by selecting a valid `ami-061fa58ed1b23b2a7`.
- GitHub Actions workflow was prepared but not triggered due to manual apply.
- Screenshots verified successful resource creation.

## 📘 Lessons Learned
- AMI IDs must match the target AWS region.
- Always verify region-AMI compatibility before `terraform apply`.
- GitHub Actions workflow structure matters: syntax errors silently fail.
- Terraform state management is crucial for reproducibility.

## ⚠️ Limitations
- Manual AMI ID validation needed.
- GitHub Actions was not triggered automatically—manual apply was used.
- Lack of custom user_data or server provisioning script.

## 🧠 How to Overcome Limitations
- Implement AMI data sources with filtering in Terraform to auto-select AMIs.
- Push commits with workflow triggers on main branch.
- Extend Terraform file with security groups, key pairs, and provisioning.

## 💡 Significance of Lab
This lab introduces core DevOps CI/CD concepts, allowing for:
- Safer deployments via Canary strategy
- Infrastructure version control
- Reproducibility of cloud resources
- Clean separation of code and infra

## 📂 GitHub Repo Naming Suggestion
`lab10-ci-cd-canary-pipeline`

## 👨‍💻 Author
**Ime Ben**  
GitHub: [ime-cloud-sec-analyst](https://github.com/ime-cloud-sec-analyst)  
AWS DevSecOps | Terraform | Cloud Security | CI/CD | Infrastructure as Code

---

📌 **Most-Do in Labs**:
- Always validate AMI/region compatibility
- Use `terraform plan` before applying
- Document with screenshots
- Commit and push regularly to version control

