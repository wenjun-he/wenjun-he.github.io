---
layout: post
title: Learning R
date: 2021-08-09
tags: markdown    
---

# Using R in an elegant way
### To check all the packages installed
```R
packages = c("MLmetrics","boot")
package.check <- lapply(
  packages,
  FUN = function(x) {
    if (!require(x, character.only = TRUE)) {
      install.packages(x, dependencies = TRUE)
      library(x, character.only = TRUE)
    }
  }
)
```