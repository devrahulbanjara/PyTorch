# Dataset and Dataloader

In this repository, we explore the concept of **Dataset** and **Dataloader** and their role in efficiently handling data during training. This approach addresses the limitations of **Batch Gradient Descent (BGD)** by introducing **Mini-Batch Gradient Descent (MBGD)** for better memory management and faster convergence.

## Why Not Use Batch Gradient Descent (BGD)?

### 1. Memory Inefficiency
- In BGD, the entire dataset is sent through the model in a single forward pass, which can be too heavy for RAM, especially for large datasets.
- This makes it computationally expensive and unmanageable for large-scale data.

### 2. Slow Convergence
- BGD updates parameters only after processing the entire dataset.
- This leads to slow convergence as we don't get frequent updates to the parameters.

## Solution: Mini-Batch Gradient Descent (MBGD)

In **MBGD**, the data is divided into smaller batches, and parameter updates are made after each batch. This balances the trade-off between computational efficiency and convergence speed:

### Advantages
- Efficient memory usage by processing data in smaller chunks.
- Faster convergence with more frequent parameter updates.
- Enables parallelization during computation.

## How Dataset and Dataloader Work

To implement **MBGD**, we use the **Dataset** and **Dataloader** classes:

### Dataset Class
- Knows where the data is stored in memory.
- Efficiently loads each row of the data as needed.

### Dataloader Class
- Responsible for making batches of data.
- Determines the number of rows per batch (batch size).
- Coordinates with the **Dataset** class to load data and form batches.

Together, these classes efficiently load and process data in batches, which are then sent for training.

## Example

- Suppose we have a dataset with 10 rows (training examples), and we set the batch size to 2.
- The total number of batches in an epoch will be:

  **Number of batches = Total data / Batch size = 10 / 2 = 5.**

- In one epoch, parameters will be updated 5 times using these 5 batches.

## Benefits of Using Dataset and Dataloader

- Scalable to large datasets by loading data in chunks.
- Improves training efficiency with faster and more frequent updates.
- Simplifies data preprocessing and batch management.

By understanding and implementing **Dataset** and **Dataloader**, we can build training pipelines that are both efficient and scalable for modern machine learning workflows.

