# Shell piping examples

**command structure: input | process | output (ls -h | wc -l > out.txt)**

- ls -l /usr/bin | wc -l > bin.txt

conditional operator ( if command fails, following commands fail, however all preceeding succesfull commands are executed)

- ls -l README.md && touch newfile.txt

sort and search:

- STR=$'1. line1\n2. line2\n3. line3' (create variable)
- echo "$STR"
- echo "$STR" > lines.txt
- cat lines.txt
- cat lines.txt | sort -r (sort in reverse order)
- cat lines.txt | sort -r | less
- cat lines.txt | grep 3 (search for line containing 3)
- cat lines.txt | grep 3 > match.txt

append to file:

- echo "something" > append.txt
- echo "overwrite" > append.txt (overwrites)
- echo "something" > append.txt
- echo "another thing" >> append.txt (appends)

throwing away errors:

- ls -l /wrong/path 2> /dev/null (throwaway standard error into trash and not to screen)

viewing logs:

- tail -f /var/log/system.log (tail keeps file open and updates as it changes)
- tail -n 3 /var/log/system.log (view last 3 lines)
- head -n 3 /var/log/system.log (view first 3 lines)

other useful commands:

- history | less
- history | grep tail (with grep, to select use ! eg: !54)
- !! = repeat prev command
- CTRL-L = clear screen
