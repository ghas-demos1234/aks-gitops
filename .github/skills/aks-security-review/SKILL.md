---

name: aks-security-review
description: Performs a detailed security review of Kubernetes workloads targeting AKS. Use when reviewing Kubernetes manifests for security vulnerabilities, insecure pod configuration, RBAC, secrets, container security, or network security.
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

# AKS Security Review Procedure

Use this skill when performing a security-focused review of Kubernetes workloads intended for AKS.

Follow this procedure:

## 1. Pod and container security

Check for:

* privileged containers
* privilege escalation
* root containers
* Linux capabilities
* hostNetwork
* hostPID
* hostIPC
* hostPath volumes
* read-only root filesystem
* container securityContext

## 2. Image security

Check:

* image tags
* use of mutable tags such as `latest`
* image provenance
* image digest pinning
* trusted registries

## 3. Identity and access

Check:

* Kubernetes service accounts
* unnecessary permissions
* RBAC
* workload identity requirements
* Azure identity integration where applicable

## 4. Secrets

Check whether:

* credentials are embedded in manifests
* Kubernetes Secrets are used appropriately
* Azure Key Vault integration should be considered

## 5. Network security

Check:

* unnecessary exposure through Services
* LoadBalancer exposure
* NetworkPolicy
* ingress/egress requirements
* public versus private exposure

## 6. Reliability-related security considerations

Identify configurations that could create operational or availability risks.

## Reporting format

For every security finding provide:

**Severity:** Critical / High / Medium / Low

**Finding:** Describe the issue.

**Why it matters:** Explain the security impact.

**Recommendation:** Explain how to remediate it.

**Example:** Provide corrected YAML where useful.

Do not report a checklist item merely because it is absent. Explain why the configuration is relevant to the workload before raising it as a finding.
