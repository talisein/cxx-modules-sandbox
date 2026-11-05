simple_export_h = configure_file(
  input: export_h_in,
  output: 'simple_export.h',
  configuration: {
    'TARGET': 'simple',
    'PREFIX': 'SIMPLE',
    'STATIC': is_static ? 1 : 0,
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
