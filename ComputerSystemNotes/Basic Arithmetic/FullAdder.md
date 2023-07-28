#Code 
Adding using 3 bits, outputs a sum and a carry. This can be multiplied to create a multi-bit Adder.

```HDL
CHIP FullAdder {

IN a, b, c; // 1-bit inputs

OUT sum, // Right bit of a + b + c

carry; // Left bit of a + b + c

  

PARTS:

// Put you code here:

HalfAdder(a=a, b=b, sum=smallA, carry=largeA);

HalfAdder(a=c, b=smallA, sum=sum, carry=largeB);

HalfAdder(a=largeA, b=largeB,sum = carry);

}
```
#BasicArithmetic

[[FullAdder.hdl]]
