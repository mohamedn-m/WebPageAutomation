Selenium Java Automation Script for Daily Monitoring

Overview
This repository contains a Selenium Java automation script designed for daily monitoring of broken links and images on a website. The script is configured to run on GitHub servers using GitHub Actions based on a scheduled cron time. The results are generated as an Excel report (.xlsx), providing detailed insights into the website's health.

Features
Broken Link Detection: Verifies the accessibility of all website links.
Image Validation: Ensures all images on the website load correctly.
Daily Monitoring: Scheduled to run automatically using GitHub Actions.
Report Generation: Outputs the results in an easy-to-read Excel file.

Requirements
No local setup is required. The script runs directly on GitHub servers.

GitHub Actions Setup
The automation script is configured to run using a GitHub Actions workflow:
                  a. Scheduled using cron syntax in yml file to execute daily. 
                  b. Leverages GitHub-hosted runners for execution.

Workflow File
The workflow file (.github/workflows/monitoring.yml) is already included in the repository. It specifies:

The schedule for running the script.
The environment setup.
The execution steps for the script.
Cron Schedule
The script runs daily at the configured time using the cron schedule. For example:
on:  
  schedule:  
     - cron: "30 0 * * *"  # 12:30 AM UTC -> 6:00 AM IST
    
Output
Excel Report: After the script runs, the Excel report is generated and saved as an artifact in the workflow.

Report Details:
URL: The link or image URL checked.
Status: Functional or broken.
Response Code: HTTP response code for links.
Timestamp: When the check was performed.

How to Use
Clone this repository to your GitHub account.
The workflow will automatically trigger at the scheduled time.
Download the Excel report from the workflow artifacts after the execution.(Note: You need to configure the necessary permissions.)

Contributing
Contributions are welcome! Fork the repository, make changes, and submit a pull request.

Contact
For questions or support, reach out via my email id(rihanfaris777@gmail.com).
                                                                                  

