##Shell script to generate multiplication table
---
```bash
#!/bin/bash

echo "Multiplication Table:"
echo "Which table do you want?"
read num
i = 1;
while[$num -le 10]
do
echo "$num * $i = `expr $num\*$i`"
i=`expr $i + 1`
done
```