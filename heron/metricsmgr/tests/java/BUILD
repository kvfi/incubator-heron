java_library(
    name = "metricsmgr-tests",
    srcs = glob(["**/*.java"]),
    deps = [
        "//heron/api/src/java:api-java-low-level",
        "//heron/common/src/java:basics-java",
        "//heron/common/src/java:network-java",
        "//heron/common/src/java:config-java",
        "//heron/common/src/java:test-helpers-java",
        "//heron/metricsmgr/src/java:metricsmgr-java",
        "//heron/spi/src/java:metricsmgr-spi-java",
        "//heron/proto:proto_common_java",
        "//heron/proto:proto_metrics_java",
        "//heron/proto:proto_tmaster_java",
        "@com_google_guava_guava//jar",
        "@com_google_protobuf//:protobuf_java",
        "//third_party/java:mockito",
        "//third_party/java:junit4",
    ],
)

java_tests(
    test_classes = [
        "org.apache.heron.metricsmgr.MetricsUtilTests",
        "org.apache.heron.metricsmgr.HandleTMasterLocationTest",
        "org.apache.heron.metricsmgr.MetricsManagerServerTest",
        "org.apache.heron.metricsmgr.executor.SinkExecutorTest",
        "org.apache.heron.metricsmgr.sink.tmaster.TMasterSinkTest",
        "org.apache.heron.metricsmgr.sink.metricscache.MetricsCacheSinkTest",
        "org.apache.heron.metricsmgr.sink.FileSinkTest",
        "org.apache.heron.metricsmgr.sink.WebSinkTest",
        "org.apache.heron.metricsmgr.sink.PrometheusSinkTests",
    ],
    runtime_deps = [
        ":metricsmgr-tests",
    ],
    data = ["//heron/config/src/yaml:test-config-internals-yaml"],
    size = "small",
)
