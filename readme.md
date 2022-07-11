# Kubernetes Multitenancy with Capsule

This repo contains some simple resources to implement multitenancy on a Kubernetes Cluster using Capsule. 

## Prerequisites
* Helm installed 
* kubectl installed
* Hackscript installed (requires `openssl` and `jq`)
  * `curl -O https://raw.githubusercontent.com/clastix/capsule/master/hack/create-user.sh`
  * `chmod +x create-user.sh`

## Install Capsule
* `helm repo add clastix https://clastix.github.io/charts`
* `helm install capsule clastix/capsule -n capsule-system --create-namespace`

## Create tenant & log in
* `k apply -f manifest.yaml`
* `./create-user.sh noah jesters`
* `export KUBECONFIG=noah-jesters.kubeconfig`

## Additional info
* `https://github.com/clastix/capsule`
* `https://github.com/clastix/capsule-community`
* ``