# sources
myownmax_sources = files('max.c')

# declare a shared library
# can use static_library() for static libraries
# or just use library() and declare by options
libmyownmax = shared_library(
    'myownmax',
    myownmax_sources,
    include_directories: incs,
    install: true,
)

# declare as a dependency
libmyownmax_dep = declare_dependency(include_directories: incs, link_with: libmyownmax)

# generate pkgconfig files
pkg_config = import('pkgconfig')
pkg_config.generate(
    name: 'myownmax',
    filebase: 'max',
    description: 'a meson tutorial dependcies',
    libraries: libmyownmax,
)
