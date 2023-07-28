#BasicLogicGates

Inverts input
if (in = 1),
return 0;
else return 1;
#Code 

```HDL
CHIP Not {

IN in;

OUT out;

  

PARTS:

// Put your code here:

Nand(a=in, b=in, out=out);

```
#TruthTable 

| in  | out |
| --- | --- |
| 1   | 0   |
| 0   | 1   |
[[Not.hdl]]
