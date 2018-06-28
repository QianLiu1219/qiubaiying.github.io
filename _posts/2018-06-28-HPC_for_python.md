---
layout:     post
title:      Python in HPC
subtitle:   humble one
date:       2018-06-28
author:     LQ
header-img: img/post-bg-ios9-web.jpg
catalog: false
tags:
    - Python 
---

>Compute Canada 2018 Summer School


# Setup

    login cedar : ssh -Y
    initial a job : salloc --time=3:0:0 --mem-per-cpu=3000 --account=wgssum-wa --reservation=wgssum-wr_cpu
    load python : module load python/3.5.4
    check location : which python
    check version : python --version
    active virtual environment : virtualenv LQENV
	install packages : pip install ...

# Basic operations new

    script name : sys.argv
    variable uid : id()
