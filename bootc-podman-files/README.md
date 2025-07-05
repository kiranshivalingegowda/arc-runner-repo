# Install the dynamic volume provisioner
  - use this document to install the local volume 
  - https://github.com/openebs/dynamic-localpv-provisioner/blob/develop/docs/quickstart.md


# Install the Github actions controller
helm install ghacont \
    --namespace "gha-arc-runners" \
    --create-namespace \
    oci://ghcr.io/actions/actions-runner-controller-charts/gha-runner-scale-set-controller 


# Install the Github actions runners
helm install gharunner \
    --namespace "gha-arc-runners" \
    oci://ghcr.io/actions/actions-runner-controller-charts/gha-runner-scale-set  --values custom-values.yaml


# Install Arc runners in kubernetes mode
  - 

# Commands
- kubectl config set-context --current --namespace=gha-arc-runners

