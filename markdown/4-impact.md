## Clusters

- Managed
  - Management Cluster
- Unmanaged
  - Create
  - Existing

---

## Install Unmanaged Cluster
```bash
tanzu uc create tce-local -c calico -p 80:80 -p 443:443
```
OUTPUT:
```bash
   Cluster created
   To troubleshoot, use:
   kubectl ${COMMAND} --kubeconfig /home/lac0ste/.config/tanzu/tkg/unmanaged/tce-local/kube.conf
   
   kubectl context set to tce-local
   
   tanzu package avaiilable list
   
Delete this cluster:
   tanzu unmanaged delete tce-local
```
---

## kubecolor

```bash
wget https://github.com/hidetatz/kubecolor/releases/download/v0.0.20/kubecolor_0.0.20_Linux_x86_64.tar.gz
tar -xvzf kubecolor_0.0.20_Linux_x86_64.tar.gz
sudo install -o root -g root -m 0755 kubecolor /usr/local/bin/kubecolor
alias kubectl="kubecolor"
kubectl get node
```
