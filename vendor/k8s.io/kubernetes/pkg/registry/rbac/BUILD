load("@io_bazel_rules_go//go:def.bzl", "go_library")

go_library(
    name = "go_default_library",
    srcs = [
        "escalation_check.go",
        "helpers.go",
    ],
    importpath = "k8s.io/kubernetes/pkg/registry/rbac",
    visibility = ["//visibility:public"],
    deps = [
        "//vendor/k8s.io/apimachinery/pkg/api/meta:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/conversion:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/runtime:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/util/runtime:go_default_library",
        "//vendor/k8s.io/apiserver/pkg/authentication/user:go_default_library",
        "//vendor/k8s.io/apiserver/pkg/authorization/authorizer:go_default_library",
        "//vendor/k8s.io/apiserver/pkg/endpoints/request:go_default_library",
        "//vendor/k8s.io/kubernetes/pkg/apis/rbac:go_default_library",
    ],
)

filegroup(
    name = "package-srcs",
    srcs = glob(["**"]),
    tags = ["automanaged"],
    visibility = ["//visibility:private"],
)

filegroup(
    name = "all-srcs",
    srcs = [
        ":package-srcs",
        "//vendor/k8s.io/kubernetes/pkg/registry/rbac/clusterrole:all-srcs",
        "//vendor/k8s.io/kubernetes/pkg/registry/rbac/clusterrolebinding:all-srcs",
        "//vendor/k8s.io/kubernetes/pkg/registry/rbac/reconciliation:all-srcs",
        "//vendor/k8s.io/kubernetes/pkg/registry/rbac/rest:all-srcs",
        "//vendor/k8s.io/kubernetes/pkg/registry/rbac/role:all-srcs",
        "//vendor/k8s.io/kubernetes/pkg/registry/rbac/rolebinding:all-srcs",
        "//vendor/k8s.io/kubernetes/pkg/registry/rbac/validation:all-srcs",
    ],
    tags = ["automanaged"],
    visibility = ["//visibility:public"],
)
