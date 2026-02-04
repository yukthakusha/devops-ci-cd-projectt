🚀 DevOps CI/CD Pipeline using GitHub Actions
📌 Project Overview

This project demonstrates a basic yet complete CI/CD (Continuous Integration & Continuous Deployment) pipeline using GitHub Actions.

The pipeline automatically:

Triggers on every code push

Runs CI checks on a Linux environment

Deploys the project to GitHub Pages without manual intervention

This project simulates how DevOps engineers automate build and deployment workflows in real-world software teams.

🎯 Why This Project?

In modern software development:

Manual deployments are slow and error-prone

Teams rely on automation to build, test, and deploy code

DevOps engineers create pipelines to ensure fast, reliable, and repeatable releases

This project helped me understand:

How CI/CD pipelines work end-to-end

How cloud-based automation is triggered using GitHub

How to debug real pipeline failures and permission issues

🛠️ Technologies & Tools Used

Git & GitHub – Version control and repository hosting

GitHub Actions – CI/CD automation tool

YAML – Workflow configuration language

Linux (Ubuntu Runner) – Cloud execution environment

GitHub Pages – Static site deployment

⚙️ How the CI/CD Pipeline Works
1️⃣ Trigger

The pipeline runs automatically whenever code is pushed to the main branch.

on: push

2️⃣ CI – Continuous Integration

GitHub spins up a fresh Ubuntu (Linux) virtual machine

The repository code is checked out

CI steps (like tests or checks) are executed

This ensures the code is valid before deployment.

3️⃣ CD – Continuous Deployment

The pipeline deploys the project to GitHub Pages

A live website is generated from the repository

Deployment happens automatically without manual commands

❌ Error Encountered & Debugged

During deployment, the pipeline initially failed with this error:

Permission denied to github-actions[bot]
Error 403

🔍 Why the Error Occurred

By default, GitHub Actions has read-only access to repositories.
The deployment step required write access to push files to the gh-pages branch.

✅ How the Issue Was Resolved

Updated repository settings:

Settings → Actions → General

Enabled Read and write permissions

Re-ran the workflow

This allowed the GitHub Actions bot to deploy successfully.

📚 Key Concepts Learned

CI/CD pipeline fundamentals

GitHub Actions workflow structure

YAML configuration syntax

Linux-based automation runners

Deployment automation using GitHub Pages

Debugging CI/CD permission and authentication errors

🌍 Real-World Relevance

This project reflects real DevOps practices such as:

Automated builds and deployments

Cloud-based infrastructure usage

Secure permission handling

Pipeline monitoring and debugging

The same concepts are used with tools like Jenkins, GitLab CI/CD, AWS CodePipeline, and Azure DevOps.

📈 Future Enhancements

Add automated tests

Deploy a real web application

Integrate Docker for containerized builds

Extend deployment to cloud platforms (AWS / Azure)

🏁 Conclusion

This project helped me gain hands-on DevOps experience by building and debugging a real CI/CD pipeline.
It strengthened my understanding of automation, cloud infrastructure, and deployment workflows — core skills required for DevOps and Cloud roles.
