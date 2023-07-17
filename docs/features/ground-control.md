---
title: Ground Control
description: Discover Ground Control, our UI console designed to manage and monitor your algorithm deployments on kubernetes.
---

# Ground Control

In concert with the OuterSpace Operator, __Ground Control__ allows you to easily manage and monitor your deployments, whether they are large or small, simple or complex. From individual algorithm deployments to orchestrating entire fleets of algorithm pods, Ground Control and OuterSpace Operator make the process easier and more efficient.

`Dashboard & Metrics`
:   Upon logging into Ground Control, you're greeted with a comprehensive dashboard. This interface provides a real-time overview of the algorithms deployed on the cluster. It includes a variety of dedicated metrics for each algorithm, giving you insights into their performance, resource utilization, and other crucial factors.

    Each algorithm's metrics are presented in an intuitive, user-friendly format, making it easy to understand the current state of your deployments at a glance.

`Log Management`

:   Efficient log management is critical for monitoring your deployments and troubleshooting potential issues. Ground Control provides a dedicated section for viewing, managing and downloading the logs of each deployed algorithm.

    Logs can be filtered based on time, algorithm, pods, severity, or any custom parameters you define, making it simple to drill down to the information you need. You can request logs using __Prometheus queries__, and Ground Control will display the results in a user-friendly format.

`OpenAPI Interface Contracts`

:   For each algorithm deployed on your cluster, Ground Control provides an easy way to view its __OpenAPI (Swagger) interface contracts__. OpenAPI contracts are an essential part of modern API development, offering a clear, standard format for describing your API.

    This feature allows you to check the details of each algorithm's API, such as endpoints, request/response types, status codes, and more, enhancing your understanding and management of your deployed algorithms. It helps Data Scientists and Data Engineers to experiment with the algorithms and test them before deploying them in production.

`Role-Based Access Control (RBAC)`

:   Security and access control are crucial in any system. Ground Control includes a feature to manage __RBAC__ for each algorithm, providing you with granular control over who can access what.

    From Ground Control, you can create teams, assign roles and permissions to different users, ensuring they only have access to the algorithms and features they need. This helps to maintain security, minimize the risk of accidental disruption, and comply with any internal or regulatory requirements.
