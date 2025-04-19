# DevOps Interview Questions

## Kubernetes Interview Questions

### Kubernetes Basics
- What is a Pod in Kubernetes? Create a pod.yaml for a single-container pod running Nginx.
- What is a Deployment in Kubernetes? Write a deployment.yaml for deploying 3 replicas of an Nginx container.
- What is a Service in Kubernetes, and what are the types of Services?
- When would you use each type of Kubernetes Service (ClusterIP, NodePort, LoadBalancer, ExternalName)?
- What is the difference between ClusterIP and ExternalName service types?
- Explain port, targetPort, and nodePort in a Kubernetes service.
- How would you expose a Kubernetes application externally?
- What is the use of Ingress and Ingress Controller in Kubernetes?
- What are Namespaces in Kubernetes?
- What is Port Forwarding in Kubernetes?
- What is the difference between kubectl apply and kubectl create?
- Explain the role of kube-dns or CoreDNS in service discovery.
- How would you detect pod-level DNS issues?

### Kubernetes Controllers and Workloads
- Explain the Kubernetes controllers: Deployment, StatefulSet, ReplicaSet, and DaemonSet.
- What is the difference between Deployment and ReplicaSet?
- What are Kubernetes Probes (Liveness, Readiness, Startup)?
- How does Kubernetes handle failed liveness probes over time?
- What are ephemeral containers and how do you use them for debugging?
- How do you set up Pod Anti-Affinity rules?
- Describe the impact of using hostNetwork: true in a pod.
- How would you debug a failing CronJob in Kubernetes?
- What is the difference between ephemeral volumes and persistent volumes?
- What are the best practices for running stateful workloads in Kubernetes?
- How do PodDisruptionBudgets interact with cluster upgrades?

### Kubernetes Security and Governance
- Explain how Kubernetes RBAC integrates with third-party identity providers.
- How would you approach securing secrets in a GitOps workflow?
- How do you manage dynamic secrets in Kubernetes for applications?
- How do you handle network segmentation in a multi-tenant Kubernetes cluster?
- How can you validate the integrity of container images before deployment?

### Kubernetes Operations and Troubleshooting
- How does Kubernetes handle node scaling with Cluster Autoscaler?
- How do you handle stuck finalizers during resource deletion?
- What are some potential performance bottlenecks in Kubernetes workloads?
- How would you perform a rolling update of a ConfigMap without downtime?
- How would you detect and recover from node pressure scenarios automatically?
- How does container resource throttling work in Kubernetes?
- How do you handle Kubernetes version upgrades in a production cluster?
- How would you migrate workloads between clusters?
- How would you build a multi-region highly available Kubernetes setup?

## Infrastructure & DevOps

### Terraform
- How do you prevent accidental resource deletion?
- How do you handle provider API rate limiting?
- What happens when recovering from a corrupted state file?
- How do you migrate from one backend to another?
- How do you handle state drift in production environments?
- How do you manage secrets securely in Terraform?
- How do you implement zero-downtime infrastructure updates?
- How do you properly structure Terraform modules for enterprise use?
- How do you handle large-scale refactoring without disruption?
- How do you implement effective Terraform testing strategies?
- Write a simple Terraform script to provision a virtual machine on any cloud.

### Infrastructure & DevOps
- What is Helm, and what are its components (Chart, Repository, Release)?
- What is kubectl kustomize and how does it compare with Helm?
- How can you prevent a misconfigured Helm chart from affecting production?
- What tools would you use for validating Kubernetes manifests before deployment?
- What is the difference between EXPOSE in a Dockerfile and docker run -p?
- How do you run Nginx on a Linux server using Docker?
- Explain HTTP, HTTPS, TCP, and UDP with examples.
- What is a Dockerfile? Write a basic Dockerfile for a Node.js application.
- What is a base image in Docker? Which base image would you use for Python or Node.js?
- How do you check for open ports on a Linux system?
- What are the benefits of using a firewall?
- What is the difference between Stateful and Stateless applications? Give examples.
- What's the process for creating custom controllers or operators in Kubernetes?

## Ansible 

### Configuration Management
- You need to configure a server differently based on its data center location. How would you dynamically apply different configurations using Ansible?
- You are tasked with patching 500 servers, but you need to ensure high availability. How do you apply updates in a rolling fashion using Ansible?
- You want to deploy an application only if the checksum of the deployment package has changed. How would you implement this in Ansible?
- How would you use Ansible to validate that a web application is accessible after deployment, and roll back automatically if it's not?

