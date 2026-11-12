# Module 19: Service Mesh with Istio

**Tasks:**

1. Deployed Istio Service Mesh components in EKS Cluster via our Terraform pipeline
2. Exposed microervice app through Istio gateway via secure HTTPS access
3. Validated Istio mTLS traffic and configured PeerAuthentication
4. Secured Pod Traffic using Istio Authorization Policy components

---

## Part1: Deployed Istio Service Mesh components in EKS Cluster via our Terraform pipeline

**repo: Infra**

- I installed `istiod`, `istio-base` and `istio-ingress-gateway` components in the cluster.
- I added cluster and node level security groups and rules for secure communication.
- By adding a label I enable Istio envoy proxy injection (at first for one namespace only).
  - It means only the objects in that namespace will get the proxy injected.
- The IaC pipeline will create the necessary resources.

## Part2: Expose microervice app through Istio gateway via secure HTTPS access

**repo: GitOps**

- Configured traffic routing in cluster via Istio gateway.
  - At first we test with HTTP(80) before enabling HTTPS.
  - Once we generated the TLS cert, we enable HTTPS(443) and redirect all HTTP traffic to it.
- Create a Virtual Service for the frontend application to route traffic through the gateway.
- Generated a self-signed certificate useing `openssl` for TLS communication and store it in AWS Secret Manager.
- Redirect HTTP traffic to HTTPS.

## Part3: Validate Istio mTLS traffic

- Enable mTLS for services in the mesh.