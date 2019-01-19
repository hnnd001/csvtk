- [csvtk v0.17.0](https://github.com/shenwei356/csvtk/releases/tag/v0.17.0)
[![Github Releases (by Release)](https://img.shields.io/github/downloads/shenwei356/csvtk/v0.17.0/total.svg)](https://github.com/shenwei356/csvtk/releases/tag/v0.17.0)
    - new command: `csvtk add-header` and `csvtk del-header`: add/delete column names. [#62](https://github.com/shenwei356/csvtk/issues/62)
- [csvtk v0.16.0](https://github.com/shenwei356/csvtk/releases/tag/v0.16.0)
[![Github Releases (by Release)](https://img.shields.io/github/downloads/shenwei356/csvtk/v0.16.0/total.svg)](https://github.com/shenwei356/csvtk/releases/tag/v0.16.0)
    - new command: `csvtk csv2json`: convert CSV to JSON format.
    - remove comand: `csvtk stats2`.
    - new command `csvtk summary`: summary statistics of selected digital fields (groupby group fields), [usage and examples](https://bioinf.shenwei.me/csvtk/usage/#stats). [#59](https://github.com/shenwei356/csvtk/issues/59)
    - `csvtk replace`: add flag `--nr-width`: minimum width for {nr} in flag -r/--replacement. e.g., formating "1" to "001" by `--nr-width 3` (default 1)
    - `csvtk rename2/replace`: add flag `-A, --kv-file-all-left-columns-as-value`, for treating all columns except 1th one as value for kv-file with more than 2 columns. [#56](https://github.com/shenwei356/csvtk/issues/56)
- [csvtk v0.15.0](https://github.com/shenwei356/csvtk/releases/tag/v0.15.0)
[![Github Releases (by Release)](https://img.shields.io/github/downloads/shenwei356/csvtk/v0.15.0/total.svg)](https://github.com/shenwei356/csvtk/releases/tag/v0.15.0)
    - `csvtk`: add global flag `-E/--ignore-empty-row` to skip empty row. [#50](https://github.com/shenwei356/csvtk/issues/50)
    - `csvtk mutate2`: add flag `-s/--digits-as-string` for not converting big digits into scientific notation. [#46](https://github.com/shenwei356/csvtk/issues/46)
    - `csvtk sort`: add support for sorting in natural order. [#49](https://github.com/shenwei356/csvtk/issues/49)
- [csvtk v0.14.0](https://github.com/shenwei356/csvtk/releases/tag/v0.14.0)
    [![Github Releases (by Release)](https://img.shields.io/github/downloads/shenwei356/csvtk/v0.14.0/total.svg)](https://github.com/shenwei356/csvtk/releases/tag/v0.14.0)
    - `csvtk`: **supporting multi-line fields by replacing [multicorecsv](https://github.com/mzimmerman/multicorecsv ) with standard library [encoding/csv](https://golang.org/pkg/encoding/csv/),
    while losing [support for metaline](https://github.com/shenwei356/csvtk/issues/13) which was supported since v0.7.0**. It also gain a little speedup.
    - `csvtk sample`: add flag `-n/--line-number` to print line number as the first column ("n")
    - `csvtk filter2`: fix bug when column names start with digits, e.g., `1000g2015aug` ([#44](https://github.com/shenwei356/csvtk/issues/44))
    - `csvtk rename2`: add support for similar repalecement symbols `{kv} and {nr}` in `csvtk replace`
- [csvtk v0.13.0](https://github.com/shenwei356/csvtk/releases/tag/v0.13.0)
[![Github Releases (by Release)](https://img.shields.io/github/downloads/shenwei356/csvtk/v0.13.0/total.svg)](https://github.com/shenwei356/csvtk/releases/tag/v0.13.0)
    - new command `concat` for concatenating CSV/TSV files by rows [#38](https://github.com/shenwei356/csvtk/issues/38)
    - `csvtk`: add support for environment variables for frequently used global flags [#39](https://github.com/shenwei356/csvtk/issues/39)
        - `CSVTK_T` for flag `-t/--tabs`
        - `CSVTK_H` for flag `-H/--no-header-row`
    - `mutate2`: add support for eval expression WITHOUT column index symbol, so we can add some string constants [#37](https://github.com/shenwei356/csvtk/issues/37)
    - `pretty`: better support for files with duplicated column names
- [csvtk v0.12.0](https://github.com/shenwei356/csvtk/releases/tag/v0.12.0)
[![Github Releases (by Release)](https://img.shields.io/github/downloads/shenwei356/csvtk/v0.12.0/total.svg)](https://github.com/shenwei356/csvtk/releases/tag/v0.12.0)
    - new command `collapse`: collapsing one field with selected fields as keys
    - `freq`: keeping orignal order of keys by default
    - `split`:
        - performance improvement
        - add option `-G/--out-gzip` for forcing output gzipped file
- [csvtk v0.11.0](https://github.com/shenwei356/csvtk/releases/tag/v0.11.0)
[![Github Releases (by Release)](https://img.shields.io/github/downloads/shenwei356/csvtk/v0.11.0/total.svg)](https://github.com/shenwei356/csvtk/releases/tag/v0.11.0)
    - add command `split` to split CSV/TSV into multiple files according to column values
    - add command `splitxlxs` to split XLSX sheet into multiple sheets according to column values
    - `csvtk`, automatically check BOM (byte-order mark) and discard it
- [csvtk v0.10.0](https://github.com/shenwei356/csvtk/releases/tag/v0.10.0)
[![Github Releases (by Release)](https://img.shields.io/github/downloads/shenwei356/csvtk/v0.10.0/total.svg)](https://github.com/shenwei356/csvtk/releases/tag/v0.10.0)
    - add subcommand `xlsx2csv` to convert XLSX to CSV format
    - `grep`, `filter`, `filter2`: add flag `-n/--line-number` to print line-number as the first column
    - `cut`: add flag `-i/--ignore-case` to ignore case of column name
- [csvtk v0.9.1](https://github.com/shenwei356/csvtk/releases/tag/v0.9.1)
[![Github Releases (by Release)](https://img.shields.io/github/downloads/shenwei356/csvtk/v0.9.1/total.svg)](https://github.com/shenwei356/csvtk/releases/tag/v0.9.1)
    - `csvtk replace`: fix bug when replacing with key-value pairs brought in v0.8.0
- [csvtk v0.9.0](https://github.com/shenwei356/csvtk/releases/tag/v0.9.0)
[![Github Releases (by Release)](https://img.shields.io/github/downloads/shenwei356/csvtk/v0.9.0/total.svg)](https://github.com/shenwei356/csvtk/releases/tag/v0.9.0)
    - add subcommand `csvtk mutate2`: create new column from selected fields by **awk-like artithmetic/string expressions**
    - add new command `genautocomplete` to generate **shell autocompletion** script!
- [csvtk v0.8.0](https://github.com/shenwei356/csvtk/releases/tag/v0.8.0)
[![Github Releases (by Release)](https://img.shields.io/github/downloads/shenwei356/csvtk/v0.8.0/total.svg)](https://github.com/shenwei356/csvtk/releases/tag/v0.8.0)
    - **new command `csvtk gather` for gathering columns into key-value pairs**.
    - `csvtk sort`: support **sorting by user-defined order**.
    - fix bug of *unselecting field*: wrongly reporting error of fields not existing.
    affected commands: `cut`, `filter`, `fitler2`, `freq`, `grep`, `inter`, `mutate`,
    `rename`, `rename2`, `replace`, `stats2`, `uniq`.
    - update help message of flag `-F/--fuzzy-fields`.
    - update help message of global flag `-t`, which overrides both `-d` and `-D`.
      If you want other delimiter for tabular input, use `-t $'\t' -D "delimiter"`.
- [csvtk v0.7.1](https://github.com/shenwei356/csvtk/releases/tag/v0.7.1)
[![Github Releases (by Release)](https://img.shields.io/github/downloads/shenwei356/csvtk/v0.7.1/total.svg)](https://github.com/shenwei356/csvtk/releases/tag/v0.7.1)
    - `csvtk plot box` and `csvtk plot line`: fix bugs for special cases of input
    - compile with go1.8.1
- [csvtk v0.7.0](https://github.com/shenwei356/csvtk/releases/tag/v0.7.0)
[![Github Releases (by Release)](https://img.shields.io/github/downloads/shenwei356/csvtk/v0.7.0/total.svg)](https://github.com/shenwei356/csvtk/releases/tag/v0.7.0)
    - fig bug of "stricter field checking" in v0.6.0 and v0.6.1 when using flag `-F/--fuzzy-fields`
    - `csvtk pretty` and `csvtk csv2md`: add attention that
      these commands treat the first row as header line and require them to be unique.
    - `csvtk stat` renamed to `csvtk stats`, old name is still available as an alias.
    - `csvtk stat2` renamed to `csvtk stats2`, old name is still available as an alias.
    - [issues/13](https://github.com/shenwei356/csvtk/issues/13) **seamlessly support for data with meta line of separator declaration used by MS Excel**.
- [csvtk v0.6.1](https://github.com/shenwei356/csvtk/releases/tag/v0.6.1)
[![Github Releases (by Release)](https://img.shields.io/github/downloads/shenwei356/csvtk/v0.6.1/total.svg)](https://github.com/shenwei356/csvtk/releases/tag/v0.6.1)
    - `csvtk cut`: minor bug: panic when no fields given. i.e., `csvtk cut`.
All relevant commands have been fixed.
- [csvtk v0.6.0](https://github.com/shenwei356/csvtk/releases/tag/v0.6.0)
[![Github Releases (by Release)](https://img.shields.io/github/downloads/shenwei356/csvtk/v0.6.0/total.svg)](https://github.com/shenwei356/csvtk/releases/tag/v0.6.0)
    - `csvtk grep`: **large performance improvement by discarding goroutine** (multiple threads),
      and **keeping output in order of input**.
    - Better column name checking and **stricter field checking,
      fields out of range are not ignored now**.
      Affected commands include `cut`, `filter`, `freq`, `grep`, `inter`, `mutate`,
      `rename`, `rename2`, `replace`, `stat2`, and `uniq`.
    - **New command: `csvtk filter2`, filtering rows by artithmetic/string expressions like `awk`**.
- [csvtk v0.5.0](https://github.com/shenwei356/csvtk/releases/tag/v0.5.0)
[![Github Releases (by Release)](https://img.shields.io/github/downloads/shenwei356/csvtk/v0.5.0/total.svg)](https://github.com/shenwei356/csvtk/releases/tag/v0.5.0)
    - `csvtk cut`: delete flag `-n/--names`, move it to a new command `csvtk headers`
    - new command: `csvtk headers`
    - new command: `csvtk head`
    - new command: `csvtk sample`
- [csvtk v0.4.6](https://github.com/shenwei356/csvtk/releases/tag/v0.4.6)
[![Github Releases (by Release)](https://img.shields.io/github/downloads/shenwei356/csvtk/v0.4.6/total.svg)](https://github.com/shenwei356/csvtk/releases/tag/v0.4.6)
    - `csvtk grep`: fix result highlight when flag `-v` is on.
- [csvtk v0.4.5](https://github.com/shenwei356/csvtk/releases/tag/v0.4.5)
[![Github Releases (by Release)](https://img.shields.io/github/downloads/shenwei356/csvtk/v0.4.5/total.svg)](https://github.com/shenwei356/csvtk/releases/tag/v0.4.5)
    - `csvtk join`: support the 2nd or later files with entries with same ID.
- [csvtk v0.4.4](https://github.com/shenwei356/csvtk/releases/tag/v0.4.4)
[![Github Releases (by Release)](https://img.shields.io/github/downloads/shenwei356/csvtk/v0.4.4/total.svg)](https://github.com/shenwei356/csvtk/releases/tag/v0.4.4)
    - add command `csvtk freq`: frequencies of selected fields
    - add lots of examples in [usage page](http://bioinf.shenwei.me/csvtk/usage/)
- [csvtk v0.4.3](https://github.com/shenwei356/csvtk/releases/tag/v0.4.3)
[![Github Releases (by Release)](https://img.shields.io/github/downloads/shenwei356/csvtk/v0.4.3/total.svg)](https://github.com/shenwei356/csvtk/releases/tag/v0.4.3)
    - improvement of using experience: flag `-n` is not required anymore when flag `-H` in `csvtk mutate`
- [csvtk v0.4.2](https://github.com/shenwei356/csvtk/releases/tag/v0.4.2)
[![Github Releases (by Release)](https://img.shields.io/github/downloads/shenwei356/csvtk/v0.4.2/total.svg)](https://github.com/shenwei356/csvtk/releases/tag/v0.4.2)
    - fix highlight bug of `csvtk grep`: if the pattern matches multiple parts,
    the text will be wrongly edited.
    - changes: disable highlight when pattern file given.
    - change the default output of all ploting commands to STDOUT, now you can
    pipe the image to "display" command of Imagemagic.
- [csvtk v0.4.1](https://github.com/shenwei356/csvtk/releases/tag/v0.4.1)
[![Github Releases (by Release)](https://img.shields.io/github/downloads/shenwei356/csvtk/v0.4.1/total.svg)](https://github.com/shenwei356/csvtk/releases/tag/v0.4.1)
    - Nothing changed. Just fix the links due to inappropriate deployment of v0.4.0
- [csvtk v0.4.0](https://github.com/shenwei356/csvtk/releases/tag/v0.4.0)
[![Github Releases (by Release)](https://img.shields.io/github/downloads/shenwei356/csvtk/v0.4.0/total.svg)](https://github.com/shenwei356/csvtk/releases/tag/v0.4.0)
    - add flag for `csvtk replace`: `-K` (`--keep-key`) keep the key as value when
    no value found for the key. This is open in default in previous versions.
- [csvtk v0.3.9](https://github.com/shenwei356/csvtk/releases/tag/v0.3.9)
  [![Github Releases (by Release)](https://img.shields.io/github/downloads/shenwei356/csvtk/v0.3.9/total.svg)](https://github.com/shenwei356/csvtk/releases/tag/v0.4.0)
    - fix bug: header row incomplete in `csvtk sort` result
- [csvtk v0.3.8.1](https://github.com/shenwei356/csvtk/releases/tag/v0.3.8.1)
  [![Github Releases (by Release)](https://img.shields.io/github/downloads/shenwei356/csvtk/v0.3.8.1/total.svg)](https://github.com/shenwei356/csvtk/releases/tag/v0.3.8.1)
    - fix bug of flag parsing library [pflag](https://github.com/spf13/pflag),
    [detail](https://github.com/spf13/pflag/pull/98).
    The bug affected the `csvtk grep -r -p`, when value of `-p` contain "[" and "]"
    at the beginning or end, they are wrongly parsed.
- [csvtk v0.3.8](https://github.com/shenwei356/csvtk/releases/tag/v0.3.8)
  [![Github Releases (by Release)](https://img.shields.io/github/downloads/shenwei356/csvtk/v0.3.8/total.svg)](https://github.com/shenwei356/csvtk/releases/tag/v0.3.8)
    - new feature: `csvtk cut` supports ordered fields output. e.g., `csvtk cut -f 2,1`
      outputs the 2nd column in front of 1th column.
    - new commands: `csvtk plot` can plot three types of plots by subcommands:
        - `csvtk plot hist`: histogram
        - `csvtk plot box`: boxplot
        - `csvtk plot line`: line plot and scatter plot
- [csvtk v0.3.7](https://github.com/shenwei356/csvtk/releases/tag/v0.3.7)
  [![Github Releases (by Release)](https://img.shields.io/github/downloads/shenwei356/csvtk/v0.3.7/total.svg)](https://github.com/shenwei356/csvtk/releases/tag/v0.3.7)
    - fix a serious bug of using negative field of column name, e.g. `-f "-id"`
- [csvtk v0.3.6](https://github.com/shenwei356/csvtk/releases/tag/v0.3.6)
  [![Github Releases (by Release)](https://img.shields.io/github/downloads/shenwei356/csvtk/v0.3.6/total.svg)](https://github.com/shenwei356/csvtk/releases/tag/v0.3.6)
    - `csvtk replace` support replacement symbols `{nr}` (record number)
      and `{kv}` (corresponding value of the key ($1) by key-value file)
- [csvtk v0.3.5.2](https://github.com/shenwei356/csvtk/releases/tag/v0.5.2)
  [![Github Releases (by Release)](https://img.shields.io/github/downloads/shenwei356/csvtk/v0.3.5.2/total.svg)](https://github.com/shenwei356/csvtk/releases/tag/v0.3.5.2)
    - add flag `--fill` for `csvtk join`, so we can fill the unmatched data
    - fix typo
- [csvtk v0.3.5.1](https://github.com/shenwei356/csvtk/releases/tag/v0.3.5.1)
  [![Github Releases (by Release)](https://img.shields.io/github/downloads/shenwei356/csvtk/v0.3.5.1/total.svg)](https://github.com/shenwei356/csvtk/releases/tag/v0.3.5.1)
    - fix minor bug of reading lines ending with `\r\n` from a dependency package
- [csvtk v0.3.5](https://github.com/shenwei356/csvtk/releases/tag/v0.3.5)
  [![Github Releases (by Release)](https://img.shields.io/github/downloads/shenwei356/csvtk/v0.3.5/total.svg)](https://github.com/shenwei356/csvtk/releases/tag/v0.3.5)
    - fix minor bug of `csv2md`
    - add subcommand `version` which could check for update
- [csvtk v0.3.4](https://github.com/shenwei356/csvtk/releases/tag/v0.3.4)
  [![Github Releases (by Release)](https://img.shields.io/github/downloads/shenwei356/csvtk/v0.3.4/total.svg)](https://github.com/shenwei356/csvtk/releases/tag/v0.3.4)
    - fix bug of `csvtk replace` that head row should not be edited.
- [csvtk v0.3.3](https://github.com/shenwei356/csvtk/releases/tag/v0.3.3)
  [![Github Releases (by Release)](https://img.shields.io/github/downloads/shenwei356/csvtk/v0.3.3/total.svg)](https://github.com/shenwei356/csvtk/releases/tag/v0.3.3)
    - fix bug of `csvtk grep -t -P`
- [csvtk v0.3.2](https://github.com/shenwei356/csvtk/releases/tag/v0.3.2)
  [![Github Releases (by Release)](https://img.shields.io/github/downloads/shenwei356/csvtk/v0.3.2/total.svg)](https://github.com/shenwei356/csvtk/releases/tag/v0.3.2)
    - fix bug of `inter`
- [csvtk v0.3.1](https://github.com/shenwei356/csvtk/releases/tag/v0.3.1)
  [![Github Releases (by Release)](https://img.shields.io/github/downloads/shenwei356/csvtk/v0.3.1/total.svg)](https://github.com/shenwei356/csvtk/releases/tag/v0.3.1)
    - add support of search multiple fields for `grep`
- [csvtk v0.3](https://github.com/shenwei356/csvtk/releases/tag/v0.3)
  [![Github Releases (by Release)](https://img.shields.io/github/downloads/shenwei356/csvtk/v0.3/total.svg)](https://github.com/shenwei356/csvtk/releases/tag/v0.3)
    - add subcommand `csv2md`
- [csvtk v0.2.9](https://github.com/shenwei356/csvtk/releases/tag/v0.2.9)
  [![Github Releases (by Release)](https://img.shields.io/github/downloads/shenwei356/csvtk/v0.2.9/total.svg)](https://github.com/shenwei356/csvtk/releases/tag/v0.2.9)
    - add more flags to subcommand `pretty`
    - fix bug of `csvtk cut -n`
    - add subcommand `filter`
- [csvtk v0.2.8](https://github.com/shenwei356/csvtk/releases/tag/v0.2.8)
  [![Github Releases (by Release)](https://img.shields.io/github/downloads/shenwei356/csvtk/v0.2.8/total.svg)](https://github.com/shenwei356/csvtk/releases/tag/v0.2.8)
    - add subcommand `pretty` -- convert CSV to readable aligned table
- [csvtk v0.2.7](https://github.com/shenwei356/csvtk/releases/tag/v0.2.7)
  [![Github Releases (by Release)](https://img.shields.io/github/downloads/shenwei356/csvtk/v0.2.7/total.svg)](https://github.com/shenwei356/csvtk/releases/tag/v0.2.7)
    - fix highlight failing in windows
- [csvtk v0.2.6](https://github.com/shenwei356/csvtk/releases/tag/v0.2.6)
  [![Github Releases (by Release)](https://img.shields.io/github/downloads/shenwei356/csvtk/v0.2.6/total.svg)](https://github.com/shenwei356/csvtk/releases/tag/v0.2.6)
    - fix one error message of `grep`
    - highlight matched fields in result of `grep`
- [csvtk v0.2.5](https://github.com/shenwei356/csvtk/releases/tag/v0.2.5)
  [![Github Releases (by Release)](https://img.shields.io/github/downloads/shenwei356/csvtk/v0.2.5/total.svg)](https://github.com/shenwei356/csvtk/releases/tag/v0.2.5)
    - fix bug of `stat` that failed to considerate files with header row
    - add subcommand `stat2` - summary of selected number fields
    - make the output of `stat` prettier
- [csvtk v0.2.4](https://github.com/shenwei356/csvtk/releases/tag/v0.2.4)
  [![Github Releases (by Release)](https://img.shields.io/github/downloads/shenwei356/csvtk/v0.2.4/total.svg)](https://github.com/shenwei356/csvtk/releases/tag/v0.2.4)
    - fix bug of handling comment lines
    - add some notes before using csvtk
- [csvtk v0.2.3](https://github.com/shenwei356/csvtk/releases/tag/v0.2.3)
  [![Github Releases (by Release)](https://img.shields.io/github/downloads/shenwei356/csvtk/v0.2.3/total.svg)](https://github.com/shenwei356/csvtk/releases/tag/v0.2.3)
    - add flag `--colnames` to `cut`
    - flag `-f` (`--fields`) of `join` supports single value now
- [csvtk v0.2.2](https://github.com/shenwei356/csvtk/releases/tag/v0.2.2)
  [![Github Releases (by Release)](https://img.shields.io/github/downloads/shenwei356/csvtk/v0.2.2/total.svg)](https://github.com/shenwei356/csvtk/releases/tag/v0.2.2)
    - add flag `--keep-unmathed` to `join`
- [csvtk v0.2](https://github.com/shenwei356/csvtk/releases/tag/v0.2)
  [![Github Releases (by Release)](https://img.shields.io/github/downloads/shenwei356/csvtk/v0.2/total.svg)](https://github.com/shenwei356/csvtk/releases/tag/v0.2)
    - finish almost functions
- [csvtk v0.2.1](https://github.com/shenwei356/csvtk/releases/tag/v0.2.1)
  [![Github Releases (by Release)](https://img.shields.io/github/downloads/shenwei356/csvtk/v0.2.1/total.svg)](https://github.com/shenwei356/csvtk/releases/tag/v0.2.1)
    - fix bug of `mutate`