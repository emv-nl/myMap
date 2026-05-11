project(
  'openstreetmapviewer',
  'c',
  meson_version : '>= 1.3.0',
  version : '0.1',
  default_options : ['warning_level=3'],
)

##
# Configuration section
##

server_url_setting = get_option('server_url')

conf_data = configuration_data()
conf_data.set('version' , '0.0.2')
conf_data.set('server_url' , server_url_setting)


configure_file(
	input : 'config.h.in',
	output : 'config.h',
	configuration : conf_data,
)

configuration_inc = include_directories('.')

##
# Dependencies section
##

webkit2gtk_dep = dependency('webkit2gtk-4.1')

dependencies_inc = [ webkit2gtk_dep
]

##
# Source file section
##

sources = [
  'openstreetmapviewer.c',
]

##
# Build and install section
##

exe = executable(
  'openstreetmapviewer',
  sources,
  dependencies : dependencies_inc,
  include_directories : configuration_inc,
  install : true,
)

