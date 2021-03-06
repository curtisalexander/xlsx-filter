# filter `xlsx`
Interactively filter an `xlsx` file.  Assumes that the data within the `xlsx` file is in a tabular format and that the table has a header.

## xlsx-dt
Filter a table from an `xlsx` file interactively within the browser.  The script creates a simple [Shiny](http://shiny.rstudio.com) app that opens in the browser, allowing the user to interact with (including filtering) the table of interest.

The script makes use of the R package [DT](https://rstudio.github.io/DT/) which is an R interface to the JavaScript [DataTables](https://datatables.net) library.

### Usage
There is an option to include a specific sheet or simply read in the first sheet.  After execution, a browser window will open allowing the user to interact with the table.

```bash
# read the first sheet
xlsx-dt myfile.xlsx
```

```bash
# read a specific sheet
xlsx-dt myfile.xlsx "mysheetname"
```

### Requirements
* `Rscript` must be on the user's search `PATH`
* The `DT`, `readxl`, and `shiny` packages must be installed

```R
install.packages("DT")
install.packages("readxl")
install.packages("shiny")
```

## xlsx-fzf
Filter a table from an `xlsx` file interactively within the command line.  The script reads a table from an `xlsx` file and pipes the result to the [fzf](https://github.com/junegunn/fzf) program.

### Usage
There is an option to include a specific sheet or simply read in the first sheet.  After execution, the user is dropped into `fzf` allowing the user to interact with the table.

```bash
# read the first sheet
xlsx-fzf myfile.xlsx
```

```bash
# read a specific sheet
xlsx-fzf myfile.xlsx "mysheetname"
```

### Requirements
* `Rscript` must be on the user's search `PATH`
* The `readxl` package must be installed

```R
install.packages("readxl")
```

* The [fzf](https://github.com/junegunn/fzf) program must be installed.  On OS X it can simply be installed via [Homebrew](http://brew.sh).

```bash
brew install fzf
```
