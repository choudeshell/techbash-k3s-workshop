# Getting Started

Download
- Rancher Desktop (https://rancherdesktop.io/)
- Open Lens (https://github.com/MuhammedKalkan/OpenLens)
- VSCode (https://code.visualstudio.com/)
    - Install Kubernetes extension (https://marketplace.visualstudio.com/items?itemName=ms-kubernetes-tools.vscode-kubernetes-tools)

## Advanced Install

> If you are running iptables in nftables mode instead of legacy you might encounter issues. We recommend utilizing newer iptables (such as 1.6.1+) to avoid issues.
> ```bash
> sudo update-alternatives --set iptables /usr/sbin/iptables-legacy
> ```

1. Download K3s v1.25.3+k3s1 from https://github.com/k3s-io/k3s/releases/tag/v1.25.3%2Bk3s1
```shell
wget https://github.com/k3s-io/k3s/releases/download/v1.25.3%2Bk3s1/k3s
```
2. Add execute modifier to `k3s`
```shell
chmod +x k3s
```
3. Run `k3s` as `root` with `server` argument
```shell
sudo ./k3s server
```
4. In another terminal, copy contents of `/etc/rancher/k3s/k3s.yaml`
```shell
cat /etc/rancher/k3s/k3s.yaml
```
5. Grab IP address of host
```shell
ip addr show
```
6. Open Lens and go to File > Add Cluster
7. Paste in contents of `/etc/rancher/k3s/k3s.yaml`
8. Change HTTP address to IP address of host Ubuntu System
----
# Bookmarks
Kubernetes API Docs
https://kubernetes.io/docs/reference/generated/kubernetes-api/v1.25/
