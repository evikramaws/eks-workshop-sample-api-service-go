# boston-flask-sample-api-service-go

A sample Kubernetes service used in the demo CI/CD Pipeline module.

The Dockerfile is a build that compiles the flask application and then packages it in a minimal image that pulls from python3.6

The buildspec.yml file is used by the [AWS CodeBuild](https://aws.amazon.com/codebuild/) stage. In this file, it pulls down
kubectl, builds the container image, pushes the image to [Amazon ECR](https://aws.amazon.com/ecr/) and then deploys the change to the
[Amazon EKS Cluster](https://aws.amazon.com/eks/).

In the hello-k8s.yml file, you will find sample boston flask deployment specification

