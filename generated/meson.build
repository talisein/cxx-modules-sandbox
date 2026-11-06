# Module sources generated at build time, as CMake's copy_if_different
# custom commands do: an interface (gen-export.mpp) and an ordinary source
# that imports it (gen-import.mpp).
fs = import('fs')
gen_export = fs.copyfile('gen-export.mpp.in', 'gen-export.mpp')
gen_import = fs.copyfile('gen-import.mpp.in', 'gen-import.mpp')

generated = executable('generated',
  gen_import,
  'use.mpp',
  gen_export,
  cpp_module_interfaces: [gen_export],
)
test('generated', generated)
