# Cloud-Native Application Development with Kubernetes

**Student Lab Manifest Pack**  
Course duration: **15 hours / 3 days**  
Delivery mode: **Concept + Imperative command + Declarative manifest + Guided lab + Mini project**

This package contains ready-to-use Kubernetes manifests for the Vel Tech Kubernetes Application Development training.

## Folder Structure

```text
k8s-student-labs/
├── 00-setup/
├── day1-foundations/
├── day2-deploy-config-service/
├── day3-troubleshooting-storage/
├── mini-project-student-portal/
└── trainer-reference/
```

## Standard Lab Flow

For every major Kubernetes resource, use this pattern:

```text
1. Understand the concept
2. Try imperative command
3. Observe output
4. Generate YAML using --dry-run=client -o yaml
5. Apply declarative YAML
6. Troubleshoot and validate
```

## Prerequisites

Students should have:

- minikube
- Docker
- kubectl
- VS Code
- Git
- Browser

## Quick Start

```bash
kubectl version --client
kubectl get nodes
kubectl apply -f 00-setup/namespace.yaml
kubectl config set-context --current --namespace=student-lab
```

## Clean Up All Lab Resources

```bash
kubectl delete namespace student-lab --ignore-not-found=true
kubectl delete namespace student-portal --ignore-not-found=true
```


## Validation and Solutions

This updated package includes:

- `00-setup/validate-yaml-python.py` for offline YAML syntax checks
- `00-setup/validate-kubectl-client-dryrun.sh` for kubectl client-side validation
- `00-setup/validate-kubectl-server-dryrun.sh` for live cluster schema/admission validation
- `00-setup/validation-guide.md` for validation workflow
- `solutions/` folder with answer keys and mini project complete solution

Recommended validation before class:

```bash
python 00-setup/validate-yaml-python.py
bash 00-setup/validate-kubectl-client-dryrun.sh day1-foundations
bash 00-setup/validate-kubectl-client-dryrun.sh day2-deploy-config-service
bash 00-setup/validate-kubectl-client-dryrun.sh day3-troubleshooting-storage
bash 00-setup/validate-kubectl-client-dryrun.sh mini-project-student-portal
```
