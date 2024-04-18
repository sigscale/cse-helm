# cse-helm
Helm chart for deploying SigScale CSE on Kubernetes

## Deploy a SigScale CSE StatefulSet
	helm install cse-1 sigscale-cse

## List Helm releases
	helm list

## Remove a SigScale CSE StatefulSet
	helm uninstall cse-1

## Deploy with localization overides in sys.config
	helm install \
			--set cseConfig.create=true \
			--set-file cseConfig.sysConfig=sys.config \
			cse-1 sigscale-cse

