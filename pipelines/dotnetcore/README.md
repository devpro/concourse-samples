# .NET samples of Concourse pipelines

0/ Login

- Login on localhost:

```bash
fly --target localhost login --concourse-url http://localhost:8080/
```

(this will give you an url link to enter username/password)

1/ ASP.NET Core web application (single project)

```bash
# create the pipeline
fly --target localhost set-pipeline --pipeline aspnetcore --config 01_aspnetcore.yml

# unpause the pipeline
fly -t localhost unpause-pipeline -p aspnetcore

# run the pipeline
fly -t localhost trigger-job -j aspnetcore/aspnetcore-unit-tests
```

2/ .NET Global tools

```bash
# create the pipeline
fly --target localhost set-pipeline --pipeline dotnetglobaltool --config pipelines/dotnetcore/02_globaltool.yml --var mdbatlas-publickey=xxxx --var mdbatlas-publickey=yyyy -var almops-token=zzz --var almops-org=xxxx -var almops-user=yyyy -var almops-token=zzz

# unpause the pipeline
fly -t localhost unpause-pipeline -p dotnetglobaltool

# run the pipeline (and watch)
fly -t localhost trigger-job -j dotnetglobaltool/mongodb-atlas -w
fly -t localhost trigger-job -j dotnetglobaltool/azure-devops -w
```
