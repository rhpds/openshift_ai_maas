# rhpds.openshift_ai_maas

Ansible collection to enable RHOAI 3.4 Models-as-a-Service (MaaS) governance layer on an existing OpenShift cluster.

## Role: ocp4_workload_openshift_ai_maas

Installs prerequisite operators (Kuadrant, cert-manager, LWS), configures the MaaS gateway, deploys PostgreSQL for maas-api, patches the DataScienceCluster to enable MaaS, and optionally deploys simulator and external models.

### Requirements

- OpenShift 4.21+
- RHOAI 3.4 already installed (Phase A)
- Ansible 2.16+
- `kubernetes.core` collection

### Usage

```yaml
workloads:
  - rhpds.openshift_ai_maas.ocp4_workload_openshift_ai_maas
```

See `roles/ocp4_workload_openshift_ai_maas/defaults/main.yml` for all configurable variables.