### Connectivity and Execution
- You need to run a command on 100 servers, but not all of them have Python installed (so Ansible can't connect). How would you handle this?
- You need to run a playbook as a different user on some servers (not the default SSH user). How would you implement this in Ansible?
- A task must only run if a specific port is open on a remote host. How can this condition be enforced using Ansible modules?
- You need to execute a shell command but only if a specific process is not running. How would you use Ansible to do this check and act accordingly?

### Organization and Structure
- You are provisioning new servers and need to apply different roles depending on their hostnames or tags. How would you dynamically assign roles?
- How would you secure sensitive variables like AWS access keys and reuse them across multiple playbooks?
- You have multiple teams working with Ansible. How would you structure your playbooks, roles, and inventories to manage RBAC and minimize conflicts?
- You want to store Ansible inventory in a CMDB or database instead of static files. How do you implement this using dynamic inventory plugins?

### Cross-Platform and Idempotency
- You need to write a playbook that can configure both Windows and Linux hosts. How would you handle cross-platform tasks in Ansible?
- You want to ensure idempotency when copying a configuration file generated from a Jinja2 template. How would you implement change detection and handlers?
- Your deployment is failing randomly on certain hosts due to transient issues. How can you add retry logic in Ansible for such tasks?
- Some servers have different package managers (e.g., yum, dnf, apt). How do you write a common playbook that handles all OS types?

### Advanced Orchestration
- You need to deploy a multi-tier application (DB > App > Web). How can you orchestrate dependencies and sequencing between the roles?
- You want to enforce security baselines on servers like SSH settings, file permissions, and package restrictions. How would you manage this with Ansible?
- You need to collect custom performance metrics like CPU or memory usage across all servers and store them in a centralized location. How would you do this with Ansible?
- How would you use Ansible to create users with different SSH keys based on the environment (dev, staging, prod)?

## DevOps Manager

### Challenging Project
- Focus on complexity: tight deadlines, legacy systems, cross-team dependencies. Highlight leadership, troubleshooting, stakeholder management.
Multiple Critical Issues
- Show how you assess business impact. Mention triaging, delegation, and stakeholder updates.

### Failed Deployment
- Acknowledge responsibility, explain root cause analysis. Share rollback plans, monitoring, and lessons learned.
- Dev vs Ops Conflict
- Emphasize empathy and communication. Mention metrics, shared goals (e.g., DORA metrics), and post-incident reviews.

### CI/CD Improvement
- Share specifics: parallel builds, containerization, test automation. Mention results like reduced deployment time or increased reliability.
Zero Downtime Change
- Explain blue-green or canary deployments. Discuss planning, traffic shifting, and automated rollbacks.

### Security & Compliance
- Talk about secrets management, role-based access, policy-as-code (e.g., OPA). Mention audits, vulnerability scanning (e.g., Snyk, Trivy).
Negative Feedback
- Stay humble. Share how you listened and improved. Mention building trust over time.

### Mentoring Juniors
- Talk about pair programming, code reviews, documentation. Mention creating onboarding guides or training sessions.
Cost Optimization
- Example: right-sizing VMs, shutting down idle resources, using spot instances. Involve FinOps concepts if applicable.

### High-Severity Incident Handling
- Mention on-call rotations, incident response playbooks. Stress calm communication and post-incident reviews.

### Cloud Migration
- Highlight planning, phased approach, dependency mapping. Talk about lift-and-shift vs rearchitecting decisions.

### Automation vs Manual
- Describe risk-based approach. Mention that automation is for repetitive tasks, manual for critical judgment-based steps.

### DevOps Metrics
- Deployment frequency, change failure rate, MTTR, lead time. Explain how you use them to improve processes.

## Environment Management Interview Questions

### How do you manage different environments across the deployment pipeline?
- Answer: Use Terraform workspaces with env-specific .tfvars files, dedicated EKS clusters, ArgoCD for GitOps, and separate AWS accounts for prod/non-prod with cross-account access via Terraform.

### How do you handle configuration management across environments?
- Answer: Combine Terraform variables with Kubernetes ConfigMaps/Secrets, store sensitive data in Vault, validate config in CI/CD, and expose infrastructure values via Terraform outputs that ArgoCD consumes.

### What's your code promotion strategy across environments?
- Answer: Git-based workflow (feature→dev, develop→staging, main→prod) using immutable container images tagged with Git SHA. Implement approvals for protected branches and verification for production deployments.

### How do you implement rollback strategies?
- Answer: Maintain Terraform state history, leverage ArgoCD's deployment history, implement health checks, tag images with Git SHAs, and design database migrations with backward compatibility.

### How do you handle disaster recovery for multi-region infrastructure?
- Answer: AWS multi-region setup with S3 replication, DynamoDB global tables, cross-region backups, consistent GitOps deployment, and Route53 failover with regular DR testing.

### How do you secure containers throughout their lifecycle?
- Answer: Implement pipeline security with pre-commit hooks and vulnerability scanning, runtime protection with network policies and monitoring, and enforce security standards with admission controllers.

### How would you optimize a slow CI/CD pipeline?
- Answer: Profile pipeline, implement caching, parallelize tests, use targeted applies, leverage selective sync, and create ephemeral environments, reducing deployment time from 65 to 12 minutes.

### What's your approach to cloud cost optimization?
- Answer: Comprehensive tagging, right-sizing, cluster autoscaling, Spot instances, storage tiering, scheduled scaling for non-production, and reserved instances, achieving 40%+ cost reduction.

### How do you implement observability for microservices?
- Answer: Three-pillar approach with Prometheus for metrics, centralized logging, and OpenTelemetry tracing, enhanced with service mesh telemetry and SLO-based alerting.

### What deployment strategies do you use for various scenarios?
- Answer: Rolling updates for stateless apps, Blue-Green deployments for critical systems, and Canary releases with progressive traffic shifting for high-traffic applications.