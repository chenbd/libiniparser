load("@rules_cc//cc:defs.bzl", "cc_library")
load("//:build/build.bzl", "COPTS")

package(default_visibility = ["//visibility:public"])

local_src = [
    "src/dictionary.c",
    "src/iniparser.c",
    "include/iniparser/dictionary.h",
    "include/iniparser/iniparser.h",
]

local_copts = [
    "-isystem third_party/",
    "-isystem third_party/libiniparser/include/",
]

cc_library(
    name = "iniparser",
    srcs = local_src,
    linkstatic = True,
    alwayslink = True,
    visibility = ["//visibility:public"],
    copts = COPTS + local_copts,
)
