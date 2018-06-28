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

# Function

write a function called **fact1** in script **fact.py**. 

    vim fact.py
    def fact1(n):
        assert n >=0,'negative factorial cannot be'
        assert type(n) == int,'only intergers'
        if n <= 1 :
        return 1
        else:
        retern n*fact1(n-1)
    :wq

write another script **hello.py** in which call the function **fact1**.

    vim hello.py
    #!/user/qianl/python
    import fact
    print ('factotial of 7 is ',fact.fact1(7))
    :wq

    chmod +x fact.py hello.py
run the script **hello.py**

    ./hello.py
