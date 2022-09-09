# pipelinerun-imagechange-go-app

A utilitly image to create a new pipleine run when base or builder images are updated from stable or latest tags.

> see <https://labs.consol.de/development/kubernetes/openshift/2022/03/14/image-change-triggers-for-tekton.html>

```sh
podman build -t quay.io/trevorbox/pipelinerun-imagechange-go-app:latest .
podman push quay.io/trevorbox/pipelinerun-imagechange-go-app:latest
```
