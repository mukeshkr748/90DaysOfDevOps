Day 06 - Linux File Practice

Today I practiced some basic Linux file commands in terminal.

## Create File

```bash
touch notes.txt
This command created a new file.
Write Text in File
Bash
echo "Today I started Linux file practice" > notes.txt

Added first line in file.
Bash
echo "Learning basic DevOps commands" >> notes.txt

Added second line.

Bash
echo "Practicing read and write commands" | tee -a notes.txt

Added third line using tee command.

Read File
Bash
cat notes.txt

Used cat command to read full file.
Bash
head -n 2 notes.txt

Used head command to check first 2 lines.
Bash
tail -n 2 notes.txt

Used tail command to check last 2 lines.
What I Learned

Today I learned

how to create a file
how to write text inside a file
how to append new lines
how to read file content

#90DaysOfDevOps