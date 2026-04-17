# CloudLens K8s / OpenShift Sizing Calculator

Production resource planning calculator for Keysight CloudLens sensor deployments on Kubernetes and OpenShift clusters.

**Live calculator:** https://keysight-tech.github.io/cloudlens-sizing-calculator/

## Features

- Supports DaemonSet, Sidecar, and Hybrid deployment modes
- Platform-specific overhead (EKS, AKS, GKE, OpenShift, Rancher, self-managed)
- Traffic-tier sizing from < 500 Mbps to 40–100 Gbps
- Auto-generates ready-to-deploy artifacts:
  - Helm install command
  - `values.yaml` for version-controlled deployments
  - Sidecar container YAML for manual injection
  - OpenShift `SecurityContextConstraints` for vTap sidecar mode
- Full deployment report (Markdown + PDF) with contextual checklist

## Usage

Open the live URL above in any modern browser. All calculations run client-side — no data leaves your machine.

For offline use, clone this repo and open `index.html` directly.

## Support

Contact your Keysight Solutions Engineer.

---

© Keysight Technologies — Prepared by Brine Ketum, Solutions Engineer
