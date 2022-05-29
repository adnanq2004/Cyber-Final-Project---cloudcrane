# {What is reverse engineering}

##### Reverse Engineering is the process of taking a piece of software or hardware and analyzing its functions and information flow so as to understand its non-visible processes and behaviors.

# {What purpose does it serve}

##### Reverse Engineering tends to be used to look at a program from the outside in, by third parties that don't have access to the source code. For a practical example, if an anti-malware company discovers a piece of malware, they can use reverse engineering techniques to break down and understand the functions of the malware without accidentally enabling or triggering the virus.

# {How is it done + How is compiling done}

## How does Reverse Engineering

##### The specific techniques for Reverse Engineering are dependent on the specific thing its being performed on, but it typically follows three general steps:

### Information Extraction

##### In this step, the design of the object being reverse engineered is studied and extracted to see how the pieces fit together. It may involve finding and examining source code, or using tools, like disassemblers, to break a thing into its part.

### Modeling

##### In this step, the information that was extracted is abstracted to make a conceptual model, like a data flow diagram or a structure chart. This model serves as a guide to design new objects and systems.

### Review

##### In this step, the model is tested in various scenarios to ensure its an accurate abstraction of the original object. Once this step is completed, the model can be used to engineer the original object.

## How does Compiling

#####

{Common tools/strategies used}

{Demo in Java + "Java isn't normally used, but we are using it purely for presentation purposes."}

{Talk about code obfuscation, the opposite of decompiling}
