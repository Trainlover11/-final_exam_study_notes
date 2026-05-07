## 1. How to clone a GitHub repository
`git` + `clone` + `URL`

## How to use the git commands
`git` + `pull:`

`git` + `add` + `.`

`git` + `commit` + `-m` + `label for your changes here`

`git` + `push:`

## How to write a Markdown file that contains images and proper formatting
You save the file as .md file. This is how you insert images ![src](screenshot.png).

## How to convert a Markdown file to PDF
You right-click and click the Markdown PDF: export (pdf) option

## 2. How to compress (zip) a directory/folder in Debian
Go to files, right click the zip file and press extract.

## 3. What are Absolute paths and relative paths? 
Absolute path - The full address of the file.
Relative paths - identifies the location of the directory.

## 4. How to work with the manual pages (man command)
`man` + `option`

## 5. How to parse (search) for specific words in the manual page
grep  "word"  file

## 6. How to redirect output (>, >>, and |)
>

## 7. How to append the output of a command to a file
>>

## 8. How and when to redirect the output of a command to another (pipes)
cat file.txt | grep "error"

## 9. How to use echo and output redirection to create a new file that contains some text
echo "hi" > file

## 10. How to use wildcards (For copying and moving multiple files at the same time)
You can use the *. 
mv ~/Downloads/Nature/* ~/Pictures/wallpapers/
cp ~/Downloads/homework/*.pdf ~/Downloads/*.txt ~/Projects/school/

## 11. How to use brace expansion (For creating entire directory structures in a single command)
mkdir -pv project_jupiter/site/{old,new}/{code/{scripts,markup},assets/{img,mp3,mp4}}

## 12. How to create a simple “hello world” shell script
Echo "hello world"

## 13. How to use variables in a shell script
Assign it using a = operator and to refer to it put a $ before the variable name

## 14. For each of the following commands, include a definition, syntax/formula/usage/, and 2 - 5 well-documented examples

## * AWK

* **Definition:**
  * Awk is used for displaying and processing text.
* **Formula:**
  * `awk` + `options` + `{awk command}` + `file` + `file to save (optional)`
* **Examples:**
  * Print first field of /etc/passwd file.
    * `awk` + `-F:` + `'{print $1}'` + `/etc/passwd`
  * Print the last field of the /etc/passwd file.
    * `awk` + `-F:` + `'{print $1}'` + `/etc/passwd`
  * Print the first and last field of the /etc/passwd.
    * `awk` + `-F:` + `'{print $1," = ",$NF}'` + `/etc/passwd`
  * Prints the length of a line(record),
    * `awk` + `'{print length($0)}'` + `/etc/passwd`
  * Start printing a file from a given line.
    * `awk` + `'NR > 3` + `{ print }'` + `/etc/passwd`


## * CAT

* **Definition:**
  * The cat command is used for displaying the content of a file.
* **Formula:**
  * `cat` + `option` + `file(s) to display`
* **Examples:**
  * Display the content of a file located in ~/Documents/sample_files/Code/helloWorld.py
    * `cat` + `~/Documents/sample_files/Code/helloWorld.py`
  * Display the content of a file.
    * `cat` + `-n` + `~/Documents/sample_files/Code/helloWorld.py`


## * CP

* **Definition**
  * Copies files and directories from a source to a destination.
* **Formula:**
  * `cp` + `files to copy` + `destination`
* **Examples:**
  * To copy directories you must use the -r option.
    * `cp` + `-r` + `directory to copy` + `destination`
  * To copy a directory with absolute path.
    * `cp` + `-r` + `~/Downloads/wallpapers` + `~/Pictures/`
  * To copy  the content of a directory to another directory.
    * `cp` + `Downloads/wallpapers/*` + `~/Pictures/`
  * To copy a file.
    * `cp` + `Downloads/wallpapers.zip` + `Pictures/`
  * To copy multiple files in a single command.
    * `sudo` + `cp` + `-r` + `script.sh` + `program.py` + `home.html` + `assets/` + `/var/www/html/`

## * cut

* **Definition**
  * Used to extract a specific section of each line of a file and display it to the screen.
* **Formula:**
  * `cut` + `option` + `files`
* **Examples:**
  * Display a list of all the users in your system.
    * `cut` + `-d` + `':'` + `-f1` + `/etc/passwd`
  * Display a list of all the users in your system with their login shell.
    * `cut` + `-d` + `':'` + `-f1,7` + `/etc`

## * grep

* **Definition**
  * Grep is used to search text in a given file.
* **Formula:**
  * `grep` + `option` + `search criteria` + `file(s)`
* **Examples:**
  * Search any line that contains the word "dracula" in the given file.
    * `grep` + `'dracula'` + `~/Documents/dracula.txt`
  * Search any line that contains the word 'dracula' regardless of the case.
    * `grep` + `-i` + `'dracula'` + `~/Documents/Books/dracula.txt`
  * Display how many lines contain the matched string.
    * `grep` + `-c` + `'dracula'` + `~/Documents/Books/dracula.txt`
  * Search for all the lines that do not contain the word 'war'.
    * `grep` + `-v` + `'war'` + `~/Documents/Books/war-and-peace.txt`
  * Display your user's information as stored in the /etc/passwd.
    * `grep` + `-i` + `$USER` + `/etc/passwd`

## * head

* **Definition**
  * The head command displays the top N number of lines of a given file.
* **Formula:**
  * `head` + `option` + `file(s)`
* **Examples:**
  * Display the first 10 lines of a file.
    * `head` + `~/Documents/Book/dracula.txt`
  * Display the first 5 lines of a file.
    * `head` + `5` + `~/Documents/Book/dracula.txt`
  * Display the first 5 lines of multiple files.
    * `head` + `-n` + `5` + `Txt/{dracula,war-and-peace}.txt`
  * Display the first line of multiple files using wildcards.
    * `head` + `-n` + `1` + `Csv/*.csv Code/*.py`
  * Display a given number of lines of the output of a given command.
    * `ls` + `-l` + `~/cis106/` + `|` + `head` + `-n` + `2`

## * ls

* **Definition**
  * List files.
* **Formula:**
  * `ls` + `directory`
* **Examples:**
  * Long list including hidden files.
    * `ls` + `-al` + `directory/to/list`
  * List all files classified.
    * `ls` + `-R` + `directory/to/list`

## * man 

* **Definition**
  * An interface to the system reference manuals.
* **Formula:**
  * `man` + `option` + `command`
* **Examples:**
  * How to display debugging.
    * `man` + `-d`
  * How to display the source nroff file.
    * `man` + `-w`

## * mkdir

* **Definition**
  * Used for creating directories.
* **Formula:**
  * `mkdir` + `the name of the directory`
* **Examples:**
  * Create a directory in the present working directory
    * `mkdir` + `wallpapers`
  * Create a directory in a different directory using relative path.
    * `mkdir` + `wallpapers/forest`
  * Create a directory in a different directory using absolute path.
    * `mkdir` + `~/wallpapers/forest`
  * Create a directory with a single quote in the name.
    * `mkdir` + `wallpapers/"majora's mask"`
  * Create multiple directories
    * `mkdir` + `wallpapers/cars` + `wallpapers/cities` + `wallpapers/forest`

## * rm

* **Definition**
  * Removes files and directories.
* **Formula:**
  * `rm` + `option`
* **Examples:**
  * Remove a file.
    * `rm` + `list`
  * Remove an empty directory.
    * `rmdir` + `Downloads/games`
  * Remove an non-empty directory.
    * `rm` + `-r` + `Downloads/games`
  * Remove a file and prompt confirmation before removal.
    * `rm` + `-i` + `list`
  * Remove all the files inside a directory and ask before removing more than 3 files.
    * `rm` + `-I` + `Downloads/games/*`

## * mv

* **Definition**
  * Moves and renames directories
* **Formula:**
  * `mv` + `source` + `destination`
* **Examples:**
  * To rename a file.
    * `mv` + `homework.docx` + `cis106homework.docx`
  * To move a file from a directory to another using relative path.
    * `mv` + `Downloads/Homework.pdf` + `Documents/`

## * TAC

* **Definition**
  * Displays the contents of a file.
* **Formula:**
  * `tac` + `option` + `file(s) to display`
* **Examples:**
  * Display the content of a file located in ~/Documents/sample_files/ in reverse order.
    * `tac` + `~/Documents/sample_files/Code/helloWorld.py`
  * Display the content of multiple files in reverse order.
    * `tac` + `~/Documents/sample_files/Code/helloWorld.py` + `~/Documents/sample_files/Code/helloWorld.py`

## * Tail
* **Definition**
  * Shows the last N number of lines of a file.
* **Formula:**
  * `tail` + `option` + `file(s)`
* **Examples:**
  * Display the last 10 lines of a file.
    * `tail` + `~/Documents/sample_files/`
  * Display the last 5 lines of a file.
    * `tail` + `-5` + `~/Documents/sample_files/`
  * Display the first 5 lines of multiple files.
    * `tail` + `-n` + `5` + `Txt/{dracula,war-and-peace}.txt`
  * Display the first line of multiple files using wildcards.
    * `tail` + `-n` + `1` + `Csv/*.csv Code/*.py`
  * Display a given number of lines of the output of a given command.
    * `ls` + `-l` + `~/cis106/` + `|` + `tail` + `-n` + `2`

## * touch
* **Definition**
  * Used to create files.
* **Formula:**
  * `touch + option + argument`
* **Examples:**
  * To create a file called list.
    * `touch` + `list`
  * To create a file using absolute path.
    * `touch` + `~/Downloads/games.txt`

## * tr
* **Definition**
  * Translates standard input to output
* **Formula:**
  * `Standard` + `output` + `|` `tr` + `option` + `set` + `set`
* **Examples:**
  * Translate on character to another.
    * `cat file.txt` + `|` + `tr` + `'.'` + `','`
  * Translate tabs into space.
    * `cat file.txt` + `|` + `tr` + `-s` + `"[:space:]"` + `' '`

## * tree
* **Definition**
  * list contents of directories
* **Formula:**
  * `Tree` + `option`
* **Examples:**
  * List contents of directory
    * `Tree`
  * List contents of lab9.
    * `Tree` + `lab9`