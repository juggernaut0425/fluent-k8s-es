改自：[fluentd-elasticsearch](https://github.com/kubernetes/kubernetes/tree/master/cluster/addons/fluentd-elasticsearch)

## 创建ES认证信息

kubectl -n kube-system create secret generic elasticsearch --from-literal=username=<es username> --from-literal=password=<es password>


## 禁止istio auto inject

[sidecar.istio.io/inject: "false"](https://github.com/juggernaut0425/fluent-k8s-es/blob/1491eb58f4ad7a24e021789fecabd0a2ba52bd6f/fluentd-es-ds.yaml#L67)
