Veel verzamelde is nooit grappigs van radio 3FM

Om deze te gebruiken in (Linux) fortunes:

```bash
# location fortune files
cd /usr/share/games/fortunes/

# add empty lines
sed '/%/G' isnooitgrappig.txt

# replace empty lines with %
sed 's/^$/%/' isnooitgrappig

VIM:

#remove ^M
:e ++ff=dos 

The :e ++ff=dos command tells Vim to read the file again, forcing dos file format. Vim will remove CRLF and LF-only line endings, leaving only the text of each line in the buffer.

then

:set ff=unix 

and finally

:wq 

# make fortune .dat file
strfile -c % isnooitgrappig isnooitgrappig.dat
```
