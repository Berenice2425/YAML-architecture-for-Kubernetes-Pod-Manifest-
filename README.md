# YAML Architecture for Kubernetes Pod Manifest

This project provides a native, declarative Infrastructure-as-Code (IaC) configuration manifest to deploy a high-performance Nginx web server pod instance inside an active Kubernetes cluster node runtime environment.

---

## 📁 Repository Project Structure

```text
yaml-architecture/
├── .git/               # Initialized local Git version tracking database
├── README.md           # Deployment manual and workspace architecture guide
└── pod.yaml            # Fixed structural declarative Kubernetes manifest
```

---

## 💻 Extracted Kubernetes Configuration Spec (`pod.yaml`)

The verified, structurally accurate schema optimized to interface directly with the Kubernetes API Control Plane:

```yaml
apiVersion: v1
kind: Pod
metadata:
  name: nginx-pod          # Globally unique identifier within the cluster namespace
spec:
  containers:
  - name: nginx            # Isolated operational logic name tag
    image: nginx:latest    # Image target pulling from the container hub registry
```

---

## 🚀 Version Control & Cluster Operations Guide

Follow these sequential execution steps inside your terminal to sync your codebase and track revisions.

### 1. Update and Stage Files
Track the corrected configurations inside your staging area workspace:
```powershell
git add pod.yaml README.md
```

### 2. Record Revision Commit History
Save your localized workspace changes cleanly into your root historical branch line:
```powershell
git commit -m "fix: resolve metadata structure indentation and add README documentation"
```

### 3. Sync Remote Changes and Push
Because your remote cloud repository contains a pre-generated file (like a LICENSE), merge the separate timeline histories into one unified track before finalizing the push operation:
```powershell
git pull origin main --allow-unrelated-histories --no-edit
git push -u origin main
```

---

## ⚠️ Essential Schema Engineering Principles

* **Immutable Whitespace Constraints**: YAML blocks rely completely on spatial offsets rather than curly brackets. Avoid typing the Tab key completely; enforce a strict structure using **2 character spaces** for child elements.
* **Declarative Manifest State**: This manifest defines the ultimate execution goals. When pushed via `kubectl apply -f pod.yaml`, Kubernetes continually drives hardware parameters to align with this configuration baseline.
