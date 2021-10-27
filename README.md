# sample-nginx-helm
Nginx application for kubernetes


## CI/CD

The github actions workflows are located on `.github/workflows`, the actions uses an IAM with an OIDC provider in order to assume such role and be able to access AWS resources.

### Dev Deployment
Every commit into `main` will trigger the dev deployment.

### Staging Deployment

1. Create a new release at https://github.com/bryan-rhm/sample-nginx-helm/releases/new.
2. Create a tag for the semantic version you plan on releasing.
3. Specify a title with the same semantic version.
4. Make sure the `This is a pre-release` option is turned on.
5. Publish the release.
6. Click on the `Actions` tab and find the workflow run for your recent release.
7. Your code will be deployed to the staging environment.
