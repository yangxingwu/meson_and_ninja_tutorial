project(
    'meson tutorial',
    'c',
    version: '0.1',
    default_options: ['c_std=c11'],
)

# headers
subdir('include')
incs = include_directories('include')

# sources
subdir('src')

# subprojects
libmin_dep = dependency('libmin', fallback: ['libmin', 'libmin_dep'])

executable(
    'tutorial',
    sources,
    include_directories: incs,
    dependencies: [libmyownmax_dep, libmin_dep],
    install: true,
)
