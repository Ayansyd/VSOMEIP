# VSomeIP Installation and Setup

## Introduction

VSomeIP (Vehicle Service Oriented Middleware over IP) is an implementation of the SOME/IP protocol. This README provides instructions on how to install and set up VSomeIP.

## Prerequisites

- CMake (version 3.13 or higher)
- Boost (version 1.55 or higher)
- GCC (version 5.0 or higher)
- Git (for version control)

## Installation Steps

### 1. Clone the VSomeIP Repository

```sh
git clone https://github.com/COVESA/vsomeip.git
cd vsomeip

# 2. Build VSomeIP
mkdir build
cd build
cmake ..
make

# 
Sure! Here is a README.md file to guide through the installation and setup of vsomeip.

markdown
Copy code
# VSomeIP Installation and Setup

## Introduction

VSomeIP (Vehicle Service Oriented Middleware over IP) is an implementation of the SOME/IP protocol. This README provides instructions on how to install and set up VSomeIP.

## Prerequisites

- CMake (version 3.13 or higher)
- Boost (version 1.55 or higher)
- GCC (version 5.0 or higher)
- Git

## Installation Steps

### 1. Clone the VSomeIP Repository

```sh
git clone https://github.com/COVESA/vsomeip.git
cd vsomeip

#2. Build VSomeIP

mkdir build
cd build
cmake ..
make

# 3. Install VSomeIP

sudo make install

#4. Set Up Environment Variables
Ensure the following environment variables are set:

export LD_LIBRARY_PATH=/your/custom/path/lib:$LD_LIBRARY_PATH
export VSOMEIP_CONFIGURATION=/path/to/vsomeip.json
export VSOMEIP_APP_NAME=World

Replace /your/custom/path with your actual installation directory and /path/to/vsomeip.json with the path to your configuration file.
If you have not changed any custom path then find the vsomeip installation directory through

# command to find the vsomeip installation directory

sudo find / -name "vsomeip"

and cd into paths till you can find the vsomeip.hpp file which would be your directory
```
# you would require a vsomeip config file which is included along with sample client and server programe 

# CMakeList is also available for the program , make path changes if required

# to Build build directory

cmake -Bbuild -DCMAKE_INSTALL_PREFIX=../../install_folder -DCMAKE_PREFIX_PATH=../../install_folder .

# to build the make file 

cmake --build build/

# to run the executable file 

LD_LIBRARY_PATH=../../install_folder/lib/:$PWD/build/ ./build/service-example
LD_LIBRARY_PATH=../../install_folder/lib/:$PWD/build/ ./build/client-example

# For any other reference you could go through the official document

https://github.com/COVESA/vsomeip/wiki/vsomeip-in-10-minutes#intro





