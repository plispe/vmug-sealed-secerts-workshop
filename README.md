# VMUG workshop sealed-secrets

## Whoami

[Petr Pliska](https://www.linkedin.com/in/petr-pliska-16b31b48/)  
petr.pliska@geetoo.com  
DevOps Engineer

## Repository
![alt text](https://github.com/plispe/vmug-sealed-secerts-workshop/blob/master/vmug-workshop.png?raw=true)


## Topics
* What is Kubernetes(k8s) 10 000 feet overview
* Kubernetes secrets (how it works)
* What is GitOps workflow
* Storing kubernetes secrets in git (how to it without compromising them)
* Sealed secrets (bitnami)


## If you want to try it yourself(no k8s cluster is needed)
* install sealed-secrets-controller `kubectl apply -f controller.yaml`
* install [kubeseal](https://github.com/bitnami-labs/sealed-secrets#installation)
* install [kubectl](https://kubernetes.io/docs/tasks/tools/#kubectl)
* for encrypting secret use `kubeseal --cert public.cert < k8s/start/mysql-credentials.yaml > mysql-credentials-sealed.yaml`
* for description secert use `kubeseal --recovery-unseal --recovery-private-key master.key < mysql-credentials-sealed.yaml`

## Some useful links
* [Sealed secrets](https://github.com/bitnami-labs/sealed-secrets)
* [Sealing Secrets with Kustomize](https://faun.pub/sealing-secrets-with-kustomize-51d1b79105d8)
* [Lightweight Kubernetes GitOps Secrets](https://www.sokube.ch/post/lightweight-kubernetes-gitops-secrets)
