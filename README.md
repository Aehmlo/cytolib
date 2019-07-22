# C++ library for the gated cytometry data

`cytolib` provides the c++ library for users to use and interact with the `GatingSet` (the gated cytometry data structure) at c++ level.

## Installation as a R package
The **cytolib** package is installed via `R CMD INSTALL ...`. 

R packages wishing to use the libraries in `cytolib` need to:

- add `cytolib` to **LinkingTo** field in the **DESCRIPTION** file so the compiler knows where to find the headers when the user package is complied
e.g.

```
LinkingTo: cytolib
```
See **CytoML** package for the example of using `cytolib`.

## Installation as a C++ standalone library

**System requirement**
1. cmake
2. g++ (>=4.9)
3. libblas, liblapack, ZLIB, boost c++ library
4. cytolib c++ library (see https://github.com/RGLab/cytolib/blob/trunk/inst/INSTALL.txt)

**Installation**

```bash
# enter your project directory
$ cd cytolib

# it is always a good idea to not pollute the source with build files
# so create a new build directory
$ mkdir build
$ cd build

# run cmake to configure the package for your system
$ cmake ..

#To install the library to custom directory, use `-DCMAKE_INSTALL_PREFIX` option
# e.g. `cmake -DCMAKE_INSTALL_PREFIX=/usr/local` 
   
$ make

#to install the package
$ make install

```
   