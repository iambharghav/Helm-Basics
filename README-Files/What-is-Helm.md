# What is Helm?

Helm is a package manager for Kubernetes, which allows to install Kubernetes controllers (like Prometheus, Grafana, argocd, ingress controller, etc) and third patry applications (like nginx, busybox, etc) using "charts," which bundle all necessary Kubernetes resources (like deployments, services, and configurations) into a single, manageable format, much like apt for Linux or pip for Python. 

Using Helm charts, you can install, update, and uninstall the controllers and third party appplications. Helm is also used to bundle or package your application into helm chart so that anyone from your team inside or outside the organisation can install your application.

## Why we need Helm?

Here are a few reasons why you might need HELM in Kubernetes:

**Application Packaging:** You can define all complex applications as a single unit (Chart) containing all Kubernetes manifests (YAML files). 

**Simplified application deployment:** With HELM, you can easily install, upgrade, and manage applications on your cluster with single command, instead of managing many separate files, and it makes it easy to roll back changes if necessary.

**Dependency management:** One of the key features of HELM is its ability to manage dependencies between different chart packages. This means that if an application requires a specific version of a database, for example, HELM can automatically ensure that the correct version of the database is installed and configured.

**Version control and rollback:** HELM provides built-in support for versioning and rollback, which is important for maintaining the stability of your applications. This makes it easy to revert to a previous version of an application if a problem occurs.
```
helm install my-nginx bitnami/nginx --version 13.0.0
```

**Sharing configuration:** Another important aspect of HELM is that it makes it easy to share your application configurations with others. By packaging your application into a chart, you can easily share it with other teams, making it easy to replicate your application in different environments.

**Portability:** HELM charts are portable and can be used across multiple Kubernetes clusters, and it allows to use same configuration across different environments.

**Configuration Management:** With APT, you can configure software via config files (like /etc/nginx/nginx.conf). With Helm, you can override configuration values using a YAML file. This allows you to customize how the application is deployed.
```
helm install my-nginx bitnami/nginx --values custom-values.yaml
```

## How Helm Works:

In Linux, you use APT to install software like nginx by running:

```
sudo apt install nginx
```

This pulls the nginx package from a repository, installs it, and sets it up on your system.

In Kubernetes, you use Helm to install applications like nginx by running:

```
helm install my-nginx bitnami/nginx
```

This pulls an nginx Helm chart from a chart repository, creates the necessary Kubernetes resources (like deployments, services), and sets up the application in your cluster.


