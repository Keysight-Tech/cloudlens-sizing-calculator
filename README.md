# CloudLens Sizing Suite

Keysight CloudLens sensor resource planning calculators for production deployments across Kubernetes, bare-metal VMs, and VMware environments.

## Live Calculators

| Calculator | URL | Status |
|---|---|---|
| **K8s / OpenShift** | https://keysight-tech.github.io/cloudlens-sizing-calculator/ | v3.2 — Live |
| **VM Sensor** (bare-metal / hypervisor tap agents) | https://keysight-tech.github.io/cloudlens-sizing-calculator/vm/ | v1.0 — Live |
| **sVM (VMware)** (per-host service VM with KVO + CLM BOM + license math) | https://keysight-tech.github.io/cloudlens-sizing-calculator/svm/ | v1.0 — Live |

## What each calculator produces

### K8s / OpenShift Calculator
- **Helm install command** — exact `helm install ...` with all `--set` flags
- **values.yaml** — version-controlled alternative to inline flags
- **Sidecar YAML** — inline container spec for CloudLens vTap sidecar injection
- **OpenShift SCC** — SecurityContextConstraints for sidecar capabilities
- **Full Markdown report** — scenario + all artifacts + deployment checklist

### VM Sensor Calculator
- **Install command** — RPM / DEB / MSI / tarball based on OS
- **sensor.conf** — configuration file with CLMS connection
- **Ansible playbook** — fleet-scale deployment automation
- **Pre-flight script** — validates kernel headers, mirror interface, CLMS reachability, disk space, SELinux
- **Full Markdown report** — scenario + all artifacts + deployment checklist

### sVM (VMware) Calculator
- **Multi-site support** — add per-data-center cards with independent ESXi host count, throughput, vSphere version, tap method
- **Full-stack BOM** — KVO + CLM (per site or shared) + sVM-per-host sizing
- **Editable tier defaults** — 7 per-host throughput tiers with SBI-anchored defaults; every cell overrideable with Keysight PS values
- **License pack math** — auto-compute `LIC-CL-VTAP-10` and `LIC-CL-VTAP-100` recommendations
- **Markdown BOM** — 8 sections: executive summary, per-site sizing, component BOM, license requirements, network requirements, deployment checklist, risks, rollback
- **CSV for SOW** — per-component rows, ready to drop into Keysight SOW templates
- **Print to PDF** — clean one-page customer-facing summary

## Features common to all calculators

- Traffic-tier sizing from < 500 Mbps to 40–100 Gbps
- Platform-specific overhead multipliers (EKS, AKS, GKE, OpenShift, ESXi, KVM, etc.)
- Per-node/VM footprint + fleet-wide totals
- Verdict badges based on cluster overhead %
- Keysight-branded UI with print-to-PDF support
- Copy + Download buttons for every generated artifact
- Runs 100% client-side — zero data leaves the browser

## Usage

Open the live URL for the deployment mode you're planning. All calculations run in your browser. No sign-up, no tracking, no data egress.

For offline use, clone this repo and open `index.html` (or `vm/index.html`) directly.

## Support

Contact your Keysight Solutions Engineer.

---

© Keysight Technologies — Prepared by Brine Ketum, Solutions Engineer
