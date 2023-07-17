---
title: Security Guide
description: Follow our comprehensive security guide to set up OuterSpace Operator.
---

# Security Guide

The OuterSpace Operator assures end-to-end security via OAuth2 protocol. Specifically, it is designed to work seamlessly with Keycloak and Azure Active Directory (AAD). In the absence of an external authentication system configuration, the operator automatically resorts to Keycloak for authentication and identity management.

## Authentication

__End-to-end OAuth2 authentication__ is crucial for securing your deployments. By leveraging OAuth2, the OuterSpace Operator guarantees that only authenticated and authorized entities can access your algorithms. This mechanism of user authentication and authorization ensures data integrity, confidentiality, and availability across your deployments.

OAuth2 provides a standardized, widely adopted framework that handles secure access to resources. It can efficiently manage and limit third-party access without exposing user credentials. By integrating with Keycloak and Azure Active Directory (AAD), OuterSpace Operator brings the power and flexibility of industry-leading authentication platforms to protect your deployed algorithms.

### Authentication with Keycloak

By default, if no external authentication system is specified, the OuterSpace Operator will automatically pull, install, and configure Keycloak. __Keycloak__ is an open-source __Identity and Access Management (IAM)__ solution that provides added security with minimum configuration. It serves as the default identity and access manager for your deployments.

If you want to rely on Keycloak, ensure that the AAD configuration is set to disabled in the values.yaml file:

```yaml
authentication:
    keycloak: 
      enabled: true
      clientID: [CLIENT-ID]
      clientSecret: [CLIENT-SECRET]
```

By setting `keycloak: enabled: true`, Keycloak is automatically set as the authentication manager.

### Optional: Azure Active Directory (AAD) Integration

If you prefer to use AAD as your authentication system, you can integrate it by adjusting the following settings in your `values.yaml` file:

```yaml
authentication:
  aad:
    enabled: true
    tenantID: [TENANT-ID]
    clientID: [CLIENT-ID]
    clientSecret: [CLIENT-SECRET]
```

By setting `aad: enabled: true`, the Operator will use AAD for authentication instead of Keycloak.

## Encryption at transit

### Certificate Management Integration

OuterSpace Operator is also designed to work seamlessly with __Cert Manager__, an open-source Kubernetes tool that automates the management and issuance of TLS certificates.

TLS (Transport Layer Security) certificates are crucial for ensuring secure communication over the internet. When used with ingress controllers in a Kubernetes environment, these certificates allow for secure HTTPs access to your deployed algorithms.

Cert Manager aids in automating the process of issuing, renewing, and managing these certificates, removing the hassle of manual certificate management. This not only saves valuable time but also reduces the risk of downtime or security breaches due to expired or misconfigured certificates.

To enable the integration with Cert Manager, you need to configure your values.yaml file as follows:

```yaml
certManager:
  enabled: true
```

By integrating Cert Manager into your setup, OuterSpace Operator ensures that your ingress communication is secure and well managed, adding yet another layer of security and reliability to your deployments.

#### Using a Certified CA with Cert Manager

In addition to automating the management and issuance of TLS certificates, Cert Manager can also be configured to work with a certified Certificate Authority (CA). This feature allows organizations that have their own internal CA, or who prefer to use a specific CA, to integrate it into their OuterSpace Operator environment.

```yaml
certManager:
  enabled: true
  useCertifiedCA: true
  caSecretName: [CA-SECRET-NAME]
```

In this configuration, `useCertifiedCA` is set to `true` to indicate that a certified CA is being used. The `caSecretName` should be replaced with the name of the secret in your Kubernetes cluster where your CA certificate and key are stored.

Using a certified CA further enhances the security of your communications and can help to meet certain organizational policies or regulatory requirements.
