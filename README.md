# multi-threading
This experiment investigates how effectively multi-threading can accelerate matrix multiplication. Here's a breakdown of the methodology:

1. Data Preparation:

We generate 100 random matrices of size 1000x1000 using NumPy's np.random.rand() function. These represent the variable data we'll be manipulating.
Additionally, we create a single constant matrix of size 1000x1000. This constant matrix will be used for multiplication across all trials.
2. Multi-Threaded Multiplication:

We perform the matrix multiplications using a multi-threaded approach. The number of threads will be varied from 1 to 8 to understand the impact of parallelism on performance.
Each thread is assigned a specific set of random matrices to multiply with the constant matrix. This ensures efficient workload distribution amongst the threads.
3. Performance Measurement:

To gauge the effectiveness of each threading configuration, we measure the time taken for each multiplication operation. We use Python's time.time() function to record the time before and after the operation, calculating the elapsed time.
4. CPU Utilization Monitoring:

The psutil library is employed to monitor CPU usage throughout the experiments. This helps us understand how the system's processing power is being utilized by the multi-threaded matrix multiplication process.
5. Visualization and Analysis:

We will create a graph titled "Time Taken vs Number of Threads." This graph will depict the relationship between the number of threads used and the corresponding time taken to complete the matrix multiplication operation.
By analyzing the graph, we can observe the trend: as the number of threads increases, the processing time should generally decrease due to parallelism. However, there's a tipping point where the overhead of managing additional threads becomes significant, negating the benefits.
The graph, along with CPU usage data, helps us identify the optimal number of threads that strike a balance between parallelism and overhead, leading to the fastest execution time. This optimal number can vary depending on the specific hardware and workload characteristics.
Benefits:

This methodology allows us to:

Evaluate the performance gains achievable with multi-threaded matrix multiplication.
Identify the optimal number of threads for this specific workload on the given hardware.
Gain insights into the trade-off between parallelism and thread management overhead.
This information can be valuable for optimizing code that performs matrix multiplications and maximizing computational efficiency.
