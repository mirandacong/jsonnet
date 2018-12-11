licenses(["notice"])

cc_binary(
    name = "_jsonnet.so",
    srcs = ["_jsonnet.c"],
    linkshared = 1,
    deps = [
        label("../core:libjsonnet"),
        "@default_python//:headers",
    ],
)

py_library(
    name = "_jsonnet",
    data = [":_jsonnet.so"],
    imports = ["."],
    visibility = ["//visibility:public"],
)

py_test(
    name = "_jsonnet_test",
    srcs = ["_jsonnet_test.py"],
    data = ["test.jsonnet"],
    deps = [":_jsonnet"],
)
