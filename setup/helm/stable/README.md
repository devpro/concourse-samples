# Concourse stable Helm chart

See [concourse/concourse-chart](https://github.com/concourse/concourse-chart)

```bash
# add Concourse repo
helm repo add concourse https://concourse-charts.storage.googleapis.com/

# generate manifest file
helm template concourse/concourse -f values.yaml > temp.yaml
```
