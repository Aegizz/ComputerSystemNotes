#BasicLogicGates

If && (a && b), return 1;
else
return 0;
#Code
```  

CHIP And {

IN a, b;

OUT out;

  

PARTS:

Nand(a = a, b = b, out = NotA);

Not(in = NotA, out = out);

// Put your code here:

}
```

#TruthTable 

| a   | b   | out |
| --- | --- | --- |
| 0   | 0   | 0   |
| 0   | 1   | 0   |
| 1   | 0   | 0   |
| 1   | 1   | 1   | 
[[And.hdl]]
