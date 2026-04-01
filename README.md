# Private Cloud Infrastructure & K8s Orchestration

[cite_start]This repository contains the configuration and deployment manifests for transitioning physical network infrastructure into a container-integrated private cloud environment[cite: 1, 2].

---

## 📝 Project Description
[cite_start]This repo features YAML manifests for a private cloud bridging Cisco networking with K8s via VMware vSphere[cite: 2, 4]. [cite_start]Highlights: Calico eBGP peering with Cisco 2911, TrueNAS iSCSI storage, and a GitOps pipeline via GitLab/ArgoCD[cite: 4, 9, 32]. [cite_start]Engineered for high availability and secure isolation[cite: 2, 8].

---

## 🚀 Key Features

* [cite_start]**Network Segmentation**: Traffic isolation using Cisco physical networking with VLAN 10 (Management), 20 (Service), and 30 (Storage)[cite: 2, 5].
* [cite_start]**Virtualization**: Enterprise-grade virtualization using VMware vSphere (ESXi and vCenter)[cite: 4, 9].
* [cite_start]**High Availability**: Kubernetes cluster with Master HA to eliminate single points of failure[cite: 4, 8, 28].
* [cite_start]**Dynamic Routing**: eBGP peering between Calico CNI (AS64512) and Cisco 2911 (AS64513) for automatic route updates[cite: 4, 9, 14].
* [cite_start]**GitOps CI/CD**: Automated container builds and deployments using GitLab CI and ArgoCD[cite: 2, 6, 9].
* [cite_start]**Storage Decoupling**: Centralized shared storage using TrueNAS iSCSI Target for data persistence[cite: 4, 32, 52].
* [cite_start]**Observability**: Full-stack monitoring with Prometheus and Grafana, including SMTP-based alerting for system health[cite: 9, 35, 43].

---

## 🛠️ Technical Stack

| Category | Technology |
| :--- | :--- |
| **Virtualization** | [cite_start]VMware ESXi 7.0.3, vCenter, vDS [cite: 9] |
| **Orchestration** | [cite_start]Kubernetes v1.29 (kubeadm) [cite: 9] |
| **Networking** | [cite_start]Cisco 2911, Calico (BGP Mode), MetalLB [cite: 4, 9, 66] |
| **CI/CD** | [cite_start]GitLab, ArgoCD [cite: 9] |
| **Storage** | [cite_start]TrueNAS CORE (iSCSI) [cite: 9] |
| **Monitoring** | [cite_start]Prometheus, Grafana, Node Exporter [cite: 9] |

---

## 📂 Repository Structure

* [cite_start]**`network/`**: BGP peering, MetalLB L2 advertisement, and Ingress-NGINX configurations[cite: 14, 64, 67].
* [cite_start]**`storage/`**: PersistentVolume (PV) and PVC manifests for TrueNAS iSCSI integration[cite: 32, 52].
* [cite_start]**`cicd/`**: GitLab CI pipelines and ArgoCD application definitions[cite: 6, 29].
* [cite_start]**`services/`**: Application manifests for MariaDB, Nginx, Jupyter, and Postfix/Dovecot[cite: 51, 54, 57, 60].
* [cite_start]**`monitoring/`**: Prometheus, Alertmanager, and Grafana deployment files[cite: 35, 37, 43].
