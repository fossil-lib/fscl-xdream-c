code = files('xdream.c')

lib = static_library('fscl-xdream-c',
    code,
    include_directories: dir)

fscl_xdream_c_dep = declare_dependency(
    link_with: lib,
    include_directories: dir)
