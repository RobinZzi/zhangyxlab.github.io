---
layout: page-fullwidth
skip_boilerplate: True
title: "Learning Bioinformatics"
#subheadline: "Getting started in Zhang lab"
#teaser: "The documentation is a work in progress..."
permalink: "/onboarding/learning_bioinformatics/"
header:
#   image: "header_roadmap_2.jpg"
   background-color: "#FFFFFF"
---
<div class="row">
<div class="medium-4 columns" markdown="1">
<div class="panel radius" markdown="1">
**Table of Contents**
{: #toc }
*  TOC
{:toc}

</div>
{% include _onboarding_sidebar.html %}
</div><!-- /.medium-4.columns __ -->

<div class="medium-8 columns" markdown="1">

## Introduction
Welcome to the world of _struggle_, sorry, Bioinformatics. Below we outlined sources to help you get started with learning Bioinformatics skill. As a starter, you should learn some basic [linux commands](#Linux-Shell), and a [scripting language](#Programming-Language), such as R and/or Python. Then you can famaliarize yourself with some popular [Bioinformatics software packages](#Bioinformatics-Software), such as BWA, samtools, etc. [Snakemake]() can be your best friend if you are going to build pipelines to process large amounts of data. 

### Linux Shell  {#Linux-Shell}
  * Basic commands - <https://www.liquidweb.com/kb/new-user-tutorial-basic-shell-commands/>
  * 3 most important commands grep, awk, sed - <http://blog.cee.moe/a-brief-introduction-to-grep-awk-and-sed.html>
  * [Understanding Load Averages](http://blog.scoutapp.com/articles/2009/07/31/understanding-load-averages)

### Git and Github  {#Git}
 * Git is great for version control. [How to Write a Git Commit Message](https://chris.beams.io/posts/git-commit/)
 * Get a Github account and join our group Github team(<https://github.com/zhangyxlab>)

### Programing languages {#Programming-Languages}

1. **Python** (_highly recommended for machine learning and basic data processing_)
2. **R** (_great for statistics and matrix processing_)
   * Basics of vectors, dataframes, functions, loops - https://uoftcoders.github.io/rcourse/lec02-basic-r.html
   * Plotting 
     * ggplot2 (aka greatest plotting function) - http://r-statistics.co/Complete-Ggplot2-Tutorial-Part1-With-R-Code.html
       * Combining multiple plots - https://cran.r-project.org/web/packages/gridExtra/vignettes/arrangeGrob.html
     * Complex heatmap - https://jokergoo.github.io/ComplexHeatmap-reference/book/
     * Color options in R 
       * http://colorbrewer2.org
       * https://www.nceas.ucsb.edu/~frazier/RSpatialGuides/colorPaletteCheatsheet.pdf
       * http://www.stat.columbia.edu/~tzheng/files/Rcolor.pdf
       * Wes Anderson fans - https://github.com/karthik/wesanderson
   * Linear Regression - https://www.andrew.cmu.edu/user/achoulde/94842/lectures/lecture09/lecture09-94842.html
   * Apply functions (faster and cleaner alternative to for loops) - https://www.datacamp.com/community/tutorials/r-tutorial-apply-family
3. **Perl** (_not as popular as Python but still useful_)

### Coding environments {#Coding-Environments}
Python Jupiter Notebook and Rstudio is a great Interactive environment to programing in those languages.

### Bioinformatics Software {#Bioinformatics-Software}
Commonly used software include: 
  * Sequence alignment: BWA, bowtie1/2, rnaSTAR
  * SAM file manipulation: samtools, pysam (Python Wrap of samtools)

For a more complete list of software and databases, please visit [Awesome Genomics Resources](https://github.com/shawnzhangyx/Pandomics-awesome-genomics-resources)

## General Learning Resources   {#Resources}
* BBS:
  * [生信技能树](http://www.biotrainee.com/)
* Books 
  * Bioinformatics Data Skills. 

## Computing Best practices {#Computing-Best-Practices}

This section is intended to offer everyone suggestions/ways to look for resources and keep a good working habit.
### Running jobs on server
We have two server options: Silencer and HPC. '''''Silencer''''' has only 64 CPUs and 384 GB memory (huge!), whereas '''''TSCC''''' has thousands of cores and unparalleled power for computing. Therefore, silencer is suited for running small batch of jobs or jobs that won't take a long time, whereas TSCC is meant for intensive jobs, such as sequence alignment.
Below we list a few bullet points what you need to know when running jobs on these servers. 

* Please monitor the memory and CPU usage of your jobs using the <code>top</code> command on silencer. The admin reserves the right to contact you and delete your jobs if your jobs are exceeding the maximum CPU load (64) and causing the system unstable.
* If you have very intensive jobs which will take > 10 CPUs for an extended amount of time(> 24h), please consider running it on HPC.
* It is highly recommended to run alignment tasks on TSCC if you have more than 5 samples because you can run them in parallel on TSCC. If the alignment step is not time sensitive, you could also run it on Silencer. But limit yourself to a maximum of 3 simultaneous jobs. Never run more than 3 alignment jobs on Silencer or you'll cause other people's jobs to jam.

### Managing project directory/storage 
Remember to organize your project directory for easy navigation. Below we give some general suggestions for how to organize your directories. In the end of the day, you will develop your own style of directory structure. 

<pre>
home
├── projects
|   ├── project A
|   |   ├── 'README'
|   |   ├── data/
|   |   ├── scripts/
|   |   ├── analysis 1/
|   |   ├── ... 
|   |   └──analysis N/
|   └── project B
| 
├── software
├── reference_database
└── other directories    
</pre>

### Naming conventions
Naming files correctly could be very important for your project. With a bad file name, you may be more likely to mislabel your samples. There are several rules could help you to manage your files. 
* Use explicit names, instead of making up some short words out of convenience. Stop using "test", "try", "exp", etc. Use the combination of labels such as tissue, protocol, condition in your file names.
* If there are numbers in your sample names, it would be a good practice to put leading zeros so that the files could be sorted easily. For example, use file-001.txt rather than file-1.txt. 

### Managing software/script 
It is a good practice to make your scripts/software package reusable. One great utility in Unix systems is that it comes with a function [[git]]. Git can help you track the changes in your code. With public hosts such as [https://github.com/ Github], you can easily share and collaborate on code. We have a [https://github.com/ren-lab lab account] on github. Consider sharing and using the scripts/modules from this account.

When you are writing software that you want to share in the public domain, you may consider licensing your software. For a simple reference, please see here: <https://choosealicense.com/>

Recommended Reading: [Ten simple rules to make research code more robust](http://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1005412)



{% include _improve_content.html %}
</div>
