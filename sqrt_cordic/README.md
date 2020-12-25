Source code use classic sqrt root algorithm first and produce three datatypes such as double, float, and float+integer input/output 
to figure out which one can achieve the lowest latency.
Next, square root cordic algorithm is introduced with fixed point datatype.
However,  no matter which algorithm is used, it has included four same subfunction and executed sequentially.
It will increase hardware utilization without any benefit.
One of optimized direction is to merge four subfunctions into one.
Because one for loop is in each subfunction, four for loops merged into one can decrease timing overhead.
Furthermore, less than one-fourth multiplexers and flip-flops will be synthesized.
Finally, optimized solution is one merged function with smaller wordlength of input/output. 
With acceptable approximated error, smaller wordlength such as 24-bit fixed point and 18-bit integer included is used.
 
It is extended from https://github.com/Xilinx/HLx_Examples/tree/master/Math/sqrt_cordic
