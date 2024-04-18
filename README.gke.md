# Manage Google Kubernetes Engine (GKE)

## Create a GKE Autopilot Cluster
	gcloud container clusters create-auto cse-cluster

## Configure `kubectl` to use the GKE Cluster
	gcloud container clusters get-credentials cse-cluster

$# Get the Pods (after `helm install`)
	kubectl get pods

## Get the log of init container
	kubectl logs cse-1-sigscale-cse-0 -c cse-init

## Get the log of container
	kubectl logs cse-1-sigscale-cse-0

## Describe the pod
	kubectl describe pod cse-1-sigscale-cse-0

## Attach to a GKE pod deployment which runs cse container
	$ kubectl attach -ti cse-1-sigscale-cse-0 -c cse -i -t
	(cse@cse-1-sigscale-cse-0.otp-cse.default.svc.cluster.local)5>
### There is no `detach` so you'll need to kill the `kubectl attach` process

