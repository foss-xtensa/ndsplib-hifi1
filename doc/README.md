# How to Build and Run the Source Code in Linux environment
  * Get the latest or required version of HiFi 1/1s NDSP Code from GitHub  
  * https://github.com/foss-xtensa/ndsplib-hifi1
  * Unzip or extract to the destination directory. 

## The source code is organized as follows.
  * **build** - contains the make file 
  * **library** - contains the optimized kernel functions for the HiFi 1/1s core 
  * **testdriver** - contains the demo driver code to tun the library   

### It is assumed that the required HiFi core configurations and the Xtensa toolchain are set installed in the Linux environment.
 An example .cshrc file  that sets up the build environment accordingly is provided for reference 

## Setting up the environment 
  * A typical way is to place this .cshrc file in your home directory and execute the following from the command line terminal... 
  * source ~/.cshrc 
  * rj3
  * setenv XTENSA_CORE CORE_NAME     
    Ex: setenv XTENSA_CORE AE_HiFi1s_ao_7
  

## Compiling the Source Code: 
  * Navigate to the testdriver directory:   …/ NDSP_HiFi1/build/project/xtclang/testdriver
  * **CLEAN:**  make clean -j   
  * **BUILD:**  make all -j  


## Running the executable: 
  ### Navigate to the bin directory: …/ NDSP_HiFi1/build/bin
  ### Performance tests:
  * xt-run testdriver-AE_AE_HiFi1s_ao_7_llvm-Xtensa-release -mips -sanity         
  * xt-run testdriver-AE_AE_HiFi1s_ao_7_llvm-Xtensa-release -mips -brief 
  * xt-run testdriver-AE_AE_HiFi1s_ao_7_llvm-Xtensa-release -mips -full   
  ###	Functional tests:
  * xt-run --turbo testdriver-AE_HiFi1s_ao_7_llvm-Xtensa-release -func -sanity
  * xt-run --turbo testdriver-AE_HiFi1s_ao_7_llvm-Xtensa-release -func -brief
  * xt-run --turbo testdriver-AE_HiFi1s_ao_7_llvm-Xtensa-release -func -full
  * xt-run --turbo testdriver-AE_HiFi1s_ao_7_llvm-Xtensa-release -func -sanity -verbose 
  * xt-run --turbo testdriver-AE_HiFi1s_ao_7_llvm-Xtensa-release -func -sanity -fir -verbose 
  * xt-run --turbo testdriver-AE_HiFi1s_ao_7_llvm-Xtensa-release -func -brief -fir -iir -fft
