pageinspect_sources = files(
  'brinfuncs.c',
  'btreefuncs.c',
  'fsmfuncs.c',
  'ginfuncs.c',
  'gistfuncs.c',
  'hashfuncs.c',
  'heapfuncs.c',
  'rawpage.c',
)

pageinspect = shared_module('pageinspect',
  pageinspect_sources,
  kwargs: contrib_mod_args,
)
contrib_targets += pageinspect

install_data(
  'pageinspect--1.0--1.1.sql',
  'pageinspect--1.1--1.2.sql',
  'pageinspect--1.2--1.3.sql',
  'pageinspect--1.3--1.4.sql',
  'pageinspect--1.4--1.5.sql',
  'pageinspect--1.5--1.6.sql',
  'pageinspect--1.5.sql',
  'pageinspect--1.6--1.7.sql',
  'pageinspect--1.7--1.8.sql',
  'pageinspect--1.8--1.9.sql',
  'pageinspect--1.9--1.10.sql',
  'pageinspect.control',
  kwargs: contrib_data_args,
)

tests += {
  'name': 'pageinspect',
  'sd': meson.current_source_dir(),
  'bd': meson.current_build_dir(),
  'regress': {
    'sql': [
      'page',
      'btree',
      'brin',
      'gin',
      'gist',
      'hash',
      'checksum',
      'oldextversions',
    ],
  },
}
