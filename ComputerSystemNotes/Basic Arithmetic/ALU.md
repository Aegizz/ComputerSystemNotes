Arithmetic Logic Unit

Used for basic operations
#BasicArithmetic
#Code 

```HDL

CHIP ALU {

IN

x[16], y[16], // 16-bit inputs

zx, // zero the x input?

nx, // negate the x input?

zy, // zero the y input?

ny, // negate the y input?

f, // compute out = x + y (if 1) or x & y (if 0)

no; // negate the out output?

  

OUT

out[16], // 16-bit output

zr, // 1 if (out == 0), 0 otherwise

ng; // 1 if (out < 0), 0 otherwise

  

PARTS:

// Put you code here:

Mux16(a=x, b[0..15]=false, sel=zx, out=Mux16A);

  

Not16(in=Mux16A, out=Not16X);

Mux16(a=Mux16A, b = Not16X, sel = nx, out=Mux16C);

  

Mux16(a=y, b[0..15]=false, sel=zy, out=Mux16B);

  

Not16(in=Mux16B, out=Not16Y);

Mux16(a=Mux16B, b = Not16Y, sel=ny, out = Mux16D);

  

Add16(a = Mux16C, b = Mux16D, out = Add16A);

And16(a = Mux16C, b = Mux16D, out = And16A);

Mux16(a = And16A, b = Add16A, sel = f, out = Mux16E);

Not16(in = Mux16E, out = notOut);

Mux16(a= Mux16E, b = notOut, sel = no, out = output);

Not16(in = output, out = notOutput);

Not16(in = notOutput, out = out);

  

And16Way(in = notOutput, out = zr);

  
  
  

And16(a=output, b=output, out[15] = ng);

  
  

}

```


[[ALU.hdl]]


#TruthTable 
![[Pasted image 20230728134613.png]]
