project('cxxmodules', 'cpp', default_options: ['cpp_std=c++20'])

# Stand-in for CMake's generate_export_header(<target>): configures
# <target>_export.h and returns it with the define that marks the
# library's own compiles, as CMake's <target>_EXPORTS does.
export_h_in = files('export.h.in')
is_static = get_option('default_library') == 'static'

subdir('simple')
subdir('duplicates')
subdir('duplicates-same-dir')
