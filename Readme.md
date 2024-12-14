

download argo cd

kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml

get deployments
 kubectl get deployments -n argocd

port formward for ui
 kubectl port-forward svc/argocd-server -n argocd 8080:443

get password
kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d
