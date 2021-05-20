##Shell script to generate multiplication table
---
```bash
#!/bin/bash

echo "Multiplication Table:"
echo "Which table do you want?"
read n 
i=0 
while [ $i -le 10 ] 
do 
echo " $n x $i = `expr $n \* $i`" 
i=`expr $i + 1` 
done
```
![](Screenshots/Program-5.png)