#BasicLogicGates

Select a bit dependant on a sorting bit "sel"
if sel = 1, out = b.
else a = out


```HDL
CHIP Mux {

IN a, b, sel;

OUT out;

  

PARTS:

// Put your code here:

Nand(a = sel, b = sel, out = NandA);

Or(a = sel, b = sel, out = OrA);

And(a=a, b=NandA, out = AndA);

And(a=OrA, b=b, out = AndB);

Xor(a=AndA,b=AndB, out = out);

}
```

#TruthTable 


| a   | b   | sel | out |
| --- | --- | --- | --- |
| 0   | 0   | 0   | 0   |
| 0   | 0   | 1   | 0   |
| 0   | 1   | 0   | 0   |
| 0   | 1   | 1   | 1   |
| 1   | 0   | 0   | 1   |
| 1   | 0   | 1   | 0   |
| 1   | 1   | 0   | 1   |
| 1   | 1   | 1   | 1   |
[[Mux.hdl]]