simple_export_h = configure_file(
  input: 'simple_export.h.in',
  output: 'simple_export.h',
  configuration: {
    'SIMPLE_STATIC_DEFINE': get_option('default_library') == 'static',
  },
)

simple = library('simple',
  'use.mpp',
  'duplicate.mpp',
  'another.mpp',
  simple_export_h,
  cpp_module_interfaces: ['duplicate.mpp', 'another.mpp'],
  cpp_args: '-Dsimple_EXPORTS',
)
