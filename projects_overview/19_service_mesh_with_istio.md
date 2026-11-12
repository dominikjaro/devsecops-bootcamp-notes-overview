# Module 19: Service Mesh with Istio

**Tasks:**
1. 

**Part1:** Deployed Istio Service Mesh components in EKS Cluster via our Terraform pipeline

Project Description:

- We install `istiod`, `istio-base` and istio-ingress-gateway` components in the cluster.
- We add cluster and node level security groups and rules forsecure communication.
- By adding a label we enable Istio envoy proxy injection.
- Our IaC pipeline will create the necessary resources.

**Part2:** Expose microervice app through Istio gateway via secure HTTPS access
Project Description:
    - We configure traffic routing in cluster via Istio gateway.
    - Create a Virtual Service for the frontend application to route traffic through the gateway.
    - Generated a self-signed certificate useing `openssl` for TLS communication and store it in AWS Secret Manager.
    - Redirect HTTP traffic to HTTPS.

**Part3:** Validate Istio mTLS traffic
Project Description:
    - Enable mTLS for services in the mesh.