# What is a Service Mesh?

* A Service mesh is a dedicated infrastructure layer that controls and manages service-to-service communication.
* It can handle service descovery, load balancin, traffic management and security.
    * **Service Discovery:** Automatically locates services and dynamically updates routing as services are added, removed and updated
    * **Load Balancing:** Distributes traffic across service instances for better performance and reliability
    * **Traffic Management:** Provides advance routing capabilities such as traffic splitting, A/B testing, canary releases...etc
    * **Security:** implements encryptiona nd authentication between services
    * **Observability:** Provides monitoring and tracing of service interactions
    * **Resilience:** Helps services recover from failures automatically

## How does a Service Mesh work?

* All non business logic is extracted into its own small sidecar proxy application
* This proxy handles all network traffic to and from the service 