# C Code to Optimised CFG

A compiler analysis and visualisation tool that transforms C programs into Control Flow Graphs (CFGs), performs dataflow analysis, applies compiler optimisation passes, and provides an interactive interface to visualise and compare program control flow before and after optimisation.

## Overview

Understanding the internal structure of a program and the effect of compiler optimisations can be difficult when working directly with source code or LLVM Intermediate Representation (IR).

This project provides a pipeline that accepts C source code, generates LLVM IR using Clang, constructs Control Flow Graphs, performs dataflow analysis, applies LLVM optimisation passes, and visualises the resulting CFGs.

The project also includes an interactive Streamlit interface that allows users to explore and compare the generated graphs.

## Features

- Accepts C programs as input.
- Generates LLVM Intermediate Representation (IR) using Clang.
- Extracts basic blocks and control-flow relationships.
- Generates Control Flow Graphs (CFGs).
- Performs dataflow analysis on program control flow.
- Applies LLVM optimisation passes.
- Generates optimised LLVM IR.
- Produces CFGs before and after optimisation.
- Visualises CFGs using Graphviz.
- Provides an interactive Streamlit interface.
- Allows comparison of original and optimised program control flow.

## Technologies Used

- C
- C++
- LLVM
- Clang
- LLVM Intermediate Representation (IR)
- Graphviz
- Python
- Streamlit

## Project Workflow

```text
C Source Code
      |
      v
Clang Compilation
      |
      v
LLVM Intermediate Representation (IR)
      |
      v
Control Flow Graph Generation
      |
      v
Dataflow Analysis
      |
      v
LLVM Optimisation Passes
      |
      v
Optimised LLVM IR
      |
      v
Optimised Control Flow Graph
      |
      v
Graphviz Visualisation
      |
      v
Interactive Streamlit Interface
```

## Control Flow Graph Generation

The input C program is compiled using Clang to generate LLVM Intermediate Representation.

The LLVM IR is analysed to identify functions, basic blocks, and control-flow relationships between the blocks.

These relationships are then used to construct a Control Flow Graph where:

- Nodes represent basic blocks.
- Directed edges represent possible control-flow transitions.

The generated CFG provides a visual representation of the execution paths within the program.

## Dataflow Analysis

The project performs dataflow analysis on the generated control-flow structure.

The analysis processes information across basic blocks and demonstrates how compiler analyses use CFGs to reason about program behaviour and optimisation opportunities.

## LLVM Optimisation

LLVM optimisation passes are applied to the generated Intermediate Representation.

These transformations may simplify control flow, remove unnecessary instructions, eliminate redundant computations, and improve the structure of the generated code.

After applying the optimisation passes, a new CFG is generated from the optimised LLVM IR.

This allows the original and optimised program structures to be compared.

## Visualisation

Graphviz is used to generate visual representations of the Control Flow Graphs.

The project visualises both:

- Original CFG generated before optimisation.
- Optimised CFG generated after LLVM optimisation passes.

This makes it easier to understand how compiler optimisations affect the control-flow structure of a program.

## Interactive Interface

A Streamlit-based interface provides an interactive environment for exploring the compiler analysis pipeline.

Users can:

- Provide C source code as input.
- Generate LLVM IR.
- View the original Control Flow Graph.
- Apply compiler optimisation passes.
- View the optimised Control Flow Graph.
- Compare program structure before and after optimisation.

## Requirements

The project requires the following tools:

- LLVM
- Clang
- Graphviz
- Python 3
- Streamlit

Install the required Python packages using:

```bash
pip install streamlit graphviz
```

LLVM, Clang, and Graphviz must also be installed and accessible from the system command line.

## Running the Project

Clone the repository:

```bash
git clone <repository-url>
```

Move into the project directory:

```bash
cd <project-directory>
```

Install the required Python dependencies:

```bash
pip install streamlit graphviz
```

Run the Streamlit application:

```bash
streamlit run app.py
```

Open the local URL displayed in the terminal to access the application.

## Example Pipeline

For an input C program:

```c
int main() {
    int x = 10;

    if (x > 5)
        x = x + 1;
    else
        x = x - 1;

    return 0;
}
```

The project performs the following steps:

```text
Input C Program

        |
        v

Generate LLVM IR

        |
        v

Construct Original CFG

        |
        v

Perform Dataflow Analysis

        |
        v

Apply LLVM Optimisation Passes

        |
        v

Generate Optimised LLVM IR

        |
        v

Construct Optimised CFG

        |
        v

Visualise and Compare CFGs
```

## Project Objective

The objective of this project is to demonstrate the relationship between C source code, LLVM Intermediate Representation, Control Flow Graphs, dataflow analysis, and compiler optimisations.

By visualising CFGs before and after optimisation, the project provides a clearer understanding of how compiler transformations affect the internal structure and control flow of programs.

## Future Improvements

- Support for additional LLVM optimisation passes.
- More detailed dataflow analysis techniques.
- Interactive highlighting of basic blocks and CFG edges.
- Side-by-side CFG comparison.
- Display of LLVM IR alongside the generated CFG.
- Support for larger and more complex C programs.

## Contributors

Developed as a group project for the Paradigms of Programming course.
