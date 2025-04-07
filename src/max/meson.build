# sources
max_sources = files('max.c')

# declare a shared library
# can use static_library() for static libraries
# or just use library() and declare by options
libmax = shared_library(
    'max',
    max_sources,
    include_directories: incs,
    install: true,
)

# declare as a dependency
libmax_dep = declare_dependency(include_directories: incs, link_with: libmax)

# generate pkgconfig files
pkg_config = import('pkgconfig')
pkg_config.generate(
    name: 'max',
    filebase: 'max',
    description: 'a meson tutorial dependency',
    libraries: libmax,
)
