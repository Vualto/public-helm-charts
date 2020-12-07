# public-helm-charts

To add as a repo:
`helm repo add vualto https://raw.githubusercontent.com/Vualto/public-helm-charts/master/`

To update the repo:
`helm repo update vualto https://raw.githubusercontent.com/Vualto/public-helm-charts/master/`

To add a new package to the repo:
1) Run `helm package --version <version> .` in the same folder as your `charts.yaml`.
2) Add the resulting `.tgz` file to the root of this repo.
3) Run `helm repo index --url https://raw.githubusercontent.com/Vualto/public-helm-charts/master/ .` to generate a new index.yaml.
4) Commit and push the new helm package and updated `index.yaml`.
5) Run `helm repo update vualto` to refresh the local version info.
6) Run `helm search vualto` to see the new version.
