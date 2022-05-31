# {What is reverse engineering}

Reverse Engineering is the process of taking a piece of software or hardware and analyzing its functions and information flow so as to understand its non-visible processes and behaviors.

# {What purpose does it serve}

Reverse Engineering tends to be used to look at a program from the outside in, by third parties that don't have access to the source code. For a practical example, if an anti-malware company discovers a piece of malware, they can use reverse engineering techniques to break down and understand the functions of the malware without accidentally enabling or triggering the virus.

# {How is it done + How is compiling done}

## How does Reverse Engineering

##### The specific techniques for Reverse Engineering are dependent on the specific thing its being performed on, but it typically follows three general steps:

### Information Extraction

In this step, the design of the object being reverse engineered is studied and extracted to see how the pieces fit together. It may involve finding and examining source code, or using tools, like disassemblers, to break a thing into its part.

### Modeling

In this step, the information that was extracted is abstracted to make a conceptual model, like a data flow diagram or a structure chart. This model serves as a guide to design new objects and systems.

### Review

In this step, the model is tested in various scenarios to ensure its an accurate abstraction of the original object. Once this step is completed, the model can be used to engineer the original object.

## How does Compiling

##### Compilers translate human-readable source code written in programming languages into machine code, for specific machine types. This process is divided into something called the "Compilation Phase", which is divided into 6 major steps:

### Lexical Analysis

In this step, the compiler divides source code into manageable fragments called "lexemes" (abstract units of a specific language’s lexical system). After splitting code into lexemes, a sequence of tokens (object that describes a lexeme and gives information about a lexeme's purpose and source code location) is created.

Ex: The code: `String greeting = "hello";` gets divided into five lexemes, `String`, `greeting`, `=`, `"hello"`, and `;`.

### Syntax Analysis

In this step, the compiler uses the tokens to create an abstract syntax tree, which represents the logical structure of the program. Then, the compiler checks grammatic structure of the source code and its syntax correctness. The compiler also alerts the user about any syntax errors it discovers.

### Semantic Analysis

In this step, the compiler uses the abstract syntax tree to look for semantic errors.

#### Semantic Analysis can be divided into three steps:
  - Type Checking: The compiler checks the type of assignment statements, arithmetic operations, functions, and method calls.
  - Flow Control Checking: The compiler checks if flow control structures are used correctly and if classes and objects are correctly accessed.
  - Label Checking: The compiler validates label and identifier usage.

#### Semantic Errors can include:
  - Assigning the wrong type to a variable.
  - Declaring variables with the same name.
  - Using undeclared variables.
  - Using a keyword as a variable name.

Finally, the compiler produces an annotated version of the abstract syntax tree, marking the semantic errors.

### Intermediate Code Generation

In this step, the compiler creates an intermediate code, a version of code between the source code and the target machine language. This intermediate code can either be high-level, where its similar to source code, or low-level, where its similar to machine code.

### Optimization

In this step, the compiler enhances the efficiency of the code.

#### Follows three principles:
  - The optimized code cannot change the original intention of the program.
  - Optimization should focus on consuming fewer resources and speeding up the software.
  - The optimization process shouldn't significantly increase compilation time.

#### Here are some common optimization techniques:
  - Function Lining: replaces function calls with the contents of the function's body.
  - Dead Code Elimination: gets rid of code that is never executed, or who's return result is never used.
  - Loop Fusion: executes operations in adjacent loops that have the same iteration conditions.
    - ex:
  - Instruction Combining: combines instructions that do similar operations.
    - ex: `x=x+10; x=x-7;` combines into `x=x+3;`

### Code Generation

In this step, the compiler finally converts optimized intermediate code into machine code for its targeted machine. The final code should have the same meaning as the source code, and be more efficient for memory and CPU usage.

# {Common tools/strategies used}

## Tools

##### Apktool

A tool designed to reverse engineer third party, binary Android apps.

##### dex2jar

A tool that can convert classes.dex files to classes.jar, or vice versa, in order to view source code of Android applications using any Java decompiler.

##### diStorm3

A decomposer library that disassembles instructions into various bit-sizes.

##### edb-debugger

A 32-bit debugger tool that analyzes binary code, for Linux devices. One of its main goals is modularity.

##### Jad Debugger

A java decompiler that converts .class files into source code.

##### Javasnoop

A tool to test the security of java applications. It lets you attach an existing process and instantly begin tampering with it.

##### OllyDbg

A 32-bit debugger tool that analyzes binary code, for Windows devices.

# {Demo in Java + "Java isn't normally used, but we are using it purely for presentation purposes."}
