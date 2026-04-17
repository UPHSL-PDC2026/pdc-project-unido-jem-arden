# Parallel Data Processing Project

## Project Overview
This project analyzes a COVID-19 dataset using both sequential and parallel processing techniques in Python. The goal is to compare execution time and evaluate the performance improvement achieved through parallel computing.

## Group Members:
Ilagan, Lloyd
Lipata, Wilmar
Mendoza, Josh Leonard
Prugalidad, Azra Raphael
Unido, Jem Arden

## Tools and Technologies Used
- Python
- Pandas
- Multiprocessing
- Google Colab / Jupyter Notebook
- Matplotlib

## Instructions for Running the Project
1. Open the notebook in Google Colab or Jupyter Notebook.
2. Mount Google Drive if using Google Colab.
3. Load the dataset from the provided CSV file.
4. Run all cells sequentially to perform data analysis and compare execution times.

## Team Members and Roles
Jem Arden D. Unido – Developer / Data Processing Implementation


# Technical Report
## Problem Description

This project aims to develop a parallel data processing application using Python to analyze a moderately large dataset. The system performs common data analytics tasks such as filtering records, aggregation, and sorting. The goal is to compare sequential execution with parallel execution to determine whether parallel processing improves performance when working with large datasets.

## Parallelization Approach

The parallel implementation uses Python's multiprocessing module to execute multiple data operations simultaneously. Instead of running filtering, aggregation, and sorting sequentially, the system distributes these tasks across multiple processes. This allows the program to utilize multiple CPU cores and perform computations concurrently.

## Performance Analysis

The experiment compared the execution time of sequential and parallel implementations of the dataset operations. Based on the results, the sequential version executed faster than the parallel version. This occurred because the dataset operations were relatively lightweight, and the overhead of creating and managing multiple processes in Python's multiprocessing module added additional execution time.

Parallel processing typically shows performance improvements when working with significantly larger datasets or computationally intensive tasks. In this case, the cost of process creation and communication outweighed the benefits of parallel execution.

<img width="689" height="490" alt="download" src="https://github.com/user-attachments/assets/b187dd1f-5017-4875-8312-a7b45e64caac" />


## Challenges Encountered

During the implementation, challenges were encountered when using multiprocessing in a Jupyter Notebook environment. Lambda functions caused pickling errors because multiprocessing requires serializable functions. This issue was resolved by defining named functions instead of lambda expressions.
