# DevOps Capstone Project

[![CI Build](https://github.com/Nihar1604/devops-capstone-project/actions/workflows/ci-build.yaml/badge.svg)](https://github.com/Nihar1604/devops-capstone-project/actions/workflows/ci-build.yaml)

This repository contains the project implementation for the **DevOps Capstone** course, part of the **IBM DevOps and Software Engineering Professional Certificate** program.

## Accounts Microservice

A Flask REST API for creating, reading, listing, updating, and deleting customer accounts.

## Technology Stack

- Python and Flask
- SQLAlchemy
- PostgreSQL
- Nose tests and coverage
- GitHub Actions
- Docker
- Kubernetes
- Tekton

## Usage

This project contains the complete microservice code along with tests, CI/CD automation pipelines, container definitions, and Kubernetes deployment configurations.

## Development Environment

These labs are designed to be executed in the IBM Developer Skills Network Cloud IDE with OpenShift.

To initialize the environment:
```bash
source bin/setup.sh

```

This installs Python 3.9, creates a Python virtual environment, and activates it.

### Useful Commands

* **Activate virtual environment:**
```bash
source ~/venv/bin/activate

```


* **Install dependencies:**
```bash
make install

```


* **Start Postgres Docker container:**
```bash
make db

```


* **Run tests with coverage:**
```bash
nosetests

```



## Project Layout

```text
├── service         <- microservice package
│   ├── common/     <- common log and error handlers
│   ├── config.py   <- Flask configuration object
│   ├── models.py   <- code for the persistent model
│   └── routes.py   <- code for the REST API routes
├── setup.cfg       <- tools setup config
└── tests           <- folder for all tests
    ├── factories.py            <- test factories
    ├── test_cli_commands.py    <- CLI tests
    ├── test_models.py          <- model unit tests
    └── test_routes.py          <- route unit tests

```

## Data Model

The `Account` model contains the following fields:

| Name | Type | Optional |
| --- | --- | --- |
| `id` | Integer | False |
| `name` | String(64) | False |
| `email` | String(64) | False |
| `address` | String(256) | False |
| `phone_number` | String(32) | True |
| `date_joined` | Date | False |

## Author
Nihar Thalkar,Student at VIT,Pune

## License

Licensed under the Apache License. 

