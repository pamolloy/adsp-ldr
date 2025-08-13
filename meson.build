project('ldr-utils', 'c',
  version: '2.0.0',
  license: 'GPLv2',
)

ldr_sources = files(
  'ldr.c',
  'ldr_elf.c',
  'helpers.c',
  'lfd.c',
  'lfd_bf506.c',
  'lfd_bf518.c',
  'lfd_bf527.c',
  'lfd_bf533.c',
  'lfd_bf537.c',
  'lfd_bf548.c',
  'lfd_bf561.c',
  'lfd_bf592.c',
  'lfd_bf609.c',
  'lfd_sc589.c',
)

inc_dirs = include_directories('.', 'src/ldr')

libusb_dep = dependency('libusb-1.0', required: false)

executable('ldr',
  ldr_sources,
  include_directories: inc_dirs,
  c_args: ['-Wall'],
  dependencies: [libusb_dep],
)
