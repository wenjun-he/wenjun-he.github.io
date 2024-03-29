---
layout: post
title:   文献检索以及引文分析的最佳实践--Pubmed为例
date: 2021-11-10
tags: markdown    
---

# 术语

## Pubmed
PubMed是主要用于检索MEDLINE数据库中生命科学和生物医学引用文献及索引的免费搜索引擎。该系统属于美国国立卫生研究院下属的国家医学图书馆维护的Entrez信息检索系统的一部分
## MeSH
医学主题词（Medical Subject Headings，MeSH，或译医学主题词表）是一部庞大的受控词表（或者说，元数据系统），是广泛应用于医学信息检索的一种工具。在生命科学领域旨在用于标引期刊文献和书籍。
## 引文分析
引文分析是一种文献计量学方法，这种方法主要通过概率论与数理统计对文献的被引用率进行分析。这种方法的主要研究依据是文献、作者、期刊等之间的引证关系。

# 文献检索的最佳实践

## 研究问题：拟定研究问题并进行主题词分解
### 方法1：Buiding Blocks
Building Blocks的方法旨在将问题拆分成几个小点，这些小点将被提炼成几个关键词，而这些关键词将是搜索策略组成的小块。[例子](http://bmcmededuc.biomedcentral.com/articles/10.1186/)如下：

**研究问题：**

​Why is geriatrics not a popular career choice for medical students?

**关键小点：**

1. medical students
2. geriatrics
3. career

**搜索策略(将小点转为主题词，并且找到同义词)：**

1. medical students: medical students - clinial education
2. geriatrics: geriatrics
3. career choice: career - career mobility - career planning - career choice - specialisation

### 方法2：PICO 
For more information please refer to this [article](https://wenjun-he.github.io/2021/09/PICEOST/)

**例子如下：**

Is using antibiotic treatment for appendicitis in adults a safe and effective alternative to an appendectomy?

**PICO分解**

![](/images/blog/PICO_example.png)

**主题词提取**

1. Appendicitis
2. Antibiotics
3. Appendectomy

**[搜索策略案例](/docs/SOP_PubMed_Examples.docx)**

## 搜索手册与日志： 根据搜索手册制定和记录搜索策略

在开始文献检索之前，建议用日志文档进行记录，内容如下：

 - 研究问题
 - 检索日期
 - 所检索的数据库
 - 所检索的记录
 - 研究问题关键词的检索策略
 - 备份检索的结果和检索记录

[Teample Logbook 下载](/docs/Logbook_template.docx)

[Example Logbook 下载](/docs/Logbook_Search_Appendicitis_aug.docx)

## 收集MeSH术语： 制定主题词检索策略

### MeSH作用
我们可以直接在Pubmed上进行检索，但是为什么还要使用MeSH来进行检索呢？
主要是因为MeSH能将某一主题词的变体归于一个主题词中；一个主题词涵盖了该主题词的多种变体。

### 使用流程
#### 了解[MeSH database](https://www.ncbi.nlm.nih.gov/mesh/)的组成

Example of *Antiviral Agents*:
![](/images/blog/mesh_ex.png)

#### 使用方式
主要使用**Add to Search builder** 来构建检索策略。

#### 使用技巧
- **Subheading**: 当主题词比较宽泛的时候，增加子标题会将范围进行缩小。
- **Restrict to MeSH Major Topic**: 此项勾选将把检索的文献的主要主题都限制在此MeSH主题词中。
- **Do not include MeSH terms found below this term in the MeSH hierarchy**: 默认情况下，Pubmed会将主题检索词以下的主题都涵盖在内，如果勾选此项，则不包括下级结构的主题词。
- **Entry Term**: 类似于同义词，这些主题词都会指向该页面的主题词介绍。

## 收集自由文本术语：制定自由文本检索策略
### 自由文本检索策略的重要性
使用MeSH+自由文本检索是最高效的检索文献方式。
因为：
 - 最新发表的文献很可能还没有来得及进行MeSH主题词索引。
 - 不太可能通过一个主题词涵盖所有的研究领域或者研究概念。
 - MeSH可能没有索引到相关文献，即使那篇文献的确跟主题词MeSH相关。

### 进行关键词组成自由文本的技巧
  - Synonyms
  - Singular/plural
  - Deived words
  - Spelling difference
 ![](/images/blog/free_text.png)
  - Look for words used in the abstracts of relevant articles. 
  - Use dictionaries and other reference materials as a source of inspiration.
  - Use the MeSH database: the Entry Terms are synonyms. Use them as **tiab**-terms(search in the title or abstract of the articles.).
  ![](/images/blog/entry_term.png)
## 截断和短语搜索
### 星号正则匹配
对名词的截断并有*号，有利于Pubmed检索所有匹配的主题词。
 - 限定于星号放在主题词最后
 - 截断后至少要包含4个字符
### 短语搜索
如果加上英文双引号，将使得PubMed限定于在该固定名词进行检索。如果不加上双引号，则PubMed检索策略将自动进行主题词拆分等。
## 搜索组合
通过逻辑运算符进行多个语句的整合。逻辑运算符使用关系如下：
![](/images/blog/boolean.png)

组合案例：
![](/images/blog/ex_pubmed.png)


# 文献计量分析

## 相关定义
>* [Bradford's Law](https://zh.wikipedia.org/wiki/%E6%96%87%E7%8D%BB%E8%A8%88%E9%87%8F%E5%AD%B8):发现经常被引用的论文出自少数期刊，这些经常有论文被引用的期刊称之为核心期刊，其与边际期刊之数量呈现1：a：a平方的关系，亦即有报酬率递减的现象。换言之，特定学科之最相关文献集中于少数的核心期刊之中。此结果可作为图书馆在做馆藏发展和馆藏评鉴时的依据，在馆藏发展时，应先将核心期刊列为优先采访的对象，若有剩下预算，再依序进行边际期刊的购买；在馆藏评鉴时，则可根据该馆在各学科当中收录了多少核心期刊，来评断其馆藏品质优劣。
>* Most Local Cited Documents：在当前数据集中高被引文献
>* Most Local Cited References：在当前数据集中高被引的参考文献
>* Reference Spectroscopy：每年参考文献的数量
>* Most Frequent Words：高频词
>* WordCloud：词云
>* TreeMap：树图
>* Word Dynamics：词出现次数，展示词变化趋势
>* Trend Topics：根据今年词出现频次推测热点话题
>* KeyWords Plus: 领域关键词


## Three-Fileds-Plot

桑基图-是使用数据流量进行可视化分析的图表。线条的宽度变化，通过线条宽度变化可以了解数据变化情况。
 - 线条的走向，也就是数据流的走向，我们需要根据线条走向进行数据流变化分析。
 - 线条的宽度变化，通过线条宽度变化可以了解数据变化情况。

 ## 文献期刊分析
 ### Most Relevant Sources
 ### Most Local Cited Sources
 ### Source Impact
 ### Source Dynamic
 ## 作者分析
 ### Most Relevant Authors
 ### Most Local Cited Authors
 ### Authors' Production over Time
 ### Lotka's law
 ### Author Impact
 ### Most Relevant Affiliations
 ### Corresponding Author's Country
 ### Country Scientific Production
 ### Most Cited Countries
 ## 文件分析
# References
>* https://libguides.vu.nl/PMroadmap/introduction

