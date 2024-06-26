# DISCONTINUATION OF PROJECT #  
This project will no longer be maintained by Intel.  
Intel has ceased development and contributions including, but not limited to, maintenance, bug fixes, new releases, or updates, to this project.  
Intel no longer accepts patches to this project.  
 If you have an ongoing need to use this project, are interested in independently developing it, or would like to maintain patches for the open source software community, please create your own fork of this project.  
  
# AMX-TMUL-Code-Samples-Intel
Code sample showing Intel® Advanced Matrix Extensions (Intel® AMX) functionality on Intel® Xeon® Scalable processor Max Series and 4th gen Intel® Xeon® Scalable processors.

Intel® AMX now introduces new extensions to the x86 Instruction Set Architecture (ISA) to work on matrices and which may accelerate matrix multiplication in AI workloads. It consists of two components:

1. A set of 2-dimensional registers (tiles), which can hold sub-matrices from larger matrices in memory.
2. An accelerator called Tile Matrix Multiply (TMUL) which contains instructions that operate on tiles.

This code sample demonstrates testing the new instructions using intrinsic functions.

A code walk-through for this sample can be found at:
https://www.intel.com/content/www/us/en/developer/articles/code-sample/advanced-matrix-extensions-intrinsics-functions.html


## Purpose

The code sample will multiply matrices A and B of size 16 x 64 containing INT8 values, and accumulate the result to a 16 x 16 matrix C containing INT32 values.

This code sample is simplified to highlight use of new Intel(R) AMX instructions. It shows use of instructions to configure the tiles, load data from memory into tiles, perform one matrix multiplication on tiles data and copy the result from tiles to memory. It should not be used as a basis for production code. Only for demostration purposes.

## License

This code sample is licensed under MIT license.  

##  Building the `test-amxtile` executable 

### On a Linux* System
Perform the following steps:
1. Build the program. 

   ```   
    cd src/ 
    make 
    ```

2. Run the program 

    ```
    ./test-amxtile  
    ```

3. Clean the program  
  
    ```
    make clean  
    ```

