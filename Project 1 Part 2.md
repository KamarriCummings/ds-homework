

```python
import pandas as pd
import os

data = pd.read_csv(os.path.join('..','data','ozone.csv'))
```


    ---------------------------------------------------------------------------

    IOError                                   Traceback (most recent call last)

    <ipython-input-30-80975ec079d5> in <module>()
          2 import os
          3 
    ----> 4 data = pd.read_csv(os.path.join('..','data','ozone.csv'))
    

    /Users/KamarriCummings/anaconda/lib/python2.7/site-packages/pandas/io/parsers.pyc in parser_f(filepath_or_buffer, sep, delimiter, header, names, index_col, usecols, squeeze, prefix, mangle_dupe_cols, dtype, engine, converters, true_values, false_values, skipinitialspace, skiprows, skipfooter, nrows, na_values, keep_default_na, na_filter, verbose, skip_blank_lines, parse_dates, infer_datetime_format, keep_date_col, date_parser, dayfirst, iterator, chunksize, compression, thousands, decimal, lineterminator, quotechar, quoting, escapechar, comment, encoding, dialect, tupleize_cols, error_bad_lines, warn_bad_lines, skip_footer, doublequote, delim_whitespace, as_recarray, compact_ints, use_unsigned, low_memory, buffer_lines, memory_map, float_precision)
        527                     skip_blank_lines=skip_blank_lines)
        528 
    --> 529         return _read(filepath_or_buffer, kwds)
        530 
        531     parser_f.__name__ = name


    /Users/KamarriCummings/anaconda/lib/python2.7/site-packages/pandas/io/parsers.pyc in _read(filepath_or_buffer, kwds)
        293 
        294     # Create the parser.
    --> 295     parser = TextFileReader(filepath_or_buffer, **kwds)
        296 
        297     if (nrows is not None) and (chunksize is not None):


    /Users/KamarriCummings/anaconda/lib/python2.7/site-packages/pandas/io/parsers.pyc in __init__(self, f, engine, **kwds)
        610             self.options['has_index_names'] = kwds['has_index_names']
        611 
    --> 612         self._make_engine(self.engine)
        613 
        614     def _get_options_with_defaults(self, engine):


    /Users/KamarriCummings/anaconda/lib/python2.7/site-packages/pandas/io/parsers.pyc in _make_engine(self, engine)
        745     def _make_engine(self, engine='c'):
        746         if engine == 'c':
    --> 747             self._engine = CParserWrapper(self.f, **self.options)
        748         else:
        749             if engine == 'python':


    /Users/KamarriCummings/anaconda/lib/python2.7/site-packages/pandas/io/parsers.pyc in __init__(self, src, **kwds)
       1117         kwds['allow_leading_cols'] = self.index_col is not False
       1118 
    -> 1119         self._reader = _parser.TextReader(src, **kwds)
       1120 
       1121         # XXX


    pandas/parser.pyx in pandas.parser.TextReader.__cinit__ (pandas/parser.c:3246)()


    pandas/parser.pyx in pandas.parser.TextReader._setup_parser_source (pandas/parser.c:6111)()


    IOError: File ../data/ozone.csv does not exist



```python

```
