# ai_agent_k8s

Kubernetes manifests for deploying the AI Agent application.

## Structure

```
manifests/
├── namespace.yaml       # Namespace: ai-agent
├── serviceaccount.yaml  # ServiceAccount
├── configmap.yaml       # App configuration
├── deployment.yaml      # Deployment (1 replica, nginx:stable)
├── service.yaml         # ClusterIP Service on port 80
├── ingress.yaml         # Ingress (nginx class, ai-agent.example.com)
└── hpa.yaml             # HorizontalPodAutoscaler (1-5 replicas)
```

## Apply

```bash
# Apply all manifests in order
kubectl apply -f manifests/namespace.yaml
kubectl apply -f manifests/
```

## Delete

```bash
kubectl delete -f manifests/
```
