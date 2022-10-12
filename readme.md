CI:
Dockerbuild:
    aws ecr login | docker login
    docker build -t ecrrepourl:tag
    docker push ecrrepourl:tag

CD:
kubectl apply -f deployment.yaml service.yaml ingress.yaml
