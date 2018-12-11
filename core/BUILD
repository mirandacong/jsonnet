licenses(["notice"])
package(default_visibility = ["//visibility:public"])

cc_library(
    name = "libjsonnet",
    srcs = [
        "desugarer.cpp",
        "formatter.cpp",
        "lexer.cpp",
        "libjsonnet.cpp",
        "parser.cpp",
        "pass.cpp",
        "static_analysis.cpp",
        "string_utils.cpp",
        "vm.cpp",
    ],
    hdrs = [
        "ast.h",
        "desugarer.h",
        "formatter.h",
        "json.h",
        "lexer.h",
        "parser.h",
        "pass.h",
        "state.h",
        "static_analysis.h",
        "static_error.h",
        "string_utils.h",
        "unicode.h",
        "vm.h",
    ],
    deps = [
        label("../include:libjsonnet"),
        label("../include:libjsonnet_fmt"),
        label("../stdlib:std"),
        label("../third_party/md5:libmd5"),
    ],
    linkopts = ["-lm"],
    includes = ["."],
)

cc_test(
    name = "lexer_test",
    srcs = ["lexer_test.cpp"],
    deps = [
        ":libjsonnet",
        # Note: On Ubuntu, apt-get install libgtest-dev google-mock
        "//third_party/cc/gtest:gtest_main",
    ],
)

cc_test(
    name = "parser_test",
    srcs = ["parser_test.cpp"],
    deps = [
        ":libjsonnet",
        "//third_party/cc/gtest:gtest_main",
    ],
)

cc_test(
    name = "libjsonnet_test",
    srcs = ["libjsonnet_test.cpp"],
    deps = [
        ":libjsonnet",
        "//third_party/cc/gtest:gtest_main",
    ],
)
