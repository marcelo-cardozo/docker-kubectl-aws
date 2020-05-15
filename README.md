# Docker & Kubectl & Aws
Dockerfile including **kubectl** and **aws-iam-authenticator** to deploy kubernetes resources to a Kubernetes Cluster hosted on AWS.

### Docker Hub
[marcecardozo/kubectl-eks](https://hub.docker.com/r/marcecardozo/kubectl-eks)

#### Example
```
docker run -v "$(pwd)/k8s/:/app/k8s/" \
           -e AWS_ACCESS_KEY_ID=${ENV_AWS_TRAVIS_ACCESS_KEY} \
           -e AWS_SECRET_ACCESS_KEY=${ENV_AWS_TRAVIS_SECRET_ACCESS_KEY} \
           -e AWS_PROFILE=${ENV_AWS_TRAVIS_PROFILE}  \
           marcecardozo/kubectl-eks \
           kubectl --kubeconfig=/app/k8s/config/kubeconfig.yaml apply -f /app/k8s/
```

