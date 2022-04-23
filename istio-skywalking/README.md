依赖镜像：
registry.cn-hangzhou.aliyuncs.com/harmony-cloud/skywalking-oap-server:8.8.1
registry.cn-hangzhou.aliyuncs.com/harmony-cloud/skywalking-ui:8.8.1
registry.cn-hangzhou.aliyuncs.com/harmony-cloud/elasticsearch:7.5.1
registry.cn-hangzhou.aliyuncs.com/harmony-cloud/busybox:1.30(同mysql initContainer)
打包说明:
helm package ./skwalking
部署说明：
helm install skywalking ./skwalking -n istio-system(这里的命名空间必须是istio-system)
istio对接skywalking原理说明:
参考 istio可观测性-skywalking.pdf