# JFrog CLI Docker Images

This repository contains custom Docker images integrating [JFrog CLI](https://jfrog.com/getcli/) with various build tools: Maven, Helm, Node.js, and Terraform.

## Available Images

- **Maven**: `maven/Dockerfile`  
  Includes Maven 3.9.9, JFrog CLI 2.77.0, Java Temurin 21, based on Alpine.
  To pull the associated container image: `docker pull ehmd96/jfrog-cli-maven:jfcli-full-2.77.0_mvn-3.9.9-temurin-21-alpine`

- **Helm**: `helm/Dockerfile`  
  Includes Helm 3.14.4, JFrog CLI 2.77.0, based on Alpine.
  To pull the associated container image: `docker pull ehmd96/jfrog-cli-helm:jfcli-full-2.77.0_alpine-helm-3.14.4`

- **Node.js**: `node/Dockerfile`  
  Includes Node.js 24.3.0, JFrog CLI 2.77.0, based on Alpine.
  To pull the associated container image: `docker pull ehmd96/jfrog-cli-node:jfcli-full-2.77.0_node-24.3.0-alpine`

- **Terraform**: `terraform/Dockerfile`  
  Includes Terraform 1.12.2, JFrog CLI 2.77.0.
  To pull the associated container image: `docker pull ehmd96/jfrog-cli-terraform:jfcli-full-2.77.0_hashicorp-terraform-1.12.2`