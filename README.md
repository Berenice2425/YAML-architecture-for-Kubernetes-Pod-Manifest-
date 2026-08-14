# YAML Architecture for Kubernetes Pod Manifest

This project provides a native, declarative Infrastructure-as-Code (IaC) configuration manifest to deploy a high-performance Nginx web server pod instance inside an active Kubernetes cluster node runtime environment.

---

## 💻 Kubernetes Configuration Spec (`pod.yaml`)

This schema  is optimized to interface directly with the Kubernetes API Control Plane:

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
<img width="1458" height="593" alt="image" src="https://github.com/user-attachments/assets/f96034cc-80b0-447a-9f46-edf30980b84b" />


---

## Basic Concepts Treated
*1. API Version*

  ```yaml
apiVersion: v1
```

<img width="287" height="69" alt="image" src="https://github.com/user-attachments/assets/bef2a4d1-a0de-43d2-870f-8bde4ab01718" />




*2. Resource Type*  

```yaml
kind: Pod
```
  
<img width="299" height="101" alt="image" src="https://github.com/user-attachments/assets/4cd4e40b-ba2a-4c05-aa28-4ec607996ac4" />




*3. parent- child structure*

```yaml
metadata:
  name: nginx-pod          # Globally unique identifier within the cluster namespace
```

<img width="274" height="64" alt="image" src="https://github.com/user-attachments/assets/d475e3fe-9af2-4766-92c8-847092a43415" />




*4. nested list: array*
    
```yaml
spec:
  containers:
  - name: nginx            # Isolated operational logic name tag
    image: nginx:latest    # Image target pulling from the container hub registry
```

<img width="327" height="101" alt="image" src="https://github.com/user-attachments/assets/cd86aa1e-d456-40d1-ac2b-1aaa20c98d89" />

  The hyphen (-) instantiates a specific container entry, assigning it a unique runtime logging tag

  ---

  
## 🛠️ Architectural Layer and functions

| Architectural Layer | Terminal Execution Command | Functional Operational Description |
|---|---|---|
| API Version | echo "apiVersion: v1" > pod.yaml | Creates a new pod.yaml file (overwriting old content) and inserts the core, stable Kubernetes API schema version. |
| Resource Type | echo "kind: Pod" >> pod.yaml | Appends the resource classification to the file, defining the deployment type as an atomic compute Pod capsule. |
| Resource Metadata | echo "metadata:" >> pod.yaml | Appends the parent organizational block used by the cluster to hold names, tracking labels, and indexing context. |
| Unique Identifier | echo " name: nginx-pod" >> pod.yaml | Appends the unique name identifier string under the metadata layer to locate the running Pod instance within the cluster namespace. |
| Desired State Specification | echo "spec:" >> pod.yaml | Appends the technical engineering blueprint block that defines the target configuration constraints the cluster must actively maintain. |
| Container Manifest Array | echo " containers:" >> pod.yaml | Appends the array list parent indicator that hosts the collection of isolated virtual application workflows inside this Pod. |
| Container Isolation Runtime Name | echo " - name: nginx" >> pod.yaml | Appends a distinct container entry using the hyphen (-) indicator, assigning it a specific runtime tracking tag. |
| Container Registry Image Target | echo " image: nginx:latest" >> pod.yaml | Appends the execution target, instructing the worker node container runtime to pull and execute the newest Nginx server binary package. |
| Print Manifest Verification | cat pod.yaml | Executes a terminal read operation to output the completed configuration file layout to the console for a final structural verification pass. |

---

## 📁 Repository Project Structure

```text
yaml-architecture/
├── .git/               # Initialized local Git version tracking database
├── README.md           # Deployment manual and workspace architecture guide
└── pod.yaml            # Fixed structural declarative Kubernetes manifest
```

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


<img width="1446" height="248" alt="image" src="https://github.com/user-attachments/assets/3a49b878-6fa7-4b2f-9b50-936fb22a67e2" />


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
*    **The Array Hyphen Protocol (`-`)**: The hyphen preceding `name: nginx` states that this block is an entry within a list array structure (`containers:`). Ensure uniform block spacing around this parameter.
* **Declarative Manifest State**: This manifest defines the ultimate execution goals. When pushed via `kubectl apply -f pod.yaml`, Kubernetes continually drives hardware parameters to align with this configuration baseline.

  
