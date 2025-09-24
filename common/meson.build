common_inc = include_directories('include')

common_deps = [ nixd_lsp_server, llvm ]

nixd_common_lib = library(
    'nixd-common',
    'lib/Eval/AttrSetClient.cpp',
    'lib/Eval/Spawn.cpp',
    'lib/Protocol/AttrSet.cpp',
    'lib/Support/AutoCloseFD.cpp',
    'lib/Support/ForkPiped.cpp',
    'lib/Support/StreamProc.cpp',
    include_directories: common_inc,
    dependencies: common_deps,
    install: true,
)

nixd_common = declare_dependency(
    include_directories: common_inc,
    link_with: nixd_common_lib,
    dependencies: common_deps,
)

