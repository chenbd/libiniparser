load("@rules_cc//cc:defs.bzl", "cc_binary", "cc_library")
load("//cyber/ehp:build/build.bzl", "COPTS")

package(default_visibility = ["//visibility:public"])

local_src = [
    "src/dictionary.c",
    "src/iniparser.c",
]

local_include = [
    "-isystem cyber/ehp/external/",
    "-isystem cyber/ehp/external/libiniparser/include/",
]

cc_library(
    name = "iniparser",
    linkstatic = True,
    srcs = local_src,
    visibility = ["//visibility:public"],
    alwayslink = True,
    copts = COPTS + local_include,
    deps = [
        "//cyber",
    ],
)
