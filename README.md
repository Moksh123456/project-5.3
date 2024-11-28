# Nand2Tetris Project 5: Computer Implementation

This repository contains the implementation of the **Computer.hdl** file, the final component of the Hack computer described in Chapter 5 of the [Nand2Tetris course](https://www.nand2tetris.org/). The goal of this project is to integrate all previously built modules (CPU, memory, and ROM) into a fully functioning Hack computer capable of executing programs.

---

## Project Overview

The Hack computer is a simple, yet powerful, von Neumann architecture machine. It integrates three main components:
1. **CPU**: Executes instructions.
2. **Memory**: Stores data and program instructions.
3. **ROM**: Contains the program to be executed.

By connecting these components, the computer can fetch instructions from ROM, execute them using the CPU, and store or retrieve data from memory.

---

## Components of the Hack Computer

1. **CPU**:
   - Executes the current instruction.
   - Reads and writes data to/from memory.
   - Determines the next instruction address based on control logic.

2. **Memory**:
   - Composed of **RAM** (for data storage) and **ROM** (for program storage).
   - The `inM` and `outM` signals allow data transfer between the CPU and memory.

3. **ROM**:
   - Stores the program instructions.
   - The program counter (PC) fetches instructions sequentially unless altered by jump commands.

---

## File Structure

- **Computer.hdl**: Hardware description language file that defines the Hack computer.
- **Computer.tst**: Test script to verify the functionality of the computer.
- **Computer.cmp**: Expected output of the test script.
- **README.md**: Documentation file (this file).

---

## Key Features

1. **Instruction Execution**:
   - Fetches instructions from ROM.
   - Passes instructions to the CPU for execution.
   - Handles A-instructions and C-instructions.

2. **Memory Management**:
   - Enables reading and writing to RAM based on the current instruction.
   - Provides the current memory address to the CPU via `inM`.

3. **Program Flow**:
   - The Program Counter (PC) directs the next instruction to fetch.
   - Supports conditional and unconditional jumps.

---

## Testing

### Steps to Test the Computer Implementation:
1. Open the **Hardware Simulator** provided with the Nand2Tetris tools.
2. Load the `Computer.tst` test script.
3. Run the script to simulate the computer's operation.
4. Compare the output with `Computer.cmp` to ensure correctness.

---

## Usage

1. Clone this repository:
   ```bash
   git clone https://github.com/your-username/nand2tetris-computer.git
   cd nand2tetris-computer
   ```

2. Open **Computer.hdl** in the Hardware Simulator.
3. Run the test script (`Computer.tst`) to verify functionality.

---

## Example Program Execution

### Program Example
A sample program stored in the ROM:
```assembly
@2
D=A
@3
D=D+A
@0
M=D
```

### Execution Steps
1. The ROM provides the instructions sequentially.
2. The CPU processes each instruction:
   - Load `2` into register `A`.
   - Add `3` to `D` and store the result in memory address `0`.
3. The RAM is updated with the final result.

---

## Resources

- [Nand2Tetris Official Website](https://www.nand2tetris.org/)
- [Project 5 Specification](https://www.nand2tetris.org/project05)

---

## Author

This implementation was created as part of the **Nand2Tetris course**, an exciting journey in understanding computer systems from the ground up.

Contributions and feedback are welcome! 😊

---

## License

This project is licensed under the MIT License.
