load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

# Build against Kythe master.  Run `bazel sync` to update to the latest commit.
http_archive(
    name = "io_kythe",
    strip_prefix = "kythe-master",
    urls = ["https://github.com/google/kythe/archive/master.zip"],
)

load("@io_kythe//:external.bzl", "kythe_dependencies")

http_archive(
    name = "com_github_google_glog",
    sha256 = "f8c9457f351775181f0b99c342baf7ec99383f27bc1bdf6fac9e427411542d63",
    strip_prefix = "glog-028d37889a1e80e8a07da1b8945ac706259e5fd8",
    url = "https://github.com/google/glog/archive/028d37889a1e80e8a07da1b8945ac706259e5fd8.zip",
)

bind(
    name = "zlib",  # required by @com_google_protobuf
    actual = "@net_zlib//:zlib",
)

kythe_dependencies()
