

## Project for Advanced Data Science course

Prof. Massimo Franceschet
write by dott. Riccardo Ferrarese



Instruction for project's set up in the first section of the final report.

Content of directory: 
-  Project: dir with all the file and environment of the project 
  - renv: dir with R env.  
  - Report: dir with .md and .html final report
  - src: dir with .R file 
  - Data: dir with all the data 
  - bibliography.bib: file for prettifying the management of citation
  
- PythonScript: dir with the script for scrapping Reddit's data 


###### Python env

View README.md in _PythonScript_ dir.


###### R env 

For manage R environment, setup working directory and install _renv_ library: 

```shell
setwd("~./<clone-dir>/Project")
install.packages("renv")
```

Initialise renv and restore: 

```r
# renv::init()
renv::restore()			# if file .lock exist 
```

### Set up Project on LINUX with CONDA

All the configuration for library and environments is a report's section. But here is a little preview, only for expert users!

We will use conda to manage virtual environments. Create the environment from file in git: 

```shell
conda env create -f environment.yml --name dsproject
```

Type the next command for check the env and activate it: 

```shell
conda env list
conda activate dsproject
```

For trouble use pip: 

```shell
conda install -n dsproject pip
conda activate dsprojectc
```

For export modify env, without prefix line: 

```{shell}
conda env export | grep -v "^prefix: " > environment.yml
```











---

_note_ 

​	For reading the .Rmd file, and not for its execution, I like to use [typora](https://typora.io/).


---



Open branches for future improvements: 

- shiny app -- modular r shiny for visualize all the data 
- aws -- use AWS for continuously extract data
- spacy -- improve dictionary

###### Spacy Set Up

In R Interactive, with conda installed: 

```r
install.packages("spacyr")

library(reticulate)
library(spacyr)

spacy_install()
conda_list()		# see if spacy_condaenv was created 
spacy_initialize()
```
