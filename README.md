# laughing-disco
Excel *.xlsx component file versioning

## Installation
Add the hooks in this repo's ```git-hooks``` dir into your project's ```.git/hooks/``` directory.

- pre-commit
- post-commit

Set hook permissions
```
chmod 755 .git/hooks/*-commit
```

## Using with Git

Work on your projects as you normally would, when you stage and commit an Excel *.xlsx file, during the commit, it will be automatically unzipped. A new ```.~[my-excel-file].xlsx/``` directory is created containing the expanded excel file components.  This new directory will be committed alongside the source ```[my-excel-file].xlsx``` file.

## NOTE
This is a one-way process.  Changes to the Excel file components are not recompressed.  This is for git diffs and branch comparisons only.