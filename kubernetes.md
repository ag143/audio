# Kubernetes basics
## Pod:
> A pod is a collection of containers sharing a network, acting as the basic unit of deployment in Kubernetes. All containers in a pod are scheduled on the same node.

## Label
> Labels are the mechanism used to organize Kubernetes objects. A label is a key-value pair with certain restrictions concerning length and allowed values but without any pre-defined meaning. You're free to choose labels as you see fit, for example, to express environments such as "this pod is running in production" or ownership, like "department X owns that pod".

## Deployment
> A deployment is a supervisor for pods, giving you fine-grained control over how and when a new pod version is rolled out as well as rolled back to a previous state.

## Service
> A service is an abstraction for pods, providing a stable, so called virtual IP (VIP) address. While pods may come and go and with it their IP addresses, a service allows clients to reliably connect to the containers running in the pod using the VIP. The "virtual" in VIP means it is not an actual IP address connected to a network interface, but its purpose is purely to forward traffic to one or more pods. Keeping the mapping between the VIP and the pods up-to-date is the job of kube-proxy, a process that runs on every node, which queries the API server to learn about new services in the cluster.

## Port Forwarding
> In the context of developing applications on Kubernetes, it is often useful to quickly access a service from your local environment without exposing it using, for example, a load balancer or an ingress resource. In these situations, you can use port forwarding. Let's create an application consisting of a deployment and a service named simpleservice, serving on port 80:

## Health Checks
> In order to verify if a container in a pod is healthy and ready to serve traffic, Kubernetes provides for a range of health checking mechanisms. Health checks, or probes as they are called in Kubernetes, are carried out by the kubelet to determine when to restart a container (liveness probes) and used by services and deployments to determine if a pod should receive traffic (readiness probes). We will focus on HTTP health checks in the following. Note that it is the responsibility of the application developer to expose a URL that the kubelet can use to determine if the container is healthy (and potentially ready).

## Environment Variables
> You can set environment variables for containers running in a pod. Additionally, Kubernetes automatically exposes certain runtime information via environment variables.

## Namespaces
> Namespaces provide a scope for Kubernetes resources, carving up your cluster in smaller units. You can think of it as a workspace you're sharing with other users. Many resources such as pods and services are namespaced. Others, such as nodes, are not namespaced, but are instead treated as cluster-wide. As a developer, you'll usually use an assigned namespace, however admins may wish to manage them, for example to set up access control or resource quotas.

## Volumes
> A Kubernetes volume is essentially a directory accessible to all containers running in a pod. In contrast to the container-local filesystem, the data in volumes is preserved across container

## Persistent Volumes or PV
> A persistent volume (PV) is a cluster-wide resource that you can use to store data in a way that it persists beyond the lifetime of a pod. The PV is not backed by locally-attached storage on a worker node but by networked storage system such as EBS or NFS or a distributed filesystem like Ceph.

## Secrets
> You don't want sensitive information such as a database password or an API key stored in clear text. Secrets provide you with a mechanism to store such information in a safe and reliable way with the following properties: • Secrets are namespaced objects, that is, exist in the context of a specific namespace • You can access them via a volume or an environment variable from a container running in a pod • The secret data on nodes is stored in tmpfs volumes • A per-secret size limit of 1MB exists • The API server stores secrets as plaintext in etcd

## Logging
> Logging is one option to understand what is going on inside your applications and the cluster at large. Basic logging in Kubernetes makes the output a container produces available through the kubectl tool. More advanced setups consider logs across nodes and store them in a central place, either within the cluster or via a dedicated (cloud-based) service.

## Jobs
> A job in Kubernetes is a supervisor for pods that run for a certain time to completion, for example a calculation or a backup operation.

## Nodes
> In Kubernetes, nodes are the (potentially virtual) machines where your workloads run. As a developer, you typically don't deal with nodes directly, however as an admin you might want to familiarize yourself with node operations. https://k8s-examples.container-solutions.com/ Cluster Role ConfigMap Daemon Set Endpoints Job Namespace Persist volume Pod PodPreset Priority clas Role Secret Service Account Storage Class Broken Secret Cloud providers Tests Cluster Role Binding Cron job Deployment Ingress Limit Range Network Policy Persistent Volume Claim Pod Disruption Budget Pod Security Policy Resource Quotas Role Binding Service Stateful set Broken-pod Broken-Deployment Plugins
