## Staring a minikube instance from config

```yml

profile: minikube

kubectl:
  keep-context: false

logging:
  alsologtostderr: true
  log_backtrace_at: file:N
  log_dir: ""
  logtostderr: true
  stderrthreshold: 2
  v: info
  vmodule: moduleSpec
  show-lib-machine-logs: true

machine_config:
  cpus: 2
  memory: 2048
  disk-size: 20g
  vm-driver: virtualbox
  xhyver-disk-driver: foobar
  host-only-cidr: 192.168.99.1/24
  hyper-virtual-switch: foobar
  iso-url: https://storage.googleapis.com/minikube/minikube-0.7.iso
  kvm-network: foobar
  disable-driver-mounts: true
  docker-env:
    key1: val1
    key2: val2
  docker-opt:
    - foobar1
    - foobar2
  insecure-registry:
    - http://registry1.net
    - http://registry2.net
  registry-mirror:
    - https://mirror1.net
    - https://mirror2.net


kubernetes:
  kubernetes-version: 1.7.3
  container-runtime: ""
  cache-images: false
  api-server-name: minikubeCA
  extra-config:
    kubelet.somecomponent: value
    apiserver.somecomponent: value
    controller-manager.somecomponent: value
    etcd.somecomponent: value
    proxy.somecomponent: value
    scheduler.somecomponent: value
  network-plugin: ""
  feature-gates:
    key1: value1
    key2: value2
  dns-domain: cluster.local

mount:
  ip: x.x.x.x
  9p-version: ""
  uid: 1001
  gid: 1001
  msize: ""
  - /host/path/dir:/guest/path/dir
  - /host/path/dir2:/guest/path/dir2


# TODO: Figure out addons configuration flags
addons:
  addon-manager: true
  dashboard: true
  kube-dns: true
  heapster: true
  ingress: true
  registry-creds: true
  registry: true
  default-storage-class: true

```
