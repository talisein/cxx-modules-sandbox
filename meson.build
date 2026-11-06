project('cxxmodules', 'cpp', default_options: ['cpp_std=c++20'])

# Stand-in for CMake's generate_export_header(<target>): each library
# configures <target>_export.h from this and compiles with
# -D<target>_EXPORTS, as CMake's <target>_EXPORTS does.
export_h_in = files('export.h.in')
is_static = get_option('default_library') == 'static'

subdir('simple')
subdir('duplicates')
subdir('duplicates-same-dir')
subdir('link-use')
subdir('link-use-mask')
subdir('generated')
