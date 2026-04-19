project(
  'openstreetmapviewer',
  'c',
  meson_version : '>= 1.3.0',
  version : '0.1',
  default_options : ['warning_level=3'],
)

webkit2gtk_dep = dependency('webkit2gtk-4.1')

dependencies = [ webkit2gtk_dep
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
