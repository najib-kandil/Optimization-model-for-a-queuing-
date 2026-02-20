In the agent scenario, an autonomous agent submits a batch of 𝑁prompts simultaneously at time zero. All service times for CPUs and GPUs are known in advance and extracted from their respective distributions at prompt creation.
The following assumptions apply:
• All buffers are considered infinite;
• Acceptance probability is 𝑝𝐴=1;
• CPU 1 buffer allows random access;
• GPU and CPU 2 buffers operate under FIFO discipline.
The performance metric of interest is the makespan, defined as the maximum completion time among all prompts.

The following variants were taken into consideration when implementing the model in Simulink:
• Prompts are sent to CPU 1 in random order (you can simply consider the index order)
• A linear programming model of the problem is run at time 0, and provides the best ordering of the operations on CPU 1 and assignments of each prompt to GPU 1 or GPU
