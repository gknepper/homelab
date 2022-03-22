# Notes on Tanzu on MAC

Runs only on Docker for mac v3.6.0: 
https://docs.docker.com/desktop/mac/release-notes/3.x/
https://desktop.docker.com/mac/stable/amd64/67351/Docker.dmg


# Start Tanzu UI
tanzu management-cluster create --ui

# Test 
tanzu mc get

# Tanzu get kubeconfig
tanzu management-cluster kubeconfig get --admin --export-file tanzu-ubuntu.yaml

# Federate Tanzu on Rancher
curl --insecure -sfL https://rancher.home/v3/import/nhst8mshwg4c4vg4tc5k656q4hkbrs2wbjt4rrjmw5658bfq7qsbgd_c-m-kxsv62xm.yaml |  kubectl --kubeconfig tanzu-ubuntu.yaml apply -f 
