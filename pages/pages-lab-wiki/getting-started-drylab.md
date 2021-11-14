---
layout: page-fullwidth
skip_boilerplate: True
title: "Getting Started (Drylab)"
permalink: "/onboarding/getting_started_drylab/"
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

## Servers 
We have two servers that you can use for data analysis and software development. 1. [High Performance Computing Cluster](#HPC) and 2. [Lab server](#Lab-Server). You'll need to log in VPN if you plan to access these servers off-campus. 
### 1. High Performance Computing cluster (HPC) {#HPC}
 * IP address to HPC: 172.16.75.132 (port 22 or 10002) 
 * Link to Westake HPC: <https://hpc.westlake.edu.cn/>
 * Help document: <https://hpc.westlake.edu.cn:8080/index.html>
#### Setting up an account on the HPC. 

#### Running jobs on HPC. 
[This page](/{{site.baseurl}}/onboarding/using_hpc) provides detailed instructions on how to run jobs on HPC. 

#### Help information 
 * Please ask the admin to be added to the Wechat group. 

### 2. Lab Server {#Lab-Server}
#### Lab server configuration 
 * CPU: 64 core;128 threads
 * Memory: 512 G
 * Disc Space: 100TB
 * IP address: x.x.x.x


## Shared directory on the server. 
We have a shared directory on the server, which contains resources that can be used by all lab members. The location of the shared directory is `/storage/zhangyanxiaoLab/share/`. They include:
 * Genome files in fasta format. 
 * Genome index for aligners such as BWA, bowtie2, rnaSTAR, etc. 

### Analysis Pipelines
We have built basic analysis pipelines with [snakemake](). They are easy to run and can produce very standard output for sequencing datasets. The location of the pipeline is currently in `/storage/zhangyanxiaoLab/share/Pipelines`. Currently we suppport analysis of: 
 * RNA-seq (paired-end or single-end)
 * ChIP-seq (single-end)
 * ATAC-seq (paired-end) (This can be applied to paired-end ChIP-seq as well. )
 * Hi-C 


{% include _improve_content.html %}
</div>
