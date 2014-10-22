add (bash script)
=================
adds a text remark to a text-based file
usage: add <file> <msg>

example usage at shell prompt
-----------------------------
notes "#todo Call that cool girl I met at that party"

description of behavior
-----------------------
appends remark to text file
leaves an extra newline between the new remark and the existing content

original code
-------------
   #!/bin/bash
   file="$1"
   msg="$2"
   if [[ `tail -n 1 "$file"` ]];   then echo "" | cat >> "$file";   fi
   echo -e "$msg" | cat >> "$file"

