# .NET samples of Concourse pipelines

0/ Login

- Login on localhost:

```bash
fly --target localhost login --concourse-url http://localhost:8080/
```

(this will give you an url link to enter username/password)

1/ Hello world

```bash
fly -t localhost execute --config tasks/basic/helloworld.yml
```
