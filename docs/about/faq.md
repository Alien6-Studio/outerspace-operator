---
title: FAQ - Managing Algorithms with OuterSpace Operator
description: Find answers to frequently asked questions about how to use OuterSpace Operator to manage your algorithms.
---

# Frequently Asked Questions

## What is the OuterSpace Operator?

The OuterSpace Operator is a __Kubernetes operator__ designed to simplify your algorithm deployment process. It manages deployments on various cloud platforms such as AWS, Google Cloud, Azure, and more, providing features like automated scaling, load normalization, wide algorithm support, and advanced security measures.

## How does OuterSpace Operator integrate with other systems?

OuterSpace Operator integrates seamlessly with a range of systems, including __KServe__ for serverless inferencing, __Prometheus__ for monitoring and alerting, and __Azure Active Directory__ for authentication. It can be installed using Helm, allowing for deployment and management via any CI/CD platform.

## What is Ground Control?

__Ground Control__ is a companion portal to the OuterSpace Operator. It provides a central place to visualize deployed algorithms, monitor metrics, review logs, view OpenAPI (Swagger) interface contracts, and manage Role-Based Access Control (RBAC) to algorithms.

## How does OuterSpace Operator handle security?

OuterSpace Operator prioritizes security and adheres to industry best practices. All pod communications are conducted via HTTPS, ensuring encryption in transit. Depending on the cluster configuration, it also provides encryption at rest. In addition, it integrates with Azure Active Directory for authentication and includes measures for access control to ensure data privacy.

## How can I customize OuterSpace Operator to suit my needs?

OuterSpace Operator is __fully customizable__, allowing users to tailor deployments according to their specific needs. For more details on customization, refer to the respective sections of the documentation.

## Can I use OuterSpace Operator across different cloud providers?

Yes, OuterSpace Operator is designed with multi-cloud support in mind. It manages deployments on managed or non-managed Kubernetes clusters independently of the selected cloud provider, providing you the flexibility and avoiding vendor lock-in.

## How does the automated scaling work?

The automated scaling feature of OuterSpace Operator ensures optimal resource utilization at all times. It dynamically scales your deployments up or down based on demand, ensuring cost efficiency and reliable performance during peak loads.