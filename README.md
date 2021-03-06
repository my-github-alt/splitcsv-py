# splitcsv


🖥️ `python splitcsv.py -h`

```
usage: python splitcsv.py </path/to/file.csv> [options] (-n | -r)

This script splits the given CSV-file evenly into a given count of parts.

Be aware!
    Can't split up the CSV-file if number of splits are larger than available rows.
    If split results into an uneven split, rows (multiple) can be discarded.

Examples:
    Split CSV-file in 3 parts
        python splitcsv.py /path/to/file.csv -n 3

    Name the output files. (example output: ./A.csv and ./B.csv)
        python splitcsv.py ./file.csv -r A B

    Split CSV-file in 2 parts and save parts to relative directory
        python splitcsv.py ./file.csv -o ./out/dir/

    Give the split up CSV-files a prefix (example output: ./csv_file1.csv, etc.)
        python splitcsv.py ./file.csv -p csv_

positional arguments:
  csvfile               CSV-file to split

options:
  -h, --help            show this help message and exit
  -n SPLITNUM, --splitnum SPLITNUM
                        n-times to split, default: 2
  -r RENAME [RENAME ...], --rename RENAME [RENAME ...]
                        names for the new files, minimal arguments: 2

optional:
  -o OUTDIR, --outdir OUTDIR
                        directory to place the new files, default: same as csvfile
  -p PREFIX, --prefix PREFIX
                        prefix for file names, default: nothing
```