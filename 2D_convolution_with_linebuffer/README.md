Originally, source code "convolutionco_orig" function implements 2d convolution w/ frame buffer.
Use stream interface with dataflow to pipeline subfunction.
One optimized option is to change coding style to store temporary data with line buffer, 
which can reduce hardware usage.
Furthermore, array partitioning on line buffer can realize 2d convolution with kernel size in one cycle.
Finally, pipeline the second for loop to unroll the innerloop further and achieve ii=1 pipelining, 
which enhance performance a lot!
In code_opt, convolution.cpp/convolution.h is changed to fit PYNQ implementation.

It is extended from Vivado\2019.2\examples\design\2D_convolution_with_linebuffer
  