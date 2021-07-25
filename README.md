# kubebuilder-tutorial

https://book.kubebuilder.io/cronjob-tutorial/cronjob-tutorial.html

```zsh
$ kubebuilder init --domain tutorial.kubebuilder.io --repo github.com/TakuKaneda/kubebuilder-tutorial
# adding new API
$ kubebuilder create api --group batch --version v1 --kind CronJob
# Implement defaulting/validating webhooks
$ kubebuilder create webhook --group batch --version v1 --kind CronJob --defaulting --programmatic-validation
``` 