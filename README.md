# Concourse samples

![Continuous integration](https://github.com/devpro/concourse-samples/workflows/Continuous%20integration/badge.svg)

Comprehensive samples to quickly get up to speed with [Concourse](https://concourse-ci.org/)

For more information, feel free to have a look at this [knowledge base](https://knowledge-base-bertrand-thomas.cfapps.io/automation/concourse/)

## Requirements

* Have an account to a running Concourse instance
  * For the first time, you can use the ["quick & dirty" way](setup/docker-compose/quick-dirty/README.md)
  * You can also deploy it on a running Kubernetes instance from [Helm stable template](/setup/helm/stable/README.md)
  * Ultimately, you can run it on a [VM](/setup/vm/README.md)

* Have `fly` executable on the machine running the command lines (careful with the version that needs to match the one from Concourse instance)
  * Grab it from the [releases GitHub page](https://github.com/concourse/concourse/releases) or from the running Concourse web page

## Samples

* Pipelines
  * [Basic pipelines](pipelines/basic/README.md)
  * [.NET pipelines](pipelines/dotnetcore/README.md)
* Tasks
  * [Basic tasks](tasks/basic/README.md)
