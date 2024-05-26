# cluster-api-provider-docker

```bash
❯ operator-sdk init --domain  cluster.x-k8s.io --repo github.com/kubeorbit/cluster-api-provider-docker --project-version 3
INFO[0000] Writing kustomize manifests for you to edit...
INFO[0000] Writing scaffold for you to edit...
INFO[0000] Get controller runtime:
$ go get sigs.k8s.io/controller-runtime@v0.16.3
INFO[0003] Update dependencies:
$ go mod tidy
Next: define a resource with:
$ operator-sdk create api
```

## Create DockerCluster API

```bash
❯ operator-sdk create api --group infrastructure --version v1alpha1 --kind DockerCluster
INFO[0000] Create Resource [y/n]
y
INFO[0001] Create Controller [y/n]
y
INFO[0002] Writing kustomize manifests for you to edit...
INFO[0002] Writing scaffold for you to edit...
INFO[0002] api/v1alpha1/dockercluster_types.go
INFO[0002] api/v1alpha1/groupversion_info.go
INFO[0002] internal/controller/suite_test.go
INFO[0002] internal/controller/dockercluster_controller.go
INFO[0002] internal/controller/dockercluster_controller_test.go
INFO[0002] Update dependencies:
$ go mod tidy
INFO[0002] Running make:
$ make generate
mkdir -p /Users/vishal/workspace/kubeorbit/cluster-api-provider-docker/bin
test -s /Users/vishal/workspace/kubeorbit/cluster-api-provider-docker/bin/controller-gen && /Users/vishal/workspace/kubeorbit/cluster-api-provider-docker/bin/controller-gen --version | grep -q v0.13.0 || \
	GOBIN=/Users/vishal/workspace/kubeorbit/cluster-api-provider-docker/bin go install sigs.k8s.io/controller-tools/cmd/controller-gen@v0.13.0
/Users/vishal/workspace/kubeorbit/cluster-api-provider-docker/bin/controller-gen object:headerFile="hack/boilerplate.go.txt" paths="./..."
Next: implement your new API and generate the manifests (e.g. CRDs,CRs) with:
$ make manifests
```