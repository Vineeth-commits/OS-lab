##Shell script to print a gross salary of an employee
---
```bash
#!/bin/bash

echo "Enter basic salary:"
read basic
if [ $basic -lt 1500 ]
then
    gross=$(($basic * 0.2))
elif [ $basic -gt 1499 ] && [ $basic -lt 2000 ]
then
    gross=$(($basic * 0.3))
else
    gross=$(($basic * 0.4))
fi
echo "gross salary = $gross"
```
![](Screenshots/Program-6.png)