# KMBox Linux

## Introduction
This is a repo for the KMBox Linux project. The goal of this project is to create a Linux lib to connect to the KMBox device and control it.

## Usage
#### 1. Clone the repo
#### 2. Use it in your C++ project
```cpp
#include "kmbox.h"
...
```
#### (Optional) 3. Build it to a static library
```bash
g++ -c kmboxNet.cpp -o kmboxNet.o -lpthread
g++ -c my_enc.cpp -o my_enc.o
ar rcs libkmbox.a kmboxNet.o my_enc.o
```

#### (Optional) 4. Build it to a shared library
```bash
g++ -c -fPIC kmboxNet.cpp -o kmboxNet.o -lpthread
g++ -c -fPIC my_enc.cpp -o my_enc.o
g++ -shared -o kmNet.so kmboxNet.o my_enc.o -lpthread
```
