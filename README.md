use case: using kustomization in dev and staging environment by adding patches inorder in increase the number of replicas

usage:
    kind create cluster kustomize

    kubectl create namespace development
    kubectl create namespace staging

    kubectl apply -k /overlays/dev -n development
    kubectl apply -k /overlays/stage -n staging
