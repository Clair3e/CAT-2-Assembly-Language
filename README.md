# ICS3203 CAT 2 – Assembly Programming

## Repository Overview
This repository contains solutions to CAT 2 practical tasks for ICS3203. Each task demonstrates fundamental assembly programming concepts, including control flow, array manipulation, modular subroutine usage, and port-based simulation. The code is written to highlight the importance of efficient memory usage and program structure.

## Tasks Overview

### **Task 1: Control Flow and Conditional Logic**
- **Purpose:**  
  Classifies a user-provided number as `POSITIVE`, `NEGATIVE`, or `ZERO` using branching logic.
  
- **Features:**
  - Prompts the user to input a number.
  - Implements **conditional jumps** (`JE`, `JG`, `JL`) for branching.
  - Utilizes **unconditional jumps** for streamlined program flow.

- **Insights & Challenges:**  
  - Balancing the use of conditional and unconditional jumps to ensure clear and efficient logic flow.
  - Handling edge cases, such as when the number is exactly zero.

---

### **Task 2: Array Manipulation with Looping and Reversal**
- **Purpose:**  
  Reverses an array of integers in place using loops, avoiding additional memory allocation.

- **Features:**
  - Accepts an array of integers (e.g., five values) as user input.
  - Reverses the array by swapping elements using a loop.
  - Outputs the reversed array to the user.

- **Insights & Challenges:**  
  - Managing in-place reversal without creating a new array required careful index management.
  - Ensuring correct memory addressing and loop termination in assembly.

---

### **Task 3: Modular Program with Subroutines for Factorial Calculation**
- **Purpose:**  
  Computes the factorial of a user-provided number using a subroutine, demonstrating modular programming and stack usage.

- **Features:**
  - Accepts a number as input from the user.
  - A subroutine performs the factorial calculation using a loop or recursion.
  - Preserves registers by pushing and popping them on the stack.
  - Stores the final factorial result in a general-purpose register (e.g., `EAX`).

- **Insights & Challenges:**  
  - Managing recursive calls within the subroutine required precise stack operations.
  - Balancing register preservation and restoration for modularity and correctness.

---

### **Task 4: Data Monitoring and Control Using Port-Based Simulation**
- **Purpose:**  
  Simulates a simple control system that reads a sensor value and performs specific actions based on its input.

- **Features:**
  - Simulates reading a "sensor value" from a memory location.
  - Controls a "motor" and "alarm" by setting or clearing bits in specific memory locations:
    - Turns on the motor if the sensor value is low.
    - Triggers an alarm if the sensor value is too high.
    - Stops the motor when the sensor value is moderate.

- **Insights & Challenges:**  
  - Mapping sensor input to memory actions was critical for effective simulation.
  - Ensuring actions were correctly triggered without overwriting or corrupting memory.

---

## How to Compile and Run
The programs in this repository are designed to run on an x86-64 architecture using NASM (Netwide Assembler). Follow these steps to compile and execute each program:

1. Compile the `.asm` file:
   ```bash
   nasm -f elf64 <filename>.asm -o <filename>.o
   ld <filename>.o -o <filename>
