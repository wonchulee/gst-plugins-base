sources = [
  'main.cpp',
  'gstthread.cpp',
  'pipeline.cpp',
  'qrenderer.cpp',
]

moc_headers = [
  'gstthread.h',
  'pipeline.h',
  'qrenderer.h',
]

moc_files = qt5_mod.preprocess(moc_headers : moc_headers)
executable('mousevideoverlay', sources, moc_files,
  cpp_args : [gst_plugins_base_args],
  include_directories: [configinc, libsinc],
  dependencies : [qt5core_dep, qt5gui_dep, gst_dep, video_dep, gstgl_dep, libgl],
  install: false)
