# 🧩 Kubernetes Init & Sidecar Containers

![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white)

Demonstrates two common multi-container patterns in Kubernetes.

| Pattern | File | What it shows |
|---|---|---|
| **Init container** | `initi-container.yml` | Runs to completion **before** the main container starts (setup, config, waiting on dependencies) |
| **Sidecar container** | `sidecar.yml` | Main container writes logs to a shared `emptyDir` volume; the sidecar tails them in parallel |

## 🚀 Usage

```bash
kubectl apply -f initi-container.yml
kubectl get pod init-test -w
kubectl logs init-test -c init-container
kubectl logs init-test -c main-container

kubectl apply -f sidecar.yml
kubectl logs sidecar-test -c sidecar-container -f
```

## 💡 When to use

- **Init**: DB migrations, downloading config, waiting for a service to be ready
- **Sidecar**: log shipping, service mesh proxies, config reloaders

---

## 👤 Author

**Abdur Rehman** · DevSecOps Engineer · Founder of [ARTechOps](https://artechops.com)

[LinkedIn](https://www.linkedin.com/in/muhamad-abdur-rehman-81777b366/) · [GitHub](https://github.com/abdur-rehman-tech) · [artechops.com](https://artechops.com)
