---
layout: post
title:   Bland-Altman-Plots
date: 2021-11-12
tags: markdown    
---
# Definition
Bland-Altman plots are a well established method to check the agreement of different measurement methods or the retest-reliability of a single measurement method. (Apparently, Bland-Altman plots are otherwise known as Tukey’s Mean Difference Plot.) 

# Features of plot
The Bland-Altman chart is a scatterplot with the difference of the two measurements for each sample on the vertical axis and the average of the two measurements on the horizontal axis. Three horizontal reference lines are superimposed on the scatterplot - one line at the average difference between the measurements, along with lines to mark the upper and lower control limits of plus and minus 1.96*sigma, respectively, where sigma is the standard deviation of the measurement differences.

![](/images/blog/ba.png)

# Interpretation
Bland-Altman plots are generally interpreted informally, without further analyses. Ask yourself these questions:

>* (1) How big is the average discrepancy between methods (the bias)? You must interpret this clinically. Is the discrepancy large enough to be important? This is a clinical question, not a statistical one.
>* (2) How wide are the limits of agreement? If it is wide (as defined clinically), the results are ambiguous. If the limits are narrow (and the bias is tiny), then the two methods are essentially equivalent.
>* (3) Is there a trend? Does the difference between methods tend to get larger (or smaller) as the average increases?
>* (4) Is the variability consistent across the graph? Does the scatter around the bias line get larger as the average gets higher?

# Example of R code
```R
library(BlandAltmanLeh)
A <- c(-0.358, 0.788, 1.23, -0.338, -0.789, -0.255, 0.645, 0.506, 
0.774, -0.511, -0.517, -0.391, 0.681, -2.037, 2.019, -0.447, 
0.122, -0.412, 1.273, -2.165)
B <- c(0.121, 1.322, 1.929, -0.339, -0.515, -0.029, 1.322, 0.951, 
0.799, -0.306, -0.158, 0.144, 1.132, -0.675, 2.534, -0.398, 0.537, 
0.173, 1.508, -1.955)
sex <- c( 1,1,1,1,2,2,2,1,1,1,2,2,2,2,2,1,1,2,1,2)

ba.stats <- bland.altman.stats(A, B)

plot(ba.stats$means, ba.stats$diffs, col=sex, 
     sub=paste("critical difference is", round(ba.stats$critical.diff,4)),
     main="make your own graph easily", ylim=c(-1.5,1.5), pch=18-sex)
abline(h = ba.stats$lines, lty=c(2,3,2), col=c("lightblue","blue","lightblue"), 
       lwd=c(3,2,3))
legend(x = "topright", legend = c("male","female"), fill = 1:2)
```


# Reference
>* https://www.researchgate.net/post/How-can-I-interpret-this-Bland-and-Altman-plot-fully
>* https://cran.r-project.org/web/packages/BlandAltmanLeh/vignettes/Intro.html
