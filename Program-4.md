##Shell script to perform arithmetic operations
---
```bash
#!/bin/bash

#Addition
echo "Enter two integers to add:"
read a b
result=`expr "$a + $b" | bc`
echo "$a + $b = $result"

#Subtraction
result=`expr "$b - $a" | bc`
echo "$b - $a = $result"

#Multiplication
result=`expr "$a * $b" | bc`
echo "$a * $b = $result"

#Division
result=`expr "$a / $b" | bc -l`
# -l option loads the standard math lib with scale set to 20 as default
echo "$a / $b = $result"
```