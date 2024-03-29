## Queue Service

- This deployment enables a queueing system within Kubernetes cluster.
- It uses the container image `richardchesterwood/k8s-fleetman-queue:release1`.
- Two key ports are exposed:
    - **8161:** Provides access to the administrative console, available externally through NodePort 30010 for user-friendly management.
    - **61616:** Handles sending and receiving messages, enabling core queue functionality.

        
## Position Simulator Service

- Simulates positional data using the image `richardchesterwood/k8s-fleetman-position-simulator:release1`.
- Operates silently without exposed ports.
- Requires the environment variable `SPRING_PROFILES_ACTIVE=production-microservice`.

## Position Tracker Service

- image: `richardchesterwood/k8s-fleetman-position-tracker:release1`
- Expose port 8080 to test the interface
- Requires the environment variable `SPRING_PROFILES_ACTIVE=production-microservice`.


## API Gateway Tracker Service

- image: `richardchesterwood/k8s-fleetman-api-gateway:release1`
- Expose port 8080 to test the interface
- Requires the environment variable `SPRING_PROFILES_ACTIVE=production-microservice`.



## Webapp Service

- image: `richardchesterwood/k8s-fleetman-webapp-angular:release1`
- Expose port 80
- Requires the environment variable `SPRING_PROFILES_ACTIVE=production-microservice`.
