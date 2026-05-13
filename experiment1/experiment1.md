# Experiment 1

get basic yaml:
`k run nginx-yaml --image=nginx --dry-run=client -o yaml > nginx-yaml.yaml`

`k exec -it nginx-docs -- /bin/bash`

create deployment yaml
`k create deploy nginx-deploy --image=nginx --replicas=5 --dry-run=client -o yaml > deploy.yaml`

create namespace
`k create ns mealie --dry-run=client -o yaml > mealie-ns.yaml`

set namespace in context
`k config set-context --current --namespace=mealie`
