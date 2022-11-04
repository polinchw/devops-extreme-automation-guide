# devops-extreme-automation-guide

## Description

This repo serves as a guide to fully (well, as close to fully as possible) automate building deploying your microservices.
It shows how to combine some great open source tools in a seperation of concerns manner.

This is a list of the most commonly used components involved in building and deploying apps along with links to external
repos as examples.  If you piece these compoents together you can let automation do most of the heavy lifting when it comes 
to devops automation.

## Component Parts

+ Containerize
+ Kubernetes Manifests
+ GitOps
+ AutoPilot
+ Infrastructure as Code

### Containerize

Starting with your app you'll want to package it in a way that makes it easy to deploy as a container.  This [hello-github-webhook](https://github.com/polinchw/hello-github-webhook) is a very basic python app that uses Github Actions to build and push a Docker image to Docker Hub.

### Kubernetes Manifests

After the example hello-github-webhook app is containerized we'll went to tell Kubernetes how to deploy it.  We want to place the Kubernetes manifests into a seperate git repository as a best practice to set ourselves up for the next building block of our automation (GitOps).  This [hello-github-webhook-cd](https://github.com/polinchw/hello-github-webhook-cd) repo will tell Kubernetes how to deploy the [hello-github-webhook](https://github.com/polinchw/hello-github-webhook) app.  