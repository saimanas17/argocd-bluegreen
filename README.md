# Blue-Green Deployment Demo with GitOps

A CI/CD demonstration project showcasing automated blue-green deployments using Jenkins, ArgoCD, Argo Rollouts, and GitOps principles.

## 🎯 What This Project Does

Developer pushes code → Jenkins builds Docker image → Updates Kubernetes manifests → ArgoCD syncs → Argo Rollouts creates preview → Manual approval → Production updated with zero downtime.

## 🏗️ Architecture

```
Code Push → Jenkins → Docker Hub → Update Manifests
                                         ↓
                                   GitHub Webhook
                                         ↓
                                      ArgoCD
                                         ↓
                                  Argo Rollouts
                                         ↓
                           Preview (Test) → Approve → Deployment
```

## 📂 Repository Structure

```
bluegreen-deployment-demo/
├── README.md
├── nginx-demo/                    # Application code (submodule)
└── argo-bluegreen-manifests/      # Kubernetes manifests (submodule)
```

## 🚀 Quick Start

```bash
# Clone with submodules
git clone --recursive https://github.com/saimanas17/argocd-bluegreen.git
cd bluegreen-deployment-demo
```

## 🛠️ Technology Stack

- **Jenkins**: CI/CD automation
- **Docker/Docker Hub**: Containerization and registry
- **GitHub**: Source control and GitOps
- **Kubernetes**: Container orchestration
- **ArgoCD**: GitOps continuous delivery
- **Argo Rollouts**: Blue-green deployment strategy
- **Nginx**: Web server

## 📊 Key Features

- Automated CI/CD pipeline
- GitOps-based infrastructure management
- Zero-downtime blue-green deployments
- Manual approval gates for safety
- Webhook-driven automation
- Separate repositories for code and infrastructure

## 🔗 Submodules

- [argo-bluegreen-app](https://github.com/saimanas17/argo-bluegreen-app) - Application code and Jenkinsfile
- [argo-bluegreen-manifests](https://github.com/saimanas17/argo-bluegreen-manifests) - Kubernetes manifests

For detailed setup and usage, see individual repository READMEs.

## 📞 Contact

Email: gourabathini.s@northeastern.edu  
GitHub: [@saimanas17](https://github.com/saimanas17)

---

**Built by Manas Gourabathini**
