 Kubernetes Manifest Files Repository

Overview

This repository contains Kubernetes manifest (YAML) files used to deploy, configure, and manage applications and infrastructure components within a Kubernetes cluster. The manifests follow declarative configuration principles, allowing resources to be version-controlled, reviewed, and deployed consistently across environments.

Repository Contents

The repository may include manifests for:

* Namespaces
* Deployments
* Services
* ConfigMaps
* Secrets
* Ingress Resources
* Persistent Volumes (PV)
* Persistent Volume Claims (PVC)
* Service Accounts
* Roles and Role Bindings
* Horizontal Pod Autoscalers (HPA)
* Jobs and CronJobs
* Network Policies

Prerequisites

Before applying the manifests, ensure the following:

* Kubernetes cluster is available and accessible.
* `kubectl` is installed and configured.
* Appropriate permissions are granted to deploy resources.
* Required namespaces and storage classes exist (if applicable).

Deployment

Apply a specific manifest:

```
kubectl apply -f <manifest-file>.yaml
```

Apply all manifests in a directory:

```
kubectl apply -f .
```

Verify deployed resources:

```
kubectl get all
```

Check resources in a specific namespace:

```
kubectl get all -n <namespace>
```

Validation

Validate manifests before deployment:

```
kubectl apply --dry-run=client -f <manifest-file>.yaml
```

Review resource definitions:

```
kubectl describe <resource-type> <resource-name>
```

Version Control

All Kubernetes configurations are maintained as code and tracked through Git, enabling:

* Change history tracking
* Peer review through pull requests
* Rollback capability
* Environment consistency
* Infrastructure as Code (IaC) practices

Best Practices

* Use namespaces to isolate workloads.
* Avoid storing plain-text secrets in repositories.
* Validate manifests before deployment.
* Follow least-privilege access principles.
* Use labels and annotations consistently.
* Maintain environment-specific configurations separately.

Purpose

This repository serves as a centralized location for Kubernetes resource definitions, simplifying deployment, management, and maintenance of workloads across development, testing, and production environments.
