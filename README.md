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

## 💻 Kubernetes Configuration Spec (`pod.yaml`)

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
<img width="1464" height="676" alt="image" src="https://github.com/user-attachments/assets/ebd596dd-5915-410a-86bf-552ce710cb38" />

---

## 🚀 Version Control & Cluster Operations Guide

These sequential execution steps inside the terminal to sync the codebase and track revisions.

### 📦 1. Repository Initialization & Initial History
These commands initialize workspace database tracker and establish first operational checkpoint save.

* Initialize a blank local Git repository inside the workspace folder:

git init

* Stage the corrected pod.yaml and new README.md files for tracking:

git add pod.yaml README.md

* Review the staging area to verify which new files are ready to be saved:

git status

* Force rename the local timeline tracking branch to the industry-standard name main:

git branch -M main
<img width="1391" height="237" alt="image" src="https://github.com/user-attachments/assets/e6123723-25b8-49f3-8d6f-d1e70c8d7ea4" />


### 📁 2. Commit History
* This saves the staged files permanently into the local Git timeline history log:
```powershell
git commit -m "feat: create nginx pod YAML manifest and add documentation"
```
### 🔗 3. Remote Cloud Synchronization
* Link the local repository to the remote public cloud repository layout:

git remote add origin https://github.com/Berenice2425/YAML-architecture-for-Kubernetes-Pod-Manifest.git

### 🔄 4. Sync Remote Changes and Push
Because the remote cloud repository contains a pre-generated file (a LICENSE), merge the separate timeline histories into one unified track before finalizing the push operation:
```powershell
git pull origin main --allow-unrelated-histories --no-edit
git push -u origin main
```
<img width="1673" height="862" alt="image" src="https://github.com/user-attachments/assets/233fb418-e59a-498d-b222-74926dfada45" />

---


## ⚠️ Essential Schema Engineering Principles

* **Immutable Whitespace Constraints**: YAML blocks rely completely on spatial offsets rather than curly brackets. Avoid typing the Tab key completely; enforce a strict structure using **2 character spaces** for child elements.
* **Declarative Manifest State**: This manifest defines the ultimate execution goals. When pushed via `kubectl apply -f pod.yaml`, Kubernetes continually drives hardware parameters to align with this configuration baseline.

  
