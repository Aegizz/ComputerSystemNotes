Add two, one bit inputs. Outputs a carry and a sum bit.
#Code 
```HDL
CHIP HalfAdder {

IN a, b; // 1-bit inputs

OUT sum, // Right bit of a + b

carry; // Left bit of a + b

  

PARTS:

// Put you code here:

And(a = a, b = b, out = carry);

Xor(a = a, b = b, out = sum);

}
```

#BasicArithmetic

[[HalfAdder.hdl]]
