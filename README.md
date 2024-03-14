# PFAS Automated Quantitation (PAQ)

## Overview

The purpose of this project is to streamline the processing of PFAS Quantitation Steps. For details around these steps, please see this [Powerpoint Presentation](https://uflorida-my.sharepoint.com/:p:/g/personal/camden_camacho_ufl_edu/EaVbQvErEnNKpVYSX4BhQ-EB34x2tahj1mSEbT9KeP13_Q?rtime=REwgXe8f20g).

## Dev Setup

### R Setup

* Set install R Version 4.3.2. It is recommended to use [rig](https://github.com/r-lib/rig)
* Install RStudio

### Project Setup

1. Spin up R Studio or an R Console with R 4.2.2 (with the command `rig rstudio {R Version}` and for Mac, `rig rstudio 4.2-arm64`)
2. There is a file [setup.R](./setup.R) that includes a list of commands that will set a project up. To run it, you can do Run `source("setup.R")` in the R Console.

### Package Management

Packages are both managed with the DESCRIPTION file and specifically installed version with an renv.lock file. 

* When adding a package, you should use `usethis::use_package("{PackageName}", min_version = TRUE)` to add it to the DESCRIPTION file.
* You need to install the package with `renv::install("{PackageName}"")`
* You also need to perform an `renv::snapshot()` to update the renv.lock file.

### code formatting

This project uses [styler](https://styler.r-lib.org/) to auto-format code.

### renv setup

* Used `renv::settings$snapshot.type("explicit")` to manage packages using the DESCRIPTION file.