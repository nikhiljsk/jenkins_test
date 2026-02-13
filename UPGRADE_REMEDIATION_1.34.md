# Kubernetes 1.34 Upgrade - Field-Level Remediation Report

## Cluster: court7ud0bmnf3uar520
## Generated: 2026-02-13 09:28:24
## Risk Level: Medium
## Risk Score: 39.9%

---

## Summary
- **Total Issues Found:** 26
- **Blocking Issues:** 5
- **Error Issues:** 12
- **Warning Issues:** 9

---

## Detailed Findings

### ERROR: DaemonSet/calico-node
- **Rule:** Probe Host Field Restricted
- **Message:** Probe host field restricted in PSS: template.calico-node.livenessProbe.httpGet.host
- **Remediation:** Remove the .host field from probe configurations, or ensure namespace allows 'privileged' PSS

### BLOCK: DaemonSet/test-nikhiljsk-portworx
- **Rule:** Portworx Not Supported
- **Message:** Portworx component detected: test-nikhiljsk-portworx
- **Remediation:** Remove Portworx before upgrading to 1.34, or wait for Portworx 1.34 support

### ERROR: Pod/calico-node-rwfw7
- **Rule:** Probe Host Field Restricted
- **Message:** Probe host field restricted in PSS: calico-node.livenessProbe.httpGet.host
- **Remediation:** Remove the .host field from probe configurations, or ensure namespace allows 'privileged' PSS

### ERROR: Pod/calico-node-v55nf
- **Rule:** Probe Host Field Restricted
- **Message:** Probe host field restricted in PSS: calico-node.livenessProbe.httpGet.host
- **Remediation:** Remove the .host field from probe configurations, or ensure namespace allows 'privileged' PSS

### ERROR: Pod/calico-node-xklxr
- **Rule:** Probe Host Field Restricted
- **Message:** Probe host field restricted in PSS: calico-node.livenessProbe.httpGet.host
- **Remediation:** Remove the .host field from probe configurations, or ensure namespace allows 'privileged' PSS

### ERROR: Pod/calico-typha-7f6df5968d-k5f6b
- **Rule:** Probe Host Field Restricted
- **Message:** Probe host field restricted in PSS: calico-typha.livenessProbe.httpGet.host, calico-typha.readinessProbe.httpGet.host
- **Remediation:** Remove the .host field from probe configurations, or ensure namespace allows 'privileged' PSS

### ERROR: Pod/calico-typha-7f6df5968d-lgff7
- **Rule:** Probe Host Field Restricted
- **Message:** Probe host field restricted in PSS: calico-typha.livenessProbe.httpGet.host, calico-typha.readinessProbe.httpGet.host
- **Remediation:** Remove the .host field from probe configurations, or ensure namespace allows 'privileged' PSS

### WARNING: Pod/test-nikhiljsk-apparmor-deploy-c765dd586-45jfs
- **Rule:** AppArmor Annotation Deprecated
- **Message:** Uses deprecated AppArmor annotations: container.apparmor.security.beta.kubernetes.io/nginx
- **Remediation:** Use securityContext.appArmorProfile instead of the deprecated annotation

### WARNING: Pod/test-nikhiljsk-apparmor-pod
- **Rule:** AppArmor Annotation Deprecated
- **Message:** Uses deprecated AppArmor annotations: container.apparmor.security.beta.kubernetes.io/test-container
- **Remediation:** Use securityContext.appArmorProfile instead of the deprecated annotation

### ERROR: Pod/test-nikhiljsk-liveness-host
- **Rule:** Probe Host Field Restricted
- **Message:** Probe host field restricted in PSS: nginx.livenessProbe.httpGet.host
- **Remediation:** Remove the .host field from probe configurations, or ensure namespace allows 'privileged' PSS

### WARNING: Pod/test-nikhiljsk-matchlabelkeys-8695c7f64d-z6cfv
- **Rule:** matchLabelKeys in TopologySpreadConstraints
- **Message:** Uses matchLabelKeys in topologySpreadConstraints - verify upgrade path
- **Remediation:** Ensure upgrade path is 1.32→1.33→1.34. Controllers can now use labelSelector directly.

### ERROR: Pod/test-nikhiljsk-readiness-host
- **Rule:** Probe Host Field Restricted
- **Message:** Probe host field restricted in PSS: nginx.readinessProbe.httpGet.host
- **Remediation:** Remove the .host field from probe configurations, or ensure namespace allows 'privileged' PSS

