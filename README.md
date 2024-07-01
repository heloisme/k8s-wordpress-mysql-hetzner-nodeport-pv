# Kubernetes Deployment on Hetzner Cloud with CSI Driver

This guide provides steps to deploy MySQL and WordPress applications on Kubernetes in the Hetzner Cloud, utilizing the Hetzner Cloud CSI driver for persistent storage.

## Prerequisites

- Kubernetes cluster running on Hetzner Cloud from [here](https://github.com/heloisme/private-k8s-cluster-hetzner).
- Hetzner Cloud CSI driver installed. Follow the instructions [here](https://github.com/hetznercloud/csi-driver/blob/main/docs/kubernetes/README.md#getting-started).

## Steps

1. **Install Hetzner Cloud CSI Driver**:
   Follow the instructions provided in the Hetzner Cloud CSI driver [documentation](https://github.com/hetznercloud/csi-driver/blob/main/docs/kubernetes/README.md#getting-started) to install the CSI driver in your Kubernetes cluster.

2. **Create Kubernetes Resources**:
   Save the following YAML configurations into separate files (`mysql-deployment.yaml`, `pv-claims.yaml`, `pvs.yaml`, `secrets.yaml`, `wordpress-deployment.yaml`).

3. **Apply Kubernetes Configurations**:
   Run the following command to create the Kubernetes resources:
   ```sh
   kubectl apply -f .

By following these steps, you will have a WordPress and MySQL deployment on your Hetzner Cloud Kubernetes cluster with persistent storage managed by the Hetzner Cloud CSI driver.
