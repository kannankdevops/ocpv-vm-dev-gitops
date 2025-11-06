# OCPV VM GitOps Repository

This repository contains VM manifests for OpenShift Virtualization.

## Structure
```
.
├── base/                 # Base VM configurations
├── overlays/
│   ├── dev/             # Development environment
│   ├── staging/         # Staging environment
│   └── prod/            # Production environment
```

## Usage

Apply VM to dev environment:
```bash
kubectl apply -k overlays/dev
```

Start the VM:
```bash
virtctl start dev-vm -n dev-vms
```

Stop the VM:
```bash
virtctl stop dev-vm -n dev-vms
```
