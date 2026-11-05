duplicates_export_h = configure_file(
  input: export_h_in,
  output: 'duplicates_export.h',
  configuration: {
    'TARGET': 'duplicates',
    'PREFIX': 'DUPLICATES',
    'STATIC': is_static ? 1 : 0,
  },
)

# Provides a module named 'duplicate', as simple does: two unrelated
# libraries in one project may each own a module of the same name as long
# as nothing links them together.
duplicates = library('duplicates',
  'duplicate.mpp',
  duplicates_export_h,
  cpp_module_interfaces: ['duplicate.mpp'],
  cpp_args: '-Dduplicates_EXPORTS',
)
