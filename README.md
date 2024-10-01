# Poker MPI

Welcome to **Poker MPI**, a parallel implementation of a poker hand simulation using the Message Passing Interface (MPI). This project aims to efficiently simulate multiple poker hands in parallel to demonstrate the use of distributed computing techniques, specifically using MPI to speed up the simulation process.

## Overview

**Poker MPI** is a C++ application that simulates poker hands across multiple processors. Using MPI, the simulation is distributed across several nodes, making it ideal for high-performance computing environments. This project serves as an educational example of how to use MPI for parallel processing tasks.

The simulation is designed to compute poker hand results, calculate probabilities, and gather statistics on the outcomes in a distributed manner. This approach allows the simulation to run much faster than a sequential version by distributing the workload across available processors.

### Installation Steps

1. Clone the repository:
    ```bash
    git clone https://github.com/mtejedor22/poker_MPI.git
    cd poker_MPI
    ```

2. Build the project:
    ```bash
    make
    ```

## Usage

Once compiled, the program can be run using an MPI launcher (e.g., `mpirun` or `mpiexec`). The number of processes can be specified when executing the program.

### Running the Poker Simulation

To run the simulation with MPI:

```bash
mpirun -np <number_of_processes> ./poker_simulation <number_of_hands>
```

Where:

- `<number_of_processes>`: The number of MPI processes to use for the simulation.
- `<number_of_hands>`: The total number of poker hands to simulate.

For example, to simulate 100,000 poker hands using 4 processes:

```bash
mpirun -np 4 ./poker_simulation 100000
```

