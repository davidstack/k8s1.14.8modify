### debian-iptables

Serves as the base image for `registry.cn-hangzhou.aliyuncs.com/google_containers/kube-proxy-${ARCH}` and multiarch (not `amd64`) `registry.cn-hangzhou.aliyuncs.com/google_containers/flannel-${ARCH}` images.

This image is compiled for multiple architectures.

#### How to release

If you're editing the Dockerfile or some other thing, please bump the `TAG` in the Makefile.

```console
Build and  push images for all the architectures
$ make all-push
# ---> staging-registry.cn-hangzhou.aliyuncs.com/google_containers/debian-iptables-amd64:TAG
# ---> staging-registry.cn-hangzhou.aliyuncs.com/google_containers/debian-iptables-arm:TAG
# ---> staging-registry.cn-hangzhou.aliyuncs.com/google_containers/debian-iptables-arm64:TAG
# ---> staging-registry.cn-hangzhou.aliyuncs.com/google_containers/debian-iptables-ppc64le:TAG
# ---> staging-registry.cn-hangzhou.aliyuncs.com/google_containers/debian-iptables-s390x:TAG
```

If you don't want to push the images, run `make build ARCH={target_arch}` or `make all-build` instead


[![Analytics](https://kubernetes-site.appspot.com/UA-36037335-10/GitHub/build/debian-iptables/README.md?pixel)]()
