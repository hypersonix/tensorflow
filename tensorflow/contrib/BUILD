# Description:
#   contains parts of TensorFlow that are experimental or unstable and which are not supported.

licenses(["notice"])  # Apache 2.0

exports_files(["LICENSE"])

package(default_visibility = ["//tensorflow:__subpackages__"])

py_library(
    name = "contrib_py",
    srcs = glob(["**/*.py"]),
    srcs_version = "PY2AND3",
    visibility = ["//tensorflow:internal"],
    deps = [
        "//tensorflow/contrib/ctc:ctc_py",
        "//tensorflow/contrib/distributions:distributions_py",
        "//tensorflow/contrib/layers:layers_py",
        "//tensorflow/contrib/linear_optimizer:sdca_ops_py",
        "//tensorflow/contrib/lookup:lookup_py",
        "//tensorflow/contrib/skflow",
        "//tensorflow/contrib/testing:testing_py",
        "//tensorflow/contrib/util:util_py",
    ],
)

cc_library(
    name = "contrib_kernels",
    visibility = ["//visibility:public"],
    deps = [
        "//tensorflow/contrib/linear_optimizer/kernels:sdca_ops",
    ],
)

filegroup(
    name = "all_files",
    srcs = glob(
        ["**/*"],
        exclude = [
            "**/METADATA",
            "**/OWNERS",
        ],
    ),
    visibility = ["//tensorflow:__subpackages__"],
)
