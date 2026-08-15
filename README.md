# devops-capstone-project

![Build Status](https://github.com/AceVerse-Reboot/devops-capstone-project/actions/workflows/ci-build.yaml/badge.svg)

This repository contains my submission for the **DevOps Capstone Project**, part of the IBM DevOps and Software Engineering Professional Certificate. The goal of this project is to develop an account microservice for an e-commerce platform. The service exposes a REST API that other microservices can call to create, read, update, delete, and list customer accounts.

The database model and the initial "create account" endpoint were provided as a starting point. This project adds the remaining REST API endpoints (read, update, delete, list), plans and tracks the work using GitHub Agile Planning tools, and prepares the service for containerization with Docker and deployment to Kubernetes.

## Data Model

The Account model contains the following fields:

| Name | Type | Optional |
|------|------|----------|
| id | Integer| False |
| name | String(64) | False |
| email | String(64) | False |
| address | String(256) | False |
| phone_number | String(32) | True |
| date_joined | Date | False |

## Project layout

```text
├── service         <- microservice package
│   ├── common/     <- common log and error handlers
│   ├── config.py   <- Flask configuration object
│   ├── models.py   <- code for the persistent model
│   └── routes.py   <- code for the REST API routes
├── setup.cfg       <- tools setup config
└── tests                       <- folder for all of the tests
    ├── factories.py            <- test factories
    ├── test_cli_commands.py    <- CLI tests
    ├── test_models.py          <- model unit tests
    └── test_routes.py          <- route unit tests
```

## License

Licensed under the Apache License. See [LICENSE](LICENSE)