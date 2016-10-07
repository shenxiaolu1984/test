# Introduction

cpp-torch is a C++ library, implemented as a wrapper around [Torch](https://github.com/torch) **C libraries** (not lua libraries).

Using this library, you can:

- load torch data tensor from `.t7` file
- load torch network model from `.t7` file
- feed data into model, perform forward pass and get output

**All in C++, without touching lua.**

Pretty handy when you want to distribute an off-the-shelf Torch model.

# Install


# Get started
A simple load-and-fire routine looks like this in C++:

```c++
... code here
```

We also provides an [example script]() to test the famous [CMU OpenFace](https://github.com/cmusatyalab/openface) model. This network transfers a 3 * 96 * 96 face image into a 128 * 1 feature vector, representing the identity of the person.

# Performance
This wrapper is **about 2x faster** than Torch's lua implementation in CPU mode.

|model|torch|cpp-torch|
|----|----|----|
|nn4.small2|?|?|


# Progress
Currently, this library only supports forward pass in CPU mode of most of the modules in [nn package](https://github.com/torch/nn), and related functions in [Torch package](https://github.com/torch/torch7).
Check [this list]() to see supported modules.


# Next step work
- Foward pass of other modules in nn package
- Wrapper for GPU mode
- Backward pass of modules in nn package
- Unit test 
