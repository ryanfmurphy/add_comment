add (bash script)
=================
adds a text remark to the end of a text-based file


Usage
-----
```
add <file> <msg>
```


Example usage at shell prompt
-----------------------------
```
notes "#todo Call that cool girl I met at that party"
```


Description of behavior
-----------------------

Appends remark to end of text file.

Leaves an extra newline between the new remark and the existing content.


Limitations / #Todo
-------------------

File must exist / #todo check if file exists and if not, create it


Original Code
-------------
```
#!/bin/bash

# add (bash script): adds a text remark to a text-based file
#  example usage at shell prompt:
#   $ notes "#todo Call that nice girl I met at that party"
#  description of behavior:
#   leaves an extra newline between the new remark and the existing content

file="$1"
msg="$2"
if [[ `tail -n 1 "$file"` ]];   then echo "" | cat >> "$file";   fi
echo -e "$msg" | cat >> "$file"
```

