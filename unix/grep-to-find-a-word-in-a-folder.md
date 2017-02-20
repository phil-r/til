# Grep to find a word in a folder


```
grep -nr 'someword' .
```

Where:

`-n` or `--line-number` Each output line is preceded by its relative line number in the file, starting at line 1.  The line number counter is reset for each file processed.

`-R`, `-r` or `--recursive` Recursively search subdirectories listed.

and `.` for current directory. Any other folder can be used, e.g. `./node_modules`
