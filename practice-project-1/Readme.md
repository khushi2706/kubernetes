💡 Project Title: URL Shortener Deployment with Kubernetes
🧩 Problem Statement:
You are tasked with deploying a production-ready URL shortener service on Kubernetes. The service should:

Be scalable

Be accessible via a LoadBalancer or Ingress

Store data persistently (even if the pod restarts)

Include health checks and basic monitoring

🛠️ Use This Docker Image:
Use docker.io/yoheimuta/url-shortener
📦 Image name: yoheimuta/url-shortener:latest

This is a tiny Go-based URL shortener with Redis support and REST API.

🔧 What You Need to Build (K8s Configs):
Deployment

Use the image above

Use environment variables for config

Add readiness and liveness probes

Set resource requests and limits

Service

Type: ClusterIP for internal communication

Expose Redis + URL shortener via names

Persistent Redis

Deploy Redis using the official image (redis:7-alpine)

Use a PVC for data persistence

Ingress (optional but recommended)

Use Ingress to expose the shortener to the outside world (if you have Ingress controller setup)

ConfigMap + Secret (Bonus)

Move environment configs to a ConfigMap

If there’s any sensitive config, move that to Secret

