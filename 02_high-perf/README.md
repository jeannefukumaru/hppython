# Dask Tutorial

This workshop on `dask` is adapted from Anaconda Inc.'s dask tutorial last given at SciPy 2017 in Austin Texas.
[A video is available online](https://www.youtube.com/watch?v=mbfsog3e5DA). Full credit goes to the SciPy 2017 instructors for illustrating `dask` internals so clearly. We have added in ecommerce-related datasets and exercises to show how `dask` can be applied to the ecommerce domain. We have also added in a notebook exploring how `dask-ml` can be used on ecommerce data. 

## Here is an overview of Dask from Anaconda Inc. :

Dask provides multi-core execution on larger-than-memory datasets.

We can think of dask at a high and a low level

*  **High level collections:**  Dask provides high-level Array, Bag, and DataFrame
   collections that mimic NumPy, lists, and Pandas but can operate in parallel on
   datasets that don't fit into main memory.  Dask's high-level collections are
   alternatives to NumPy and Pandas for large datasets.
*  **Low Level schedulers:** Dask provides dynamic task schedulers that
   execute task graphs in parallel.  These execution engines power the
   high-level collections mentioned above but can also power custom,
   user-defined workloads.  These schedulers are low-latency (around 1ms) and
   work hard to run computations in a small memory footprint.  Dask's
   schedulers are an alternative to direct use of `threading` or
   `multiprocessing` libraries in complex cases or other task scheduling
   systems like `Luigi` or `IPython parallel`.

## Prepare

You should clone this repository

    git clone http://github.com/dask/dask-tutorial

and then install necessary packages.

#### a) Create a conda environment (preferred)

In the repo directory

    conda env create -f environment.yml 
    conda activate dask-tutorial

#### b) Install into an existing environment

You will need the following core libraries

    conda install numpy pandas h5py Pillow matplotlib scipy toolz pytables snakeviz dask distributed

You may find the following libraries helpful for some exercises

    pip install graphviz
    pip install dask-ml
    pip install dask-ml[xgboost]
    
#### c) Use Dockerfile

You can build a docker image out of the provided Dockerfile.



#### Graphviz on Windows

You may need to do the following

1. conda install -c conda-forge graphviz
2. conda install -c conda-forge python-graphviz



### Prepare artificial data.

From the repo directory

    python prep.py


### Launch notebook

From the repo directory

    jupyter notebook 


## Links

*  Reference
    *  [Docs](http://dask.pydata.org/en/latest/)
    *  [Code](https://github.com/dask/dask/)
    *  [Blog](http://matthewrocklin.com/blog/)
*  Ask for help
    *   [`dask`](http://stackoverflow.com/questions/tagged/dask) tag on Stack Overflow, for usage questions
    *   [github issues](https://github.com/dask/dask/issues/new) for bug reports and feature requests
    *   [gitter chat](https://gitter.im/dask/dask) for general, non-bug, discussion
    *   Attend a live tutorial
