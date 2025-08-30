# Distributed Computing Laboratory (19Z611)

This repository contains the programs and algorithms implemented as part of the **Distributed Computing Laboratory** course.

---

## 📚 Course Details
- **Course Code:** 19Z611
- **Lab Type:** Distributed Computing
- **Hours:** 0 0 2 1  
- **Total Marks:** 30

---

## ✅ Experiments List

1. **Client–Server Implementation using RPC**
2. **Election Algorithms**
   - Bully Algorithm
   - Ring Algorithm
3. **Distributed Deadlock Detection**
   - Centralized Approach
   - Hierarchical Approach
   - Wait-For Graph (WFG) Approach
   - Probe-Based Approach
4. **Study of MPI (Message Passing Interface)**
   - Point-to-Point Matrix Multiplication
   - Point-to-Point Pi Calculation (Monte Carlo)
   - Broadcast Matrix Multiplication
   - Broadcast Pi Calculation (Monte Carlo)

---

## 🔍 Algorithms Implemented

### 1. **Remote Procedure Call (RPC)**
- Define RPC interface using IDL.
- Implement client and server programs.
- Generate stubs using `rpcgen`.
- Compile and execute using `make`.
- **Run:**
    ```bash
    # Start the server
    sudo ./add_server

    # Start the client
    ./add_client localhost 5 8
    ```

---

### 2. **Election Algorithms**
#### 2.1 Bully Algorithm
- Detect coordinator failure and elect the highest-ID node as the new coordinator.

#### 2.2 Ring Algorithm
- Processes arranged in a logical ring, circulate election messages until a new coordinator is elected.

---

### 3. **Deadlock Detection**
- **Centralized Approach:** Single coordinator checks for cycles.
- **Hierarchical Approach:** Multi-level detection using local and global coordinators.
- **Wait-For Graph (WFG):** Detects cycles in WFG.
- **Probe-Based Approach:** Detect deadlocks using probes sent across processes.

---

### 4. **MPI Programs**
#### 4.1 Broadcast Communication
- **Matrix Multiplication** using `MPI_Bcast` and `MPI_Gather`.
- **Pi Calculation** using `MPI_Reduce`.

#### 4.2 Point-to-Point Communication
- **Matrix Multiplication** using `MPI_Send` and `MPI_Recv`.
- **Pi Calculation** using point-to-point communication.

**Compile & Run:**
```bash
# Compile
mpicc program_name.c -o output_name

# Run with 4 processes
mpirun -np 4 ./output_name
