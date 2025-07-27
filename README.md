# 🧠 Custom Memory Allocator (User-Land `malloc` Replacement)

This repository provides a lightweight, custom memory allocator written in **C**, demonstrating core principles of user-space memory management. It's ideal for educational purposes and low-level system programming experiments.

---

## ✨ Features

- **User-Land Heap**: Manages a pre-defined 1GB memory segment.
- **Minimal Overhead**: 4-byte (1 word) header per block.
- **Word-Based Operations**: All allocations are in 32-bit word units.
- **First-Fit Strategy**: Efficiently finds the first suitable free block.
- **Block Splitting**: Efficient memory usage by splitting larger blocks.
- **Basic Deallocation**: Frees blocks and zeroes data (`destroy()`).
- **Debugging Utility**: `show()` visualizes the current heap status.
- **Error Handling**: Uses `errno` for handling allocation failures.
- **Cross-Architecture**: Includes both 32-bit and 64-bit heap definitions.

---

## 📚 Key Concepts

- **Heap**: A statically reserved memory region handled manually by the allocator.
- **Words & Headers**: Memory is allocated in 32-bit word units, each block having a 4-byte header.
- **Allocation Algorithm**: First-fit with optional block splitting for optimization.
- **Pointer Arithmetic**: Direct manipulation of memory addresses.



---

## 🛠️ Building the Project and Executing

Open a terminal, navigate to the project directory, and build using `make`:

```bash
cd "Custom Memory Allocator"
make
./alloc

