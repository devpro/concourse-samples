# Basic samples of Concourse pipelines

0/ Login

- Login on localhost:

```bash
fly --target localhost login --concourse-url http://localhost:8080/
```

(this will give you an url link to enter username/password)

1/ Hello world

- Create the pipeline

```bash
fly --target localhost set-pipeline --pipeline helloworld --config 01_helloworld.yml
```

- Open [pipelines/helloworld](http://localhost:8080/teams/main/pipelines/helloworld)
  - Enable the pipeline (play symbol) and reate a new run (+ symbol)
  - Or, quick a new run from the command line

  ```bash
  fly -t localhost unpause-pipeline -p helloworld
  fly -t localhost trigger-job -j helloworld/job
  ```