### ERROR: ReplicaSet/calico-typha-6bd4bccdc8
- **Rule:** Probe Host Field Restricted
- **Message:** Probe host field restricted in PSS: template.calico-typha.livenessProbe.httpGet.host, template.calico-typha.readinessProbe.httpGet.host
- **Remediation:** Remove the .host field from probe configurations, or ensure namespace allows 'privileged' PSS

### ERROR: ReplicaSet/calico-typha-6c9f6886f5
- **Rule:** Probe Host Field Restricted
- **Message:** Probe host field restricted in PSS: template.calico-typha.livenessProbe.httpGet.host, template.calico-typha.readinessProbe.httpGet.host
- **Remediation:** Remove the .host field from probe configurations, or ensure namespace allows 'privileged' PSS

### ERROR: ReplicaSet/calico-typha-7f6df5968d
- **Rule:** Probe Host Field Restricted
- **Message:** Probe host field restricted in PSS: template.calico-typha.livenessProbe.httpGet.host, template.calico-typha.readinessProbe.httpGet.host
- **Remediation:** Remove the .host field from probe configurations, or ensure namespace allows 'privileged' PSS

### WARNING: ReplicaSet/test-nikhiljsk-apparmor-deploy-c765dd586
- **Rule:** AppArmor Annotation Deprecated
- **Message:** Uses deprecated AppArmor annotations: template.container.apparmor.security.beta.kubernetes.io/nginx
- **Remediation:** Use securityContext.appArmorProfile instead of the deprecated annotation

### WARNING: ReplicaSet/test-nikhiljsk-matchlabelkeys-8695c7f64d
- **Rule:** matchLabelKeys in TopologySpreadConstraints
- **Message:** Uses matchLabelKeys in topologySpreadConstraints - verify upgrade path
- **Remediation:** Ensure upgrade path is 1.32→1.33→1.34. Controllers can now use labelSelector directly.

### ERROR: Deployment/calico-typha
- **Rule:** Probe Host Field Restricted
- **Message:** Probe host field restricted in PSS: template.calico-typha.livenessProbe.httpGet.host, template.calico-typha.readinessProbe.httpGet.host
- **Remediation:** Remove the .host field from probe configurations, or ensure namespace allows 'privileged' PSS

### WARNING: Deployment/test-nikhiljsk-apparmor-deploy
- **Rule:** AppArmor Annotation Deprecated
- **Message:** Uses deprecated AppArmor annotations: template.container.apparmor.security.beta.kubernetes.io/nginx
- **Remediation:** Use securityContext.appArmorProfile instead of the deprecated annotation

### BLOCK: Deployment/test-nikhiljsk-cluster-autoscaler
- **Rule:** Cluster Autoscaler Not Supported
- **Message:** Cluster Autoscaler component detected: test-nikhiljsk-cluster-autoscaler
- **Remediation:** Remove or disable Cluster Autoscaler before upgrading to 1.34, or wait for support

### BLOCK: Deployment/test-nikhiljsk-istio-ingress
- **Rule:** Istio 1.25 Not Supported
- **Message:** Istio version 1.25.0 not supported on IKS 1.34
- **Remediation:** Upgrade Istio to 1.26+ or migrate to community Istio before upgrading the cluster

### BLOCK: Deployment/test-nikhiljsk-istiod
- **Rule:** Istio 1.25 Not Supported
- **Message:** Istio version 1.25.0 not supported on IKS 1.34
- **Remediation:** Upgrade Istio to 1.26+ or migrate to community Istio before upgrading the cluster

### WARNING: Deployment/test-nikhiljsk-matchlabelkeys
- **Rule:** matchLabelKeys in TopologySpreadConstraints
- **Message:** Uses matchLabelKeys in topologySpreadConstraints - verify upgrade path
- **Remediation:** Ensure upgrade path is 1.32→1.33→1.34. Controllers can now use labelSelector directly.

### BLOCK: Deployment/test-nikhiljsk-portworx-api
- **Rule:** Portworx Not Supported
- **Message:** Portworx component detected: test-nikhiljsk-portworx-api
- **Remediation:** Remove Portworx before upgrading to 1.34, or wait for Portworx 1.34 support

### WARNING: Service/test-nikhiljsk-traffic-clusterip
- **Rule:** PreferClose Traffic Distribution Deprecated
- **Message:** Service uses deprecated trafficDistribution=PreferClose
- **Remediation:** Change trafficDistribution from 'PreferClose' to 'PreferSameZone' or 'PreferSameNode'

### WARNING: Service/test-nikhiljsk-traffic-nodeport
- **Rule:** PreferClose Traffic Distribution Deprecated
- **Message:** Service uses deprecated trafficDistribution=PreferClose
- **Remediation:** Change trafficDistribution from 'PreferClose' to 'PreferSameZone' or 'PreferSameNode'

