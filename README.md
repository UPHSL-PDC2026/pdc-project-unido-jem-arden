## Problem Description

This project aims to develop a parallel data processing application using Python to analyze a moderately large dataset. The system performs common data analytics tasks such as filtering records, aggregation, and sorting. The goal is to compare sequential execution with parallel execution to determine whether parallel processing improves performance when working with large datasets.

## Parallelization Approach

The parallel implementation uses Python's multiprocessing module to execute multiple data operations simultaneously. Instead of running filtering, aggregation, and sorting sequentially, the system distributes these tasks across multiple processes. This allows the program to utilize multiple CPU cores and perform computations concurrently.

## Performance Analysis

Two implementations were tested: sequential and parallel execution. The sequential version processes each operation one after another, while the parallel version executes them concurrently using multiple processes. Based on the recorded execution times, the parallel version demonstrates faster performance compared to the sequential version, showing the advantage of shared-memory parallelism for data processing tasks.

## Challenges Encountered

During the implementation, challenges were encountered when using multiprocessing in a Jupyter Notebook environment. Lambda functions caused pickling errors because multiprocessing requires serializable functions. This issue was resolved by defining named functions instead of lambda expressions.
