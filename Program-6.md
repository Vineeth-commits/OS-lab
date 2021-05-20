##Shell script to print a gross salary of an employee
---
```bash
#!/bin/bash

echo "Enter basic salary:"
read basic
if [$basic -lt 1500]
then
    gross=`expr $basic*0.2`
elif [$basic -gt 1499] && [$basic -lt 2000]
then
    gross=`expr $basic*0.3`
else
    gross=`expr $basic*0.4`
fi
echo "gross salary = $gross"
```