# HiFi1_NDSP
NatureDSP Library for HiFi 1 and HiFi 1s DSP cores
Note: Both HiFi 1 and HiFi 1s have single repository

# The repo is organized as follows.

## xws:
  * Last stable release version of the NDSP containing two xws files.
  * An xws each, for the library-kernels and the test-driver.
    Ex : HiFi1s_VFPU_library_v200.xws & HiFi1s_VFPU_demo_v200.xws
  * Building and executing the xws in Xtensa Xplorer is described in the API Reference Document. 
  * Detailed release documentation can be extracted from lib.xws/doc folder.

### Release v2.0.0 Brief: 
  * Release Date : Apr-2025.  
  * The source code has been updated to make it compatible with RJ-2024.4 tool chain.
  * Verification & testing has been done with a very limited number of HiFi 1/1s cores,  RJ-2024.4 tool chain (LX8.0.4).
  * The same source code can be built for both HiFi1/1s cores, with and without LP option enabled.

## NDSP_HiFi1
This contains the source code along with make files that will build in linux environment.  

## doc folder
This contains help documentation on how to build the source code in linux and run the performance and functional regressions. 
