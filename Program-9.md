## Shell program to list out all the files and directories separately
---
```bash
#!/bin/bash

echo "enter the file name"
read dir

for file in "$dir/"
do
    [[-d "$file"]] && echo "$file is a directory"
    [[-f "$file"]] && echo "$file is a regular file"
done
```