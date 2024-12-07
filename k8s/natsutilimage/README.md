# natsutil


## Description
A container image Nat uses for debugging and the like


## Use
### Launch a shell in a temporary container

    kubectl run --rm -it natsutil --image=ghcr.io/natpowning/natsutil -- zsh

### Deploy a persistent container that you can launch shells within

Deploy

    kubectl apply -f deployment.yml

Launch zsh session

    kubectl exec -it $(kubectl get pod -l app=natsutil -o jsonpath="{.items[0].metadata.name}") -- zsh
