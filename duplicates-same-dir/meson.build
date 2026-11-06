# Two libraries built from the same interface source with the same flags,
# each providing the module 'duplicate'. They share a BMI class, so this
# builds only because each target keeps its BMIs in its own directory; it
# would still be an error for one link to reach both.
foreach n : ['1', '2']
  library('duplicates-same-dir-' + n,
    'duplicate.mpp',
    cpp_module_interfaces: ['duplicate.mpp'],
  )
endforeach
