project('valabind', 'c', 'vala')

add_project_arguments([
  '--vapidir', join_paths(meson.current_source_dir(), 'vapi')], 
  language: 'vala')

files = [
  'config.vala',
  'ctypeswriter.vala',
  'cxxwriter.vala',
  'dlangwriter.vala',
  'girwriter.vala',
  'gowriter.vala',
  'nodeffiwriter.vala',
  'swigwriter.vala',
  'utils.vala',
  'valabindwriter.vala',
  'main.vala',
]
                      
vala_dep = dependency('libvala-0.36')
glib_dep = dependency('glib-2.0')
gobject_dep = dependency('gobject-2.0')

executable(
  'valabind',
  files,
  dependencies: [glib_dep, gobject_dep, vala_dep],
  vala_args: ['--pkg', 'posix']
)
