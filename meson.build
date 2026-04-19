project(
  'openstreetmapviewer',
  'c',
  meson_version : '>= 1.3.0',
  version : '0.1',
  default_options : ['warning_level=3'],
)

dependencies = [ webkitdep('webkit2gtk', version : '>=4.0')
]

sources = [
  'openstreetmapviewer.c',
]

exe = executable(
  'openstreetmapviewer',
  sources,
  dependencies : dependencies,
  install : true,
)

test('basic', exe)
