## 安装
### 修改docker registry

[Makefile](https://github.com/juggernaut0425/fluent-k8s-es/blob/3b2b9048420d8f821aff0a0b1a6738f2ec22075d/fluentd-es-image/Makefile#L17)

[fluentd-es-ds.yaml](https://github.com/juggernaut0425/fluent-k8s-es/blob/3b2b9048420d8f821aff0a0b1a6738f2ec22075d/fluentd-es-ds.yaml#L73)

[修改imagePullSecret](https://github.com/juggernaut0425/fluent-k8s-es/blob/3b2b9048420d8f821aff0a0b1a6738f2ec22075d/fluentd-es-ds.yaml#L106)



### 创建ES认证信息

```
kubectl -n kube-system create secret generic elasticsearch --from-literal=username=<es username> --from-literal=password=<es password>
```


## 说明

* [禁止istio auto inject](https://github.com/juggernaut0425/fluent-k8s-es/blob/1491eb58f4ad7a24e021789fecabd0a2ba52bd6f/fluentd-es-ds.yaml#L67)

* [使用 concat 处理多行日志](https://github.com/juggernaut0425/fluent-k8s-es/blob/fc4bdcc87041b3f73c769b3eeae2d43e49f131cf/fluentd-es-configmap.yaml#L408)



## 参考
* [kubernetes-fluentd-elasticsearch](https://github.com/kubernetes/kubernetes/tree/master/cluster/addons/fluentd-elasticsearch)
