# AKS Security Review Checklist

Use this checklist as supporting material during an AKS security review.

* [ ] Container runs as non-root where appropriate
* [ ] `allowPrivilegeEscalation` is disabled where appropriate
* [ ] Linux capabilities are minimized
* [ ] Privileged mode is not enabled
* [ ] Host namespaces are not unnecessarily shared
* [ ] HostPath is not unnecessarily used
* [ ] Root filesystem is read-only where practical
* [ ] Images do not rely on mutable `latest` tags
* [ ] Images come from trusted registries
* [ ] Image digest pinning is considered for critical workloads
* [ ] Service accounts are appropriately configured
* [ ] RBAC follows least privilege
* [ ] Secrets are not hard-coded
* [ ] External exposure is intentional
* [ ] NetworkPolicy requirements have been considered
* [ ] Azure Workload Identity is considered where Azure resources require workload identity
