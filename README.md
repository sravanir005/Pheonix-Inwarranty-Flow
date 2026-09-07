# Postman API Automation Integration with Github Actions #

This repository is a demonstration for POC for integrating postman tests with Github actions. The tests are written in Postman and they are executed on the VM
with the help of newman and newman-reporter-htmlextra.Github Actions will trigger the project execution on every push to the main branch.You can also execute
the project manually using workflow_dispatch. The projects runs on a scheduled time with the help of cron job.

The HTML report is archieved and kept in the artifact section for the team to download it.Along with that they can view the report directly from the github page:
https://sravanir005.github.io/Pheonix-Inwarranty-Flow/
The latest report is mailed to the team members using GMAIL SMTP.

## Testing Coverage ##
1. Happy Flow Testing
2. Negative Testing and Edge Case Testing
3. Token Testing
4. Data Driven Testing with CSV
5. Schema Validation
6. Secrets Management with Github Secrets

## Tech Stack ##
1.Postman
2.Node js 22v
3.Newman
4.Newman-Reporter-Htmlextra
5.Github Actions
6.Gmail SMTP
7.Github Pages
8.CSV for Data Driven Testing
9.AWS-EC2 instance for Self hosted github runner

## Github Pages ##
You can directly view the latest test report of the postman test at the github page link : https://sravanir005.github.io/Pheonix-Inwarranty-Flow/

## HTML Report ##
The report will be created in the newman folder
![Postman Report](https://github.com/sravanir005/Pheonix-Inwarranty-Flow/blob/static-content/newman-report.PNG)

## Project Structure ##


## How to run the project ? ##
You can run the project on your local system for that:

1. Clone the project on local system : https://github.com/sravanir005/Pheonix-Inwarranty-Flow.git
2. Install Nodejs and NPM from https://nodejs.org/en
3. Install Newman npm install -g newman
4. Install Newman-reporter-htmlextra npm install -g newman-reporter-htmlextra
5. Run the Newman Command:
             newman run 'Inwarranty-Flow Collection.postman_collection.json' \ 
            -e QA.postman_environment.json \
            -d TestData.csv \
            -r cli,htmlextra \
            --reporter-htmlextra-export ./newman/index.html








