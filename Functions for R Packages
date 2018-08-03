###  R Packages

############################################
## function for installing multiple packages 
############################################
ipak <- function(pkg){
  new.pkg <- pkg[!(pkg %in% installed.packages()[, "Package"])]
  if (length(new.pkg)) 
    install.packages(new.pkg, dependencies = TRUE)
  sapply(pkg, require, character.only = TRUE)
}

# usage
pkg <- c("ggplot2", "dplyr", "reshape2", "RColorBrewer", "stringr", "data.table")
ipak(pkg)


###############################################
## list all the functions in a specific package
###############################################

lsp <- function(package, all.names = FALSE, pattern) 
{
  package <- deparse(substitute(package))
  ls(
    pos = paste("package", package, sep = ":"), 
    all.names = all.names, 
    pattern = pattern
  )
}

# usage
lsp(ggplot2, pattern = "geom")
