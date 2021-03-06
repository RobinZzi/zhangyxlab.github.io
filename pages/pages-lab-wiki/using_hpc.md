---
layout: page-fullwidth
skip_boilerplate: True
title: "Instructions for HPC"
#subheadline: "Getting started in Zhang lab"
#teaser: "The documentation is a work in progress..."
permalink: "/onboarding/using_hpc/"
header:
#   image: "header_roadmap_2.jpg"
   background-color: "#FFFFFF"
---
<div class="row">
<div class="medium-3 columns" markdown="1">
<div class="panel radius" markdown="1">
**Table of Contents**
{: #toc }
*  TOC
{:toc}
</div>
{% include _onboarding_sidebar.html %}
</div><!-- /.medium-4.columns __ -->



<div class="medium-9 columns" markdown="1">
### Introduction 
The High Performance Computing Cluster (HPC) uses SLURM (Simple Linux Utility for Resource Management) to manage job submission. For every job you want to run, you have to write a [Job Script](#Example-Script) and submit it (using `sbatch [script]`) to the job scheduler. You have to specify the sources (such as number of CPUs, memory and running time) for your job. 

### Login information: 
Login node: 172.16.75.132


### Example script {#Example-Script}
<pre>
#!/bin/bash
#SBATCH -o job.%j.out
#SBATCH -p amd-ep2
#SBATCH --qos=normal
#SBATCH -J JobName
#SBATCH --nodes=1
#SBATCH --ntasks-per-node=1
#SBATCH --cpus-per-task=1
#SBATCH --mem-per-cpu=4Gb
pwd; hostname; date
$command 
</pre>

Save this script as `test.pbs` and run `sbatch test.pbs`. 

### External Resources
* SLURM info:  <https://slurm.schedmd.com/documentation.html> 
* Sample SLURM scripts: <https://help.rc.ufl.edu/doc/Sample_SLURM_Scripts>

### Useful commands: 
* sacct：查看历史作业信息
* salloc：分配资源
* sbatch：提交批处理作业
* scancel：取消作业
* scontrol：系统控制
* sinfo：查看节点与分区状态
* squeue：查看队列状态
* srun：执行作业
 
#### $ sinfo

|关键词 | 含义 |
|-------|------|
|PARTITION | 分区名，大型集群为了方便管理，会将节点划分为不同的分区设置不同权限|
|AVAIL  | 可用状态：up 可用；down 不可用|
|TIMELIMIT | 该分区的作业最大运行时长限制, 30:00 表示30分钟，如果是2-00:00:00表示2天，如果是infinite表示不限时间 |
|NODES | 数量|
|STATE |  状态：drain: 排空状态，表示该类结点不再分配到其他；idle: 空闲状态；alloc: 被分配状态;mix:部分被占用，但是仍有可用资源|

#### $ scontrol  
* `scontrol show partition [PARTITION_NAME]`: 查看分区的状态信息 
*  `scontrol show node [NODE_NAME]`: 查看节点的状态信息

#### $ squeue  
* `squeue`: 查看全局
* `squeue  -u $USER`:  查看自己的任务

|关键词 | 含义|
|-------|-----|
|JOBID | job的id号，每个成功提交的任务都会有唯一的id|
|PARTITION | 计算分区名|
|NAME |  任务名，默认以提交脚本的名称当作任务名|
|USER |  用户名，提交该任务的用户名|
|ST | 任务状态：PD排队；R运行；S挂起；CG正在退出|
|TIME |  任务运行时间|
|NODES | 任务作占节点数|
|NODELIST(REASON) | 任务所占节点列表，如果是排队状态的任务，则会给出排队原因|

#### $ module 
* `module avail`: 查看可用的module模块
* `module load [MODULE_NAME]`:  加载module模块
* `module list`:  查看加载的模块
* `module unload [MODULE_NAME]`: 卸载模块

{% include _improve_content.html %}
</div>
