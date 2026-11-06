# Not built with Meson.
#
# CMake's link-use-mask and link-use-mask-reverse each link both simple and
# duplicates, which both provide a module named 'duplicate', and expect the
# library listed first to win. Meson rejects this on purpose: a module name
# may have only one provider reaching a link.
#
# A module name owns more than its exported symbols. Every provider also
# defines the same module initializer symbol, which runs the module's dynamic
# initialization. With shared libraries the first one bound runs for every
# caller, including the other library's own load-time initialization, so the
# shadowed module is silently left uninitialized. With static archives the
# same collision is a duplicate-symbol link error as soon as both objects are
# needed.
#
# If Meson permitted it, the directory would build as:
#
# link_use_mask = executable('link-use-mask',
#   'use.mpp',
#   link_with: [simple, duplicates],
# )
# test('link-use-mask', link_use_mask)
#
# link_use_mask_reverse = executable('link-use-mask-reverse',
#   'use.mpp',
#   link_with: [duplicates, simple],
# )
# test('link-use-mask-reverse', link_use_mask_reverse, should_fail: true)
