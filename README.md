# Cloud Builder for SigScale CSE Helm Charts
Google [Cloud Build](https://cloud.google.com/build/docs/overview)
runs a Docker container to execute build steps provided in a YAML
file (`cloudbuild.yaml`). This project creates a Docker container
to be used by Cloud Build in our CI/CD pipelines.

## Pushing commits to a branch triggers Cloud Builder:
	$ git push

## Manually trigger Cloud Builder:
	$ gcloud --project sigscale-sigtran builds submit --config cloudbuild.yaml

