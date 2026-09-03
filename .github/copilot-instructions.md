# Repository Instructions

This repository contains Kubernetes manifests for workloads that may be deployed to Azure Kubernetes Service (AKS).

Follow these repository-wide rules for every task:

* Treat Kubernetes manifests as production-oriented configuration.
* Prefer secure-by-default Kubernetes configurations.
* When reviewing Kubernetes manifests, explain the reason behind each recommendation.
* Do not assume that a configuration is acceptable simply because Kubernetes accepts it.
* For recommendations, distinguish between Kubernetes best practices and AKS-specific recommendations.
* Do not make changes to files unless the user explicitly asks you to modify them.
* When suggesting changes, show the relevant YAML.
