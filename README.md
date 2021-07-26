# kubebuilder-tutorial

<https://book.kubebuilder.io/cronjob-tutorial/cronjob-tutorial.html>

```zsh
$ kubebuilder init --domain tutorial.kubebuilder.io --repo tutorial.kubebuilder.io/kubebuilder-tutorial
# adding new API
$ kubebuilder create api --group batch --version v1 --kind CronJob
# Implement defaulting/validating webhooks
$ kubebuilder create webhook --group batch --version v1 --kind CronJob --defaulting --programmatic-validation
```

## Running and deploying the controller

```zsh
# install CRD
$ make install
# run locally
$ make run ENABLE_WEBHOOKS=false
# create CronJob
$ kubectl create -f config/samples/batch_v1_cronjob.yaml
# check
$ kubectl get cronjob.batch.tutorial.kubebuilder.io -o yaml
$ kubectl get job
```
