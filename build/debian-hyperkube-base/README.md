### debian-hyperkube-base

Serves as the base image for `registry.cn-hangzhou.aliyuncs.com/google_containers/hyperkube-${ARCH}`
images.

This image is compiled for multiple architectures.

#### How to release

If you're editing the Dockerfile or some other thing, please bump the `TAG` in the Makefile.

```console
# Build and  push images for all the architectures
$ make all-push
# ---> staging-registry.cn-hangzhou.aliyuncs.com/google_containers/debian-hyperkube-base-amd64:TAG
# ---> staging-registry.cn-hangzhou.aliyuncs.com/google_containers/debian-hyperkube-base-arm:TAG
# ---> staging-registry.cn-hangzhou.aliyuncs.com/google_containers/debian-hyperkube-base-arm64:TAG
# ---> staging-registry.cn-hangzhou.aliyuncs.com/google_containers/debian-hyperkube-base-ppc64le:TAG
# ---> staging-registry.cn-hangzhou.aliyuncs.com/google_containers/debian-hyperkube-base-s390x:TAG
```

If you don't want to push the images, run `make all-build` instead


[![Analytics](https://kubernetes-site.appspot.com/UA-36037335-10/GitHub/build/debian-hyperkube-base/README.md?pixel)]()
