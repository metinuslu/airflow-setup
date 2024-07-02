# Airflow Docker

This repository contains a Docker Compose file for building Airflow with CeleryExecutor. It is mostly production-ready, but further investigation and implementation are needed for CI/CD and cloud connections. One of the best possible scenarios is deploying on Kubernetes/EKS or ECS (Amazon managed cluster services). To achieve this, the cloud configuration with Secrets Manager, Fargate, and ECS must be applied.

## How to Run Locally

### Install Docker:

- **For Windows:** Follow the steps outlined in the [official Docker documentation for Windows](https://docs.docker.com/desktop/install/windows-install/).
- **For macOS:** Refer to the [official Docker documentation for macOS](https://docs.docker.com/desktop/install/mac-install/).

### Install Docker Compose:

- Instructions for installing Docker Compose can be found [here](https://docs.docker.com/compose/install/).

### Run the following command to start Airflow with CeleryExecutor:

```bash
docker-compose up
