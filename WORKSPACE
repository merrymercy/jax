load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

# To update TensorFlow to a new revision,
# a) update URL and strip_prefix to the new git commit hash
# b) get the sha256 hash of the commit by running:
#    curl -L https://github.com/tensorflow/tensorflow/archive/<git hash>.tar.gz | sha256sum
#    and update the sha256 with the result.
#http_archive(
#    name = "org_tensorflow",
#    sha256 = "ad97bf01f63fe8dd02834e186d6b08cc1c7a0e4ca8051e6881891e0c4859d402",
#    strip_prefix = "tensorflow-8a3ef14ca77ae2c23523324d669d8a2b9b71c420",
#    urls = [
#        "https://github.com/tensorflow/tensorflow/archive/8a3ef14ca77ae2c23523324d669d8a2b9b71c420.tar.gz",
#    ],
#)

# For development, one can use a local TF repository instead.
# local_repository(
#    name = "org_tensorflow",
#    path = "tensorflow",
# )

# Load the path of tensorflow from environment variable TF_PATH
load("//build:load_tensorflow_from_env.bzl", "load_tensorflow_from_env")
load_tensorflow_from_env(name="org_tensorflow")

load("//third_party/pocketfft:workspace.bzl", pocketfft = "repo")
pocketfft()

# Initialize TensorFlow's external dependencies.
load("@org_tensorflow//tensorflow:workspace3.bzl", "workspace")
workspace()
load("@org_tensorflow//tensorflow:workspace2.bzl", "workspace")
workspace()
load("@org_tensorflow//tensorflow:workspace1.bzl", "workspace")
workspace()
load("@org_tensorflow//tensorflow:workspace0.bzl", "workspace")
workspace()
