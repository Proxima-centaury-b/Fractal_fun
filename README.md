# Introduction

Some classical fractal sets powered by Numba framework (Nvidia) to have faster computation. As I haven't Nvidia GPU, I run this notebook on CPU only, but the way Numba computes greatly optmize the calculation time. So it is useful for people whitout an up-to-date NvidiaGPU to compute their programs.

- Also, bigger the data is, bigger will be the spread between with and without Numba (and of course much more with a suitable GPU). 
- However, for small datasets, it has the inverse effect; indeed, the transfert of the data to the GPU + GPU calculation takes more time than CPU calculation, but the difference is very thin.


Some references on GPU vs CPU  and Numba :

[1] [Medium article](https://medium.com/geekculture/executing-a-python-script-on-gpu-using-cuda-and-numba-in-windows-10-1a1b10c29c9)

[2] [Numba official doc](https://numba.readthedocs.io/en/stable/cuda/index.html)

Numba is an Open Source NumPy-aware optimizing compiler for Python sponsored by Anaconda. It uses the LLVM compiler infrastructure to compile Python syntax to machine code. It is aware of NumPy arrays as typed memory regions and so can speed-up **code using NumPy arrays and functions, and loops**.

The most common way to use Numba is through its collection of decorators that can be applied to your functions to instruct Numba to compile them. When a call is made to a Numba decorated function it is compiled to machine code “just-in-time” for execution and all or part of your code can subsequently run at native machine code speed you want to compile with @jit for "just-in-time". Numba will compile them for the CPU (if it can resolve the types used).
With numba, the compilation of a python function is then triggered by a decorator.  A python decorator is a function that takes another function as input, modifies it, and returns the modified function to the user. 


### Some well-known Numba limitations

* Numba compile individual functions, not whole programs
* Numba supports a subset of Python, Some dict/list/set support, but not mixed types for keys and values
* Numba supports a subset of Numpy (not all functions and all arguments are available)
* Numba does not support Pandas

### Fractals

For a brief historic review of Mandelbrot's fractals, see https://www.ibm.com/ibm/history/ibm100/us/en/icons/fractal/

Most common fractals : https://en.wikipedia.org/wiki/List_of_fractals_by_Hausdorff_dimension
https://en.wikipedia.org/wiki/Mandelbrot_set
https://en.wikipedia.org/wiki/Julia_set



