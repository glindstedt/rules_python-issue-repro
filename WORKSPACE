load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

# rules_python_version = "740825b7f74930c62f44af95c9a4c1bd428d2c53"  # Latest @ 2021-06-23
#
# http_archive(
#     name = "rules_python",
#     sha256 = "",
#     strip_prefix = "rules_python-{}".format(rules_python_version),
#     url = "https://github.com/bazelbuild/rules_python/archive/{}.zip".format(rules_python_version),
# )

# http_archive(
#     name = "rules_python",
#     sha256 = "778197e26c5fbeb07ac2a2c5ae405b30f6cb7ad1f5510ea6fdac03bded96cc6f",
#     urls = [
#         "https://mirror.bazel.build/github.com/bazelbuild/rules_python/releases/download/0.2.0/rules_python-0.2.0.tar.gz",
#         "https://github.com/bazelbuild/rules_python/releases/download/0.2.0/rules_python-0.2.0.tar.gz",
#     ],
# )

http_archive(
    name = "rules_python",
    sha256 = "934c9ceb552e84577b0faf1e5a2f0450314985b4d8712b2b70717dc679fdc01b",
    url = "https://github.com/bazelbuild/rules_python/releases/download/0.3.0/rules_python-0.3.0.tar.gz",
)

load("@rules_python//python:pip.bzl", "pip_parse")

pip_parse(
    name = "py_deps",
    requirements_lock = "//:requirements_lock.txt",
)

load("@py_deps//:requirements.bzl", "install_deps")

install_deps()
