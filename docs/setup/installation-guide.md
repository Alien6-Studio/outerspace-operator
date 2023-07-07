# Installation Guide

The OuterSpace Operator provides flexibility and options when it comes to its setup, allowing you to choose between various integrations. This guide provides an overview of how to install the OuterSpace Operator, along with some customizable options like the choice of database, queuing system, security options and monitoring.

## Prerequisites

Before you proceed with the installation, make sure you have the following:

1. A Kubernetes cluster, such as Google Kubernetes Engine (GKE), Azure Kubernetes Service (AKS), or Amazon Elastic Kubernetes Service (EKS).
2. Helm installed on your workstation,
3. An access to the OuterSpace Operator Helm Chart Repository.

## Installation Steps

Here are the general steps to install the OuterSpace Operator using Helm:

1. __Preparation__: Make sure you have Helm installed on your workstation. You'll also need to have the OuterSpace Operator Helm chart ready. From our OuterSpace Operator Helm Chart Repository, download or clone the OuterSpace Operator Helm chart to your local system.

2. __Configuration__: Edit the `values.yaml` file according to your needs. This includes configuration for the database, auth2, and monitoring.

3. __Deploy the Helm Chart__: Once the `values.yaml` file is configured as per your needs, deploy the Helm chart:

    ```bash
    helm install [RELEASE_NAME] [CHART] --values [VALUES_FILE]
    ```

    !!! warning "Warning"
        Replace [RELEASE_NAME] with the name you want to assign to your deployment, [CHART] with the path to your OuterSpace Operator Helm chart, and [VALUES_FILE] with the path to your updated values.yaml file.

4. __Verify the Installation__: After the Helm chart is deployed, verify that all components are running as expected:

    ```bash
    kubectl get pods
    ```
