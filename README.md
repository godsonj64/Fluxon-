# Fluxon-
A New Natural Language inspired Programming language 

Fluxon Official Documentation

Table of Contents

Overview
Language Goals and Philosophy
Getting Started
Syntax and Structure
4.1. Basic Concepts
4.2. Data Types
4.3. Variables
Processes
Pipelines
Contexts
Control Structures
8.1. Conditional Statements
8.2. Loops
8.3. Switch Statements
Error Handling with Shields
Macros (Metaprogramming)
HyperTypes (Dynamic Typing)
Modules and Imports
Concurrency
Tooling and Execution
14.1. Fluxon Compiler Overview
14.2. Compiling and Running Fluxon Code
Example Projects
Best Practices
FAQ
Conclusion
1. Overview

Fluxon is a programming language designed to bridge the gap between human-readable instructions and machine-executable code. It leverages natural language-inspired syntax alongside flow-based and contextual constructs (e.g., Processes, Pipelines, Contexts) to create highly readable and maintainable software. Fluxon features:

Intuitive Constructs: Familiar English-like statements.
Robust Error Handling: Shields for structured error management.
Dynamic Typing: HyperTypes for flexible data representation.
Metaprogramming: Macros for automating repetitive tasks.
Contextual Data: Encapsulation of related resources.
2. Language Goals and Philosophy

Readability and Accessibility: Lower barriers for new developers and non-programmers through a natural language-inspired approach.
Flow-Based Design: Emphasize data pipelines and sequences of Processes for clarity of logic.
Contextual Awareness: Organize code with explicit contexts that encapsulate data and shared states.
Error Resilience: Encourage graceful error handling with Shields.
Scalability and Performance: Support advanced features (e.g., concurrency, HyperTypes, macros) while maintaining efficient execution.
3. Getting Started

3.1. Installation
Fluxon requires a Fluxon Compiler. Depending on your chosen implementation:

Python-to-Python Transpiler or Python-to-C++ code generator version:
Ensure you have Python 3.x and/or a C++ compiler (e.g., g++, clang++).
3.2. Hello World
A simple "Hello, World" in Fluxon:

Create a process named "HelloWorld" with no input. Then, display "Hello, World!".

Start a pipeline called "MainFlow" by running "HelloWorld", and finally end with "EndProcess".

Create a process named "EndProcess" with no actions.
4. Syntax and Structure

4.1. Basic Concepts
Process: A self-contained block of code that takes inputs, performs operations, and may produce outputs.
Pipeline: A sequence of Processes connected to form a data flow.
Context: An encapsulation of variables and resources, promoting modularity.
Shield: A structured error-handling mechanism akin to try-catch.
HyperType: A dynamic typing mechanism allowing variables to hold multiple types.
Macro: A metaprogramming construct to automate repetitive code generation.
4.2. Data Types
Data Type	Description
Integer	Whole numbers (e.g., 42, -7)
Decimal	Floating-point numbers (e.g., 3.14)
Text	Strings or sequences of characters
Boolean	true or false values
List	Ordered collection of items
Dictionary	Key-value pairs
Set	Unordered collection of unique items
Tuple	Fixed-size, ordered collection
Optional	Value that may or may not be present
HyperType	A union-like dynamic type system
4.3. Variables
Syntax:

Initialize a [Type] variable called "VariableName" with a value of [InitialValue].
Example:

Initialize an integer variable called "counter" with a value of 0.
Initialize a text variable called "greeting" with a value of "Hello".
5. Processes

A Process is the fundamental unit of work in Fluxon. It receives inputs, performs operations, and may produce outputs.

Syntax:

Create a process named "ProcessName" that takes [Input1, Input2, ...] as input and produces [Output1, Output2, ...] as output. Then, perform [actions].
Example:

Create a process named "AddNumbers" that takes "NumberA" and "NumberB" as input and produces "Sum" as output.
Then, set "Sum" to "NumberA" plus "NumberB".
Key Points:

Inputs: Variables the Process reads to perform its task.
Outputs: Variables produced after execution.
Action Block: Contains assignments, displays, calls to other Processes, conditionals, loops, etc.
6. Pipelines

Pipelines define the flow of data through multiple Processes.

Syntax:

Start a pipeline called "PipelineName" by running "ProcessA" with [Arguments], then execute "ProcessB", followed by "ProcessC", and finally end with "ProcessN".
Example:

Start a pipeline called "MathFlow" by running "AddNumbers" with 5 and 10, then execute "PrintResult", and finally end with "EndProcess".
Explanation:

Start: The pipeline begins with a specific Process and arguments.
Then / Followed by: Chains subsequent Processes.
Conclude with: Ends the pipeline with a final Process.
7. Contexts

Contexts group related data and resources, promoting modularity and clarity.

Syntax:

Establish a context named "ContextName". Initialize variables within the context.
Example:

Establish a context named "UserContext". Initialize a text variable called "userName" with a value of "Alice". Initialize a boolean variable called "isLoggedIn" with a value of false.
Within the same Context, Processes have direct access to declared variables without explicit parameter passing.

8. Control Structures

8.1. Conditional Statements
8.1.1. If-Else

If "age" is greater than 18, then set "canVote" to true. Otherwise, set "canVote" to false.
8.2. Loops
8.2.1. For Each

For each number "i" in "numbers", do display "i".
8.2.2. While

While "counter" is less than 10, do set "counter" to "counter" plus 1.
8.3. Switch Statements
Syntax:

