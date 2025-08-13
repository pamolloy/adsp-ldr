project('ldr-utils', 'c',
  version: '2.0.0',
  license: 'GPLv2',
)

ldr_sources = files(
  'src/ldr.c',
  'src/ldr_elf.c',
  'src/helpers.c',
  'src/lfd.c',
  'src/lfd_bf506.c',
  'src/lfd_bf518.c',
  'src/lfd_bf527.c',
  'src/lfd_bf533.c',
  'src/lfd_bf537.c',
  'src/lfd_bf548.c',
  'src/lfd_bf561.c',
  'src/lfd_bf592.c',
  'src/lfd_bf609.c',
  'src/lfd_sc589.c',
  'src/termios-mingw.c',
)

inc_dirs = include_directories('include')

libusb_dep = dependency('libusb-1.0', required: false)

executable('ldr',
  ldr_sources,
  include_directories: inc_dirs,
  c_args: ['-Wall'],
  dependencies: [libusb_dep],
)
