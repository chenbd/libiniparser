load("@rules_cc//cc:defs.bzl", "cc_library")
load("//modules/map/hdmap_static:build/build.bzl", "COPTS")

package(default_visibility = ["//visibility:public"])

local_src = [
    "src/dictionary.c",
    "src/iniparser.c",
]

local_copts = [
    "-isystem modules/map/hdmap_static/external/",
    "-isystem modules/map/hdmap_static/external/libiniparser/include/",
]

cc_library(
    name = "iniparser",
    srcs = local_src,
    linkstatic = True,
    alwayslink = True,
    visibility = ["//visibility:public"],
    copts = COPTS + local_copts,
    deps = [
        "//modules/map/hdmap_static",
    ]
)