Switch on "VariableName":
    Case "Value1": [actions]
    Case "Value2": [actions]
    Default: [actions]
Example:

Switch on "day":
    Case "Monday":
        display "Start of the week."
    Case "Friday":
        display "End of the week."
    Default:
        display "Midweek day."
9. Error Handling with Shields

Shields provide structured error handling akin to try-catch.

Syntax within a Pipeline:

Start a pipeline called "SafeFlow" by running "RiskyProcess" with [args], shielded by "HandleError", then execute "EndProcess".
Example:

Create a process named "RiskyProcess" that takes "x" as input and produces "result" as output. Then, set "result" to 10 divided by "x".

Create a process named "HandleError" that takes "error" as input. Then, display "An error occurred: " plus "error".

Start a pipeline called "SafeFlow" by running "RiskyProcess" with 0, shielded by "HandleError", then execute "EndProcess".
10. Macros (Metaprogramming)

Macros automate repetitive tasks, reducing code duplication. Macros can generate Processes, variables, or entire pipelines.

Syntax:

Create a macro named "MacroName" that defines [template code].
Example:

Create a macro named "CreateLogger" that defines a process "LogMessage" which takes "message" as input and displays it.

Invoke macro "CreateLogger".
Generated Code:

Create a process named "LogMessage" that takes "message" as input. Then, display "message".
11. HyperTypes (Dynamic Typing)

HyperTypes allow variables to hold multiple possible types, dynamically resolved at runtime.

Syntax:

Define a HyperType called "NumberType" that can be either Integer or Decimal.

Initialize a "NumberType" variable called "measurement" with a value of 25.
Set "measurement" to 25.7.
Usage:

If "measurement" is an Integer, then display "Whole number measurement.".
Otherwise, display "Decimal measurement.".
12. Modules and Imports

Modules help organize code into separate namespaces or files for reusability.

Syntax:

Create a module named "ModuleName".
Within the module, define [Processes, Contexts, Variables].
Importing a Module:

Import "ModuleName".
Usage:

Start a pipeline called "CalcFlow" by running "ModuleName.AddNumbers" with 5 and 10, then execute "EndProcess".
13. Concurrency

Fluxon can be extended to support parallel or concurrent execution of Processes:

Parallel Pipelines: Running multiple Pipelines concurrently.
Async Processes: Declaring certain Processes as asynchronous to handle I/O-bound operations.
Example (Conceptual):

Start two pipelines concurrently: "PipelineA" and "PipelineB".
Wait for both to complete. 
Then, execute "FinalizeProcess".
14. Tooling and Execution

14.1. Fluxon Compiler Overview
The Fluxon Compiler comprises:

Lexer: Converts Fluxon source code into tokens.
Parser: Builds an AST (Abstract Syntax Tree) from the tokens.
Semantic Analyzer: Validates the AST.
Code Generator: Outputs the final code (e.g., Python, C++, or machine code).
14.2. Compiling and Running Fluxon Code
Write Fluxon Code: Create a .fluxon file.
Compile: Use the Fluxon compiler to generate Python or C++ code.
Run Generated Code: Execute the Python or compile the C++ output for a fast, robust binary.
Example Python Command:

python compiler_driver.py hello_world.fluxon hello_world.py
python hello_world.py
Example C++ Command:

python compiler_driver.py hello_world.fluxon hello_world.cpp
g++ -std=c++17 -o hello_world hello_world.cpp
./hello_world
15. Example Projects

15.1. User Registration Flow
Context "UserContext": Stores username and isRegistered.
Process "RegisterUser": Takes username, outputs registrationStatus.
Process "NotifyUser": Displays welcome message.
Pipeline "UserRegistration": Runs RegisterUser, then NotifyUser, ends with EndProcess.
15.2. Data Analytics
Context "DataSettings": Stores dataset paths.
Process "LoadData": Outputs raw data.
Process "CleanData": Inputs raw data, outputs cleaned data.
Process "AnalyzeData": Inputs cleaned data, outputs analysis results.
Pipeline "AnalyticsFlow": LoadData -> CleanData -> AnalyzeData -> Summarize.
16. Best Practices

Consistent Naming: Use descriptive names for Processes, Variables, and Pipelines (e.g., AddNumbers, FetchData).
Modular Design: Break large Pipelines into smaller sub-Pipelines or modules.
Error Handling: Use Shields for robust error management in complex Pipelines.
Leverage Macros: Automate repetitive Patterns (e.g., generating standard CRUD Processes).
Document Thoroughly: Add comments and annotations to clarify code.
Testing: Maintain a suite of test .fluxon files to validate new features or changes in the compiler.
Performance: Use concurrency or compile to C++ for performance-critical sections.
17. FAQ

Q1: Is Fluxon suitable for production systems?
A1: Fluxon is still evolving. It can be used for certain production scenarios, but thorough testing and performance benchmarking are recommended.

Q2: Does Fluxon support object-oriented programming?
A2: Fluxon primarily uses Processes and Pipelines. Object-like behavior can be emulated via Contexts or extended using Modules and advanced macros.

Q3: What are Shields?
A3: Shields are akin to try-catch blocks, letting you wrap Processes and handle exceptions gracefully within Pipelines.

Q4: How do I handle concurrency?
A4: Concurrency features can be implemented in the compiler to create parallel or async Pipelines. For now, concurrency is conceptual or requires an extended feature set.

Q5: Where can I find more examples?
A5: Check official Fluxon repositories or the community for sample Projects and advanced tutorials.

