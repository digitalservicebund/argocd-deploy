# Update Kustomize Manifests and Deploy in one Step!

## About

This GHA takes care of the multiple steps required to deploy code changes to a selected environment:
- Bump the container image tag in your infra repo to point the newest version available.
- Trigger ArgoCD to sync.
- Wait and report the result of the ArgoCD sync. This can be used to make sure the service is up and running before starting the E2E test step of your CI/CD pipeline. Default to 120s and can be modified with the `argocd_sync_timeout` variable.

## How To Use And Example

Pre-requisites and detailed instructions on how to use this GHA are available in the [Platform docs](https://platform-docs.prod.ds4g.net/user-docs/how-to-guides/hosting-applications/deploy-new-application-platform/automate-application-deployment). 

## Updating this action

After merging a dependabot PR or pushing changes, you need to [cut a new release](https://docs.github.com/en/repositories/releasing-projects-on-github/managing-releases-in-a-repository).
