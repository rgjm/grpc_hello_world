load("@com_github_grpc_grpc//bazel:cc_grpc_library.bzl", "cc_grpc_library")
load("@com_github_grpc_grpc//bazel:grpc_build_system.bzl", "grpc_proto_library")

package(default_visibility = ["//visibility:public"])

proto_library(
  name = "hello_world_proto",
  srcs = ["hello_world.proto"],
)

cc_proto_library(
  name = "hello_world_cc_proto",
  deps = [":hello_world_proto"],
)

cc_grpc_library(
    name = "hello_world_cc_grpc",
    srcs = [":hello_world_proto"],
    grpc_only = True,
    deps = [":hello_world_cc_proto"],
)
