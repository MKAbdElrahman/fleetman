**## Queue Service**

**Overview:**

- This deployment enables a queueing system within Kubernetes cluster.
- It uses the container image `richardchesterwood/k8s-fleetman-queue:release1`.
- Two key ports are exposed:
    - **8161:** Provides access to the administrative console, available externally through NodePort 30010 for user-friendly management.
    - **61616:** Handles sending and receiving messages, enabling core queue functionality.

**Getting Started:**

1. **Prerequisites:**
    - Kubernetes cluster (I use minkube for local development)
    - kubectl access
2. **Deployment:**
    ```bash
    kubectl apply -f queue-service.yaml
    ```
3. **Access:**
    - **Admin Console:**
        - Open http://<NODE_IP>:<NODE_PORT> in your browser (replace`<NODE_PORT>` with the value `minikube ip`).
        - Default credentials: username: admin, password: admin.
    - **Message API:**
        - See official documentation for details on using the API at port 61616.
