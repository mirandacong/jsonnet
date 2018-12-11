licenses(["notice"])
package(default_visibility = ["//visibility:public"])

cc_library(
    name = "libjsonnet++",
    srcs = ["libjsonnet++.cpp"],
    deps = [
        label("../core:libjsonnet"),
        label("../include:libjsonnet++"),
    ],
)

# TODO (zhongming): Re-enable this test after introducing rules_jsonnet.
#cc_test(
    #name = "libjsonnet++_test",
    #srcs = ["libjsonnet++_test.cpp"],
    #data = [label("./testdata")],
    #deps = [
        #":libjsonnet++",
        #"//third_party/cc/gtest:gtest_main",
    #],
#)
