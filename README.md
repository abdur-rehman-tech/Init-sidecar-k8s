
# Kubernetes Init & Sidecar Example

[![Kubernetes Version](https://img.shields.io/badge/Kubernetes-1.24+-green.svg?style=flat-square)](https://kubernetes.io/)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg?style=flat-square)](LICENSE)

This project demonstrates the **Init + Sidecar container pattern** in Kubernetes.

---

## 🚀 Features

- **Init Containers:** Preload configuration, scripts, or data before main container starts.
- **Sidecar Containers:** Run alongside main application for logging, monitoring, or auxiliary tasks.
- **Production-ready:** Ensures proper startup sequence and resource management.
- **Highly Configurable:** Customize images, commands, and resources.

---

## 🛠 Prerequisites

- Kubernetes cluster (local, cloud, or KIND)
- `kubectl` installed and configured

---

## ⚡ Deployment

Apply the deployment manifest:

```bash
kubectl apply -f deployment.yaml
