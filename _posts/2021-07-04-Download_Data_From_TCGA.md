---
layout: post
title: How to download data from TCGA database
date: 2021-07-20 
tags: markdown    
---

## 什么是TCGA
TCGA是由National Cancer Institute ( NCI, 美国国家癌症研究所) 和  National Human Genome Research Institute (NHGRI, 国家人类基因组研究所) 合作建立的癌症研究项目，通过收集整理癌症相关的各种组学数据，提供了一个大型的，免费的癌症研究参考数据库。 官方提供了对应的下载工具Genomic Data Commons Datga Portal,  简称GDC, 网址如下:https://portal.gdc.cancer.gov/
## 下载TCGA数据的三种方式
### 官方下载方式
* TCGA官网的data-portal: portal.gdc.cancer.gov
* 优点：数据最全，更新最快
* 缺点：下载速度慢，不利于进一步分析。
### Firehose网页下载方式
* Firehose服务器：gdac.broadinstitute.org
* 优点：这里的数据经过了简单的合并，将每种癌症相同类型的数据合并到了一个文件中，下载方式最简单且可以直接下一步分析
* 缺点：临床随访数据几乎没有更新。
### 使用R包的下载方式
* R包包括TCGA-ASSEMBLER 、TCGA2STAT、GDCRNATOOLS等。最常用的是TCGAbiolinks包。
* 优点：包更新比较快，同时也是直接下载官网数据保证准确性，同时该包的使用者比较多，利于进一步分析和挖掘。
## 使用TCGAbiolinks包进行数据下载
### 查询数据  GDCquery()
### 下载数据  getResults()
### 保存整理数据 GDCprepare()
## 参考材料
>* [TCGA数据库介绍以及下载方式小结](https://www.jianshu.com/p/7ba924d4b296)
>* [TCGA数据下载—TCGAbiolinks包参数详解](https://www.omicsclass.com/article/1060)
