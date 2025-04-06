# library project declare
project(
    'libmin',
    'c',
    version: '0.1',
    default_options: ['c_std=c11'],
)

# headers
subdir('include')
headers = include_directories('include')

# sources
sources = files('min.c')

# declare a static library
# can use shared_library() for shared libraries
# or just use library() and declare by options
libmin = static_library(
    'libmin',
    sources,
    include_directories: headers,
    install: true,
)

# declare as a dependency
libmin_dep = declare_dependency(include_directories: headers, link_with: libmin)

# generate pkgconfig files
pkg_config = import('pkgconfig')
pkg_config.generate(
    name: 'min',
    filebase: 'min',
    description: 'a meson tutorial subproject',
    libraries: libmin,
)
