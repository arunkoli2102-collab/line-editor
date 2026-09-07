# Simple Line Editor in C

A command-line line editor built in C for the **Portfolio Building Studio Course (3rd Semester) Coding Competition**. This tool allows users to create, view, and modify text documents line-by-line directly from the terminal without a GUI.

--

## Team Information
- **Members:**
  Arun kumar - R25EJ014
  Harsha Nayak - R25EJ038
  Abhishek - R25EJ002

## Features Implemented

### Core Features
- **Display Document:** View all text lines alongside their 1-based line numbers.
- **Insert Line:** Add a line of text at any valid position, shifting existing lines downward.
- **Delete Line:** Remove a line by its line number, shifting remaining lines upward.
- **Save / Load File:** Export the in-memory text to a `.txt` file or import an existing file on demand[cite: 1].

### Bonus Features
- **Line & Word Count:** View real-time statistics on total document lines and word count[cite: 1].

---

## Data Structure Choice & Justification

We chose a **Dynamic Array of Strings (`char **lines`)** to store the document in memory[cite: 1].

- **Pros:** Offers $O(1)$ random access to any line by index, fast iterations for displaying the document, and straightforward memory management using `realloc` and `malloc`.
- **Trade-offs:** Inserting or deleting lines requires shifting pointers, taking $O(n)$ time. Given that standard text documents edited line-by-line fit easily within memory limits, $O(n)$ pointer shifts are negligible and computationally inexpensive compared to the simplicity of memory allocation.

---

## How to Compile and Run

### Prerequisites
- GCC Compiler installed on your system[cite: 1].

### Compilation
Open your terminal in the project directory and run:

```bash
gcc -Wall -o editor main.c
