load("@io_bazel_rules_go//go:def.bzl", "go_library")

go_library(
    name = "go_default_library",
    srcs = ["metrics.pb.go"],
    importmap = "k8s.io/kubernetes/vendor/github.com/prometheus/client_model/go",
    importpath = "github.com/prometheus/client_model/go",
    visibility = ["//staging/src/k8s.io/component-base/metrics:prometheus_import_allow_list"],
    deps = ["//vendor/github.com/golang/protobuf/proto:go_default_library"],
)

filegroup(
    name = "package-srcs",
    srcs = glob(["**"]),
    tags = ["automanaged"],
    visibility = ["//visibility:private"],
)

filegroup(
    name = "all-srcs",
    srcs = [":package-srcs"],
    tags = ["automanaged"],
    visibility = ["//visibility:public"],
)
