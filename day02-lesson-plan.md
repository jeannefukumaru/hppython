# High Performance Python with Parquet, Pyarrow and Dask 
When datasets increase in size, Pandas users usually start encountering a few problems: 
1. For datasets more than 1GB, file I/O and processing speed starts to slow down 
2. For datasets more than 8GB/16GB, the dataset no longer fits into the memory of a single machine 


At this point, most users will start switching to Spark or other parallel processing tools like MPI on an HPC Cluster. However, there are also Python Packages that handle this problem. These packages (Pyarrow, Parquet and Dask) allow developers to continue working within the Python ecosystem and also provide more flexibility with respect to specifying custom algorithms. 


Learning Objectives/Lesson Plan: 
* Use Parquet and Arrow to optimise File I/O when Pandas starts to slow down 
* Use Dask arrays to process out-of-core Numpy arrays
* Use Dask dataframes to process out-of-core Pandas arrays
* Use Dask bags to handle out-of-core unstructured data (? maybe no time) 
* Use Dask.distributed to parallelise Python processes like XGBoost on a single machine and on a cluster of machines 
* Use Dask to specify a custom algorithm (stable out-of-core SVD)
