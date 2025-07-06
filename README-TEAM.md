# GKE React Test App - Team Repository

This is the **p-ai-smart-sales** team version of the GKE React test application with full CI/CD pipeline.

## 🚀 Quick Start

This React app automatically deploys to Google Kubernetes Engine (GKE) when you push to the `main` branch.

### Current Deployment
- **Live App**: http://34.139.79.66
- **GKE Cluster**: `smart-sales-test` (us-east1)
- **Registry**: Artifact Registry (`us-central1-docker.pkg.dev`)

## 🔄 CI/CD Pipeline

Every commit to `main` triggers:
1. ✅ Build React app
2. ✅ Create Docker image  
3. ✅ Push to Artifact Registry
4. ✅ Deploy to GKE cluster
5. ✅ Update running pods

## 🛠 Setup for Team Members

### Prerequisites
- Access to `smart-sales-464807` GCP project
- GitHub Actions secrets configured (already done)

### Local Development
```bash
npm install
npm start
```

### Deploy Changes
Simply push to `main`:
```bash
git add .
git commit -m "Your changes"
git push origin main
```

## 📁 Project Structure
```
├── .github/workflows/gke-cicd.yml  # CI/CD pipeline
├── k8s/deployment.yaml             # Kubernetes manifests
├── Dockerfile                      # Container configuration
├── src/                           # React source code
└── public/                        # Static assets
```

## 🔧 Configuration Files

- **Dockerfile**: Multi-stage build with nginx
- **k8s/deployment.yaml**: Kubernetes deployment + LoadBalancer service
- **.github/workflows/gke-cicd.yml**: Complete CI/CD pipeline

## 🌐 Access & Monitoring

- **App URL**: http://34.139.79.66
- **GCP Console**: [smart-sales-464807](https://console.cloud.google.com/kubernetes/clusters?project=smart-sales-464807)
- **GitHub Actions**: Check the Actions tab for deployment status

## 🚨 Important Notes

- The `GCP_SA_KEY` secret is already configured for CI/CD
- Pushes to `main` automatically deploy to production
- The app runs on GKE with 2 replicas for high availability

---

**Original setup**: Created from [rich-p-ai/gke-react-test-app](https://github.com/rich-p-ai/gke-react-test-app)
