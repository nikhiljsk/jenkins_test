# Kubernetes 1.34 Upgrade - Field-Level Remediation Report

## Cluster: court7ud0bmnf3uar520
## Generated: 2026-02-13 08:36:12
## Risk Level: Medium
## Risk Score: 37.5%

---

## Summary
- **Total Issues Found:** 10
- **Blocking Issues:** 0
- **Error Issues:** 10
- **Warning Issues:** 0

---

## Detailed Findings

### ERROR: DaemonSet/calico-node
- **Rule:** Probe Host Field Restricted
- **Message:** Probe host field restricted in PSS: template.calico-node.livenessProbe.httpGet.host
- **Remediation:** Remove the .host field from probe configurations, or ensure namespace allows 'privileged' PSS

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

### ERROR: Deployment/calico-typha
- **Rule:** Probe Host Field Restricted
- **Message:** Probe host field restricted in PSS: template.calico-typha.livenessProbe.httpGet.host, template.calico-typha.readinessProbe.httpGet.host
- **Remediation:** Remove the .host field from probe configurations, or ensure namespace allows 'privileged' PSS

