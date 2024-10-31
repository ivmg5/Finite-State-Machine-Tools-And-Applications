# **Finite-State Machine Tools and Applications**
> *A suite of Python tools for creating, visualizing, and utilizing finite-state machines in lexical analysis and production rule conversions.*

## **Introduction**
The "Finite-State Machine Tools and Applications" repository provides a collection of three miniprojects focused on the implementation and application of Finite State Machines (FSMs). Each project demonstrates distinct FSM uses, from lexical analysis to graphical representation of automata derived from production rules. Implemented in Python, these projects highlight the power of FSMs in various computational contexts, making complex tasks in text processing, syntax highlighting, and automata theory accessible and interactive.

## **Project Overview**

### 1. Arithmetic Lexer Program

**Description**: This project implements a Deterministic Finite State Machine (DFSM) to analyze and process arithmetic expressions. The lexer categorizes sequences of characters into tokens, including integers, floating-point numbers, identifiers, operators, and symbols, based on predefined rules and transitions. The program reads from an input file and outputs a table of tokens and their respective types.

**Key Features**:
- Recognizes various token types: integers, floats, operators, symbols, and identifiers.
- Uses a state machine to traverse the input string, transitioning between states based on the current character.
- Optionally generates a graphical representation of the automaton for visualization.

**How to Run**:
1. Prepare an input file (`input.txt`) containing arithmetic expressions.
2. Execute `main.py` to tokenize the expressions with:
   ```bash
   python main.py
   ```
3. To generate an automaton graph, uncomment the line in `main.py` that calls the `graph()` function.

For more details, see the project directory: [Arithmetic Lexer Program](./LexicalAnalyzer).

### 2. Python Lexical Highlighter

**Description**: This project provides a lexical highlighter for Python code, identifying lexical categories such as keywords, operators, literals, comments, identifiers, and data structures. The highlighter uses regular expressions to scan the code, generating an HTML file with highlighted syntax for easy readability.

**Key Features**:
- Identifies Python-specific tokens including keywords, operators, literals, comments, and data structures.
- Generates an HTML file (`out.html`) where syntax elements are highlighted based on defined styles.
- Easy-to-use interface for input and output.

**How to Run**:
1. Prepare the necessary files (`main.py`, `template.html`, `input.txt`) in the project directory.
2. Run the lexical highlighter with:
   ```bash
   python main.py
   ```
3. Open the generated HTML file (`out.html`) in a browser to view the highlighted syntax.

For more details, see the project directory: [Python Lexical Highlighter](./LexicalHighlighter).

### 3. Automaton Converter Web Application

**Description**: This web application converts user-defined production rules into a non-deterministic finite automaton (NFA) and visually represents it using the `visual-automata` library. The application, built with Python's `shiny` library, provides an interactive interface for entering production rules and viewing the resulting NFA.

**Key Features**:
- Converts user-specified production rules into a non-deterministic finite automaton.
- Displays a graphical NFA diagram, showing states, transitions, and final states clearly.
- Uses `shiny` to provide a web-based, user-friendly interface, and `visual-automata` for graphical rendering.

**How to Run**:
1. Ensure `graphviz` is installed on your system and accessible in the PATH.
   - On Ubuntu:
     ```bash
     sudo apt-get install graphviz
     ```
   - On macOS:
     ```bash
     brew install graphviz
     ```
   - On Windows: It’s recommended to use WSL2 with Ubuntu and follow Ubuntu instructions.

2. Clone the repository:
   ```bash
   git clone https://github.com/ivmg5/Finite-State-Machine-Tools-And-Applications.git
   cd Finite-State-Machine-Tools-And-Applications/Converter
   ```

3. Run the application with:
   ```bash
   shiny run app.py
   ```

4. Access the web application at `http://localhost:8000/` in your browser, enter production rules, and view the generated NFA.

For more details, see the project directory: [Automaton Converter Web Application](./Converter).

## **Table of Contents**
1. [Introduction](#introduction)
2. [Project Overview](#project-overview)
3. [Installation](#installation)
4. [Usage](#usage)
5. [License](#license)

## **Installation**
1. **Prerequisites**:
   - **Python 3.x** - [Download](https://www.python.org/downloads/)
   - **NetworkX** - `pip install networkx`
   - **Matplotlib** - `pip install matplotlib`
   - **Additional Packages** (for visualization in Proyecto3) - `pip install shiny visual_automata forbiddenfruit frozendict`

2. **Clone the repository**:
   ```bash
   git clone https://github.com/ivmg5/Finite-State-Machine-Tools-And-Applications.git
   cd Finite-State-Machine-Tools-And-Applications
   ```

3. **Navigate to the specific project directory** (e.g., `LexicalAnalyzer`) and install dependencies as needed:
   ```bash
   cd LexicalAnalyzer
   ```

4. **Run the projects** using the main scripts within each directory:
   ```bash
   python main.py
   ```

### **Configuration Options**
- Each project may require adjusting configurations in script files for custom input or FSM visualization options.

## **Usage**
To use each project:
1. **Lexical Analyzer**:
   - Place input text in `input.txt`.
   - Run `main.py` to parse tokens.
   - Output: Token type and matches.

2. **Lexical Highlighter**:
   - Place code to be highlighted in `input.txt`.
   - Run `main.py` to generate an HTML file (`out.html`) with syntax highlighting.

3. **Converter**:
   - Place production rules in the provided text area in `app.py`.
   - Run `app.py` and follow the UI instructions to generate a graph.

**Example usage**:
```python
# In LexicalAnalyzer/main.py
lexer("input.txt")
```

## **License**
This project is licensed under the MIT License.

[![Build Status](https://img.shields.io/badge/status-active-brightgreen)](#)
[![Code Coverage](https://img.shields.io/badge/coverage-80%25-yellowgreen)](#)
