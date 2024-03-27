# HiFi1_NDSP
NatureDSP Library for HiFi1 and HiFi1s DSP cores
Note: Both HiFi1 and HiFi1s have single repository

# The repo is organized as follows.

## xws:
  * Last stable release version of the NDSP containing two xws files.

  * An xws each, for the library-kernels and the test-driver.
    Ex : HiFi1_VFPU_Library_v1_2_0.xws & HiFi1_VFPU_Demo_v1_2_0.xws

  * Building and executing the xws in Xtensa Xplorer is described in the API Reference Document. 
  * Detailed release documentation can be extracted from lib.xws/doc folder.

### Release v1.2.0 Brief: 
  * Release Date : March-2024.  
  * The source code has been updated to make it compatible with RJ-2024.3 tool chain.
  * Verification & testing has been done with a very limited number of HiFi1/1s cores,  RJ-2024.3 tool chain (LX8.0.3).
  * Sanity testing has been done for backward compatibility on xt-clang using RI-2023.11 tool chain (LX7.1.10) cores.     
  * The same source code can be built for both HiFi1/1s cores, with and without LP option enabled.

## NDSP_HiFi1
This contains the source code along with make files that will build in linux environment.  

## doc folder
This contains help documentation on how to build the source code in linux and run the performance and functional regressions. 
