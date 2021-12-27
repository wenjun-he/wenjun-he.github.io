---
layout: post
title: Learning R
date: 2021-08-09
tags: markdown    
---

## Using R in an elegant way

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

### Get the directory of current R script
```R
dirname(rstudioapi::getSourceEditorContext()$path)
```

### Use the character to build the formula
```R
formula_character <- paste("Surv(", "variable1", ",", "variable2", ")~")
fmla <- as.formula(paste(formula_character,paste("variable3", collapse = "+")))
```

### When the KM curve crossed in survival analysis
```R
# R package (ComparisonSurv)
crosspoint()
Long.test()
Short.test()
```

### Examples to plot and save
```R
# Plot to the console and then save as the pdf file
ggplot(data, aes(x = x_variable,fill=arm)) + 
  geom_histogram(binwidth = 0.1,position ="dodge",alpha=0.3)+
  geom_density(alpha=0.5,adjust=0.2,size=0.3) + 
  facet_grid(arm ~.) +
  scale_fill_discrete(name = "Experimental\nCondition", labels = c("Control","Treatment"))+
  xlab("Adherence of T1")+
  ylab("Count")+
  theme_classic()
ggsave("save.pdf", device = "pdf")
```
### get function to exchange the character into variable name
```R
plot_bar <- function(dataframe, var_plot, var_group, cha_xlab, cha_scale, title){
  ggplot(data=dataframe,mapping=aes(x=forcats::fct_infreq(get(var_group)), fill=get(var_plot))) +
    geom_bar(stat="count",position="dodge")+
    xlab(cha_xlab)+
    ggtitle(title)+
    scale_fill_discrete(name = cha_scale)+
    theme_classic()+
    theme(axis.text.x = element_text(angle = 60, hjust = 0.5, vjust = 0.5))
}
```
### Others

*  To check some useful functions in [Cookbook for R](https://openbiox.github.io/Cookbook-for-R-Chinese/index.html)
* When seleting the color for ggplot2, please refer this [website](https://colorbrewer2.org/)
* When conducting analysis, it is a good way to maintain a R scripts containing the functions mostly used.