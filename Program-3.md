## Shell script to backup a directory
---
```bash
#!/bin/bash

echo "Enter the directory name to backup"
read FILE
if[-f $FILE]; then
    mv $FILE backup
    echo "Directory backed up"
else
    echo "File doesnt exist"
    exit 1
```