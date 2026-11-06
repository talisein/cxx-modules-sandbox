# A module with an interface partition (parta) and two internal partitions
# (partb, impl). CMake's CXX_MODULE_INTERNAL_PARTITIONS file set type maps to
# cpp_internal_partitions.
partitions = library('partitions',
  'module.mpp',
  'parta.mpp',
  'partb.mpp',
  'impl.mpp',
  cpp_module_interfaces: ['module.mpp', 'parta.mpp'],
  cpp_internal_partitions: ['partb.mpp', 'impl.mpp'],
)
