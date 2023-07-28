#BasicLogicGates

If (a = 1)
	return 1;
If (b = 1)
	return 1;
else
	return 0;
#Code 
```HDL
CHIP Or {

IN a, b;

OUT out;

  

PARTS:

Not(in = a, out = NotA);

Not(in = b, out = NotB);

Nand(a = NotA, b = NotB, out = out);

// Put your code here:

}
```
#TruthTable 

| a   |  b  | out |
| --- |:---:|:---:|
| 0   |  0  |  0  |
| 0   |  1  |  1  |
| 1   |  0  |  1  |
| 1   |  1  |  1  |
[[Or.hdl]]
