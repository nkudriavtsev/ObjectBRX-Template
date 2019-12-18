project('Sample', 'cpp',
  version : '0.1',
  default_options : ['warning_level=3', 'cpp_std=c++11'])

incdir = include_directories([
  'cmd',
  'dbx',
  'gui',
  )

headers = files([
  'StdAfx.h',
  'cmd/cmdCom.h'
])

sources = files([
  'Sample.cpp',
  'StdAfx.cpp',
  'acrxEntryPoint.cpp',
  'cmd/cmdCom.cpp',
  'cmd/cmdDbx.cpp',
  'cmd/cmdGui.cpp',
  'dbx/MyEntity.cpp',
  'dbx/MyOPMExtension.cpp',
  'gui/MyDialogBar.cpp',
  'gui/MyQuadExtension.cpp',
  'gui/MyRibbonContent.cpp'
])

brx_sdk = dependency('brx19-sdk')

add_global_arguments([
  ## '-Wall',
  '-fPIC',
  '-frtti',
  '-fno-signed-zeros',
  '-fvisibility=default',
  '-Wno-sign-compare',
  '-Wno-sign-conversion',
  '-Wno-empty-body',
  '-Wno-reorder',
  '-Wno-parentheses',
  '-Wno-switch',
  '-Wno-unused-parameter',
  '-Wno-unused-function',
  '-Wno-unused-variable',
  '-Wno-unused-label',
  '-Wno-unknown-pragmas',
  '-Wno-comment',
  '-Wno-strict-aliasing',
  '-Wno-unused-but-set-variable',
  '-Wno-unused-value',
  '-Wno-attributes',
  '-D_UNICODE',
  '-DUNICODE',
  '-DNDEBUG',
  '-D_AFXEXT',
  '-D_ACRXAPP',
  '-DBRX_APP',
  '-D_FILE_OFFSET_BITS=64',
  '-D_LARGE_FILES',
  '-D__BRXTARGET=19'
  ], language : 'cpp')

shared_library('Sample',
  sources,
  dependencies : brx_sdk,
  include_directories : incdir,
  name_prefix : '',
  name_suffix : 'lrx',
  link_args : '-ldl')
