
# Connection Proto
package(default_visibility = ["//visibility:public"])
load("@com_github_grpc_grpc//bazel:cc_grpc_library.bzl", "cc_grpc_library")

java_proto_library (
    name = "ComputerJavaProto",
    deps = ["ComputerProto"],
)

cc_proto_library (
    name = "ComputerCcProto",
    deps = ["ComputerProto"]
)

cc_grpc_library (
    name = "ComputerCcGrpc",
    srcs = [":ComputerProto"],
    grpc_only = True,
    deps = [":ComputerCcProto"],
)

proto_library (
    name = "ComputerProto",
    srcs = ["computer.proto"],
)
