AWS Three-Tier Web Architecture Deployment
This project demonstrates the deployment of a scalable and secure three-tier web application on AWS. It features a React.js frontend, a Node.js/Express backend, and a MySQL RDS database, all orchestrated within a custom VPC.

🏗️ Architecture Overview
Presentation Tier (Frontend): React.js application hosted on Amazon S3 with static website hosting.

Application Tier (Backend): Node.js API running on an Amazon EC2 (Ubuntu/Amazon Linux) instance.

Data Tier (Database): Managed Amazon RDS (MySQL) instance for persistent data storage.

🛠️ Infrastructure & Networking
VPC Design: A custom VPC with Public and Private subnets across Availability Zones to ensure high availability.

Security Groups: Implemented a "Chain of Trust" where:

Web SG: Allows HTTP/HTTPS traffic.

App SG: Allows traffic only from the Web SG on port 8000.

DB SG: Allows traffic only from the App SG on port 3306.

Connectivity: Used an Internet Gateway (IGW) for public access and configured Route Tables for internal communication.

🚀 Key Features & DevOps Practices
Environment Security: Managed sensitive credentials (DB host, user, password) using .env files and protected them via .gitignore to prevent leaks to version control.

Process Management: Used PM2 on EC2 to ensure the Node.js backend remains operational 24/7 with auto-restart capabilities.

Automation: Deployed frontend assets to S3 using the AWS CLI s3 sync command for efficient updates.

How to Run Locally
Clone the repo:

Bash
git clone https://github.com/anand-singh02/Three-tier-Deployment.git
Configure Backend: Create a .env file in /backend with your DB_HOST, DB_USER, and DB_PASS.

Install Dependencies: Run npm install in both /frontend and /backend.

Start: Run npm start (Frontend) and node run build and npm start (Backend).

# SCREENSHOT

Testing API REST with Rest Client Extension VSCODE
![](assets/screenshot1.jpg)

App Tasks Fullstack

![](assets/screenshot2.jpg)

![](assets/screenshot3.jpg)

![](assets/screenshot4.jpg)
