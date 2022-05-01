# Wordpress deployment in k8s
WordPress is a free and open-source content management system (CMS). It is a web publishing software that allows you to create your own website or blog. Every organization requires a WordPress site due to its popularity and SEO-friendly behaviour, but there is also the hassle of deploying the WordPress site in production. We, like many other organization, recently felt compelled to use WordPress for some of our blog and product pages. Because our entire infrastructure is deployed on [Kubernetes](https://kubernetes.io/), we needed to configure the wordpress site on Kubernetes to avoid additional server maintenance for only some of our wordpress sites. So, in this article, I’ll take you through the steps which I took during deployment.

Steps: 


1. **Create a** [**PVC**](https://kubernetes.io/docs/concepts/storage/persistent-volumes/#persistentvolumeclaims) **YAML file.**
2. **Create a** [**Deployment**](https://kubernetes.io/docs/concepts/workloads/controllers/deployment/) **YAML file.**
3. **Create a** [**Service**](https://kubernetes.io/docs/concepts/services-networking/service/#defining-a-service) **YAML file.**
4. **Create an** [**Ingress**](https://kubernetes.io/docs/concepts/services-networking/ingress/) **YAML file.**

So, let’s get started with the deployment with the above yaml file. :)

Run the following command


    kubectl apply -f full-manifest.yaml

The following command will also display the resources.

    kubectl get pods
    kubectl get pvc
    kubectl get deployments
    kubectl get svc
    kubectl get ingress

The following command will display the entire syntax of your yml file.

    kubectl get pvc wordpress-pvc -o yaml
    kubectl get deployments wordpress -o yaml
    kubectl get svc wordpress-svc -o yaml
    kubectl get ingress wordpress -o yaml


