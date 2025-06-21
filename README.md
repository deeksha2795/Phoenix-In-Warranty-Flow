# Postman API Automation Integration with Github Actions #

This repository is a demonstration for POC for integrating postman tests with github actions.The Tests are written is Postman and they are executed on the VM with the help of newman and newman-reporter-htmlextra.
Github Actions will trigger the project execution on every push on the main branch.You can also execute the project manually using workflow_dispatch.The project runs on a scheduled time with the help of the cron job.

The HTML reports is archieved and kept in the artifact section for the team to download it.Along with that they can viw the reports directly from the github page : https://deeksha2795.github.io/Phoenix-In-Warranty-Flow/
The latest reports are mailed to the team members using GMAIL SMTP.

## Testing Coverage ##
1. Happy Flow Testing
2. Negative Testing and Edge Case Testing
3. Data driven Testing using CSV
4. Token Testing
5. Schema Validation
6. Secrets Management with Github Secrets

## Tech Stack ##
1. Postman
2. Node js 22v
3. Newman
4. Newman-Reporter-Htmlextra
5. Github Actions
6. GMAIL SMTP
7. Github Pages
8. CSV for Data Driven Testing
9. AWS EC2 instance for Self Hosted Github Runner

## Github Pages ##
You can directly view the reports from the github pages : https://deeksha2795.github.io/Phoenix-In-Warranty-Flow/

## HTML Reports ##
The report will be created in the newman folder

![Postman Report](https://github.com/deeksha2795/Phoenix-In-Warranty-Flow/blob/Static-Content/Newman%20Test%20Report.png)

## Project Structure ##
```
Postman Module
└─ Phoenix InWarranty-Flow
   ├─ In-Warranty Flow Collection.postman_collection.json # Collection File
   ├─ newman # HTML Report Folder
   │  └─ In-Warranty Flow Collection-2025-06-18-10-04-59-491-0.html
   ├─ QA.postman_environment.json # Environment File
   └─ testData.csv # Test Data File

```
## How to run the Project? ##
You can run the project on your local systyem, following are the steps :
1. Clone the project on your Local System : https://github.com/deeksha2795/Phoenix-In-Warranty-Flow.git
2. Instal Node js and npm : https://nodejs.org/en
3. Install newman : ```npm install -g newman```
4. Install newman-reporter-htmlextra : ```npm install -g newman-reporter-htmlextra```
5. Run the Newman Command :
   
             newman run 'In-Warranty Flow Collection.postman_collection.json' \
                -e QA.postman_environment.json \
                -d testData.csv \
                -r cli,htmlextra \
                --reporter-htmlextra-export ./newman/index.html



