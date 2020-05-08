In the name of compiling some info for a future blog post, what ended up being the things we did to make Kustomize/Kubebuilder not be a nightmare to work with? Was it just .template files that we generate off of so actual values don't get checked into the repo/so `envsubst` works and doesn't clobber stuff? I feel like it was more but maybe it just took a lot of iterations to get there (I know we did the Git filter/hook first).

`provision.sh`

```
git update-index --assume-unchanged deploy/validator-dev-env/kustomization.yaml
```
