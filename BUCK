load('//:buckaroo_macros.bzl', 'buckaroo_deps_from_package')
load('//:subdir_glob.bzl', 'subdir_glob')

cxx_library(
  name = 'aws-lambda-cpp', 
  exported_headers = subdir_glob([
    ('include', '**/*.h'), 
  ]), 
  srcs = glob([
    'src/**/*.cpp', 
  ]), 
  deps = buckaroo_deps_from_package('github.com/buckaroo-pm/aws-sdk-cpp') + 
    buckaroo_deps_from_package('github.com/buckaroo-pm/pkg-config-curl'), 
  visibility = [
    'PUBLIC', 
  ], 
)
