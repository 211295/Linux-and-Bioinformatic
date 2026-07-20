# Tutorial Linux and Bash Language 
### Central Processing Unit and Memomry
    The kernel (operating system kernel) manages the computer's resources, such as the Central Processing Unit (or "CPU"), the memory, all input/output (I/O), etc., and allows other programs to run and use these resources.
     The CPU gets commands and data from the working memory, processes them, and returns the results to working memory.
     A single CPU can have more than one processing core (a “mini-CPU” within), example: dual-core, quad-core, octo-core etc
     The RAM (random access memory) is a set of chips that function as the working memory of the computer. RAM is usually the system component that is most crucial to computer speed.
     The RAM stores commands and data that are being actively used: everything  you see on the screen is in a form of RAM (either the main system memory or a video card’s memory).
    If your RAM gets full, a part of the hard-disk drive (or SSD, solid state drive) is used as auxiliary working memory.
    The amount of data that can go into RAM is measured in multiples of bits or bytes (Gb or GB for gigabits or gigabytes, respectively). Data in RAM disappears when the computer is turned off


    The Linux command line is a text interface, and called shell, terminal, console, prompt... The shell, also known as (aka) a Command Line Interpreter (CLI), is a text-only interface between the user and the kernel.
     Its main function is to read the commands that are typed in the terminal window by the user and execute them. Just a keyboard and screen, with no power to run programs locally. There was no mouse, no fancy graphics, not even any choice of colour. Everything was sent as text, and received as text.
- **examples of shell** : sh , csh , tcsh , bash  

    The programs can be drived by to external programs that can be installed on the computer, however UNIX (or UNIX-like) operating systems come with many built-in command-line interface programs and shell utilities:

- **File system** -> cat, cd, chmod, chown, chgrp, cksum, cmp, cp, dd, du, df, file, fsck, fuser, ln, ls, lsattr, lsof, mkdir, mount, mv, pax, pwd, rm, rmdir, size, split, tee, touch, type, umask
- **Processes** -> at, bg, chroot, cron, fg, kill, killall, nice, pgrep, pidof, pkill, ps, pstree, time, top
- **User environment** -> clear, env, exit, finger, history, id, logname, mesg, passwd, su, sudo, uptime, talk, tput, uname, w, wall, who, whoami, write
- **Text processing** -> awk, banner, basename, comm, csplit, cut, dirname, ed, ex, fmt, head, iconv, join, less, more, paste, sed, sort, spell, strings, tail, tr, uniq, vi, wc, xargs
- **Shell builtins** -> alias, echo, expr, printf, sleep, test, true, and, false, unset, wait, yes
- **Networking** -> dig, host, ifconfig, inetd, netcat, netstat, nslookup, ping, rdate, rlogin, ssh, traceroute
- **Searching** -> find, grep, locate, whatis, whereis
- **Documentation** -> apropos, help, man
- **Miscellaneous** -> bc, dc, cal, date, lp, lpr

     Hardware initialization when The BIOS (Basic Input/Output System) execute (the firts code of software). In other words 'puts in an available state' every piece of hardware, such as the network card, the hard disk, the graphic card, the optical drive, the keyboard, the mouse, etc.
     When every piece of hardware is initialized, the BIOS of the motherboard tries to start the Opening Sistem. The OS is started and takes control, eventually.
     The OS kernel searches for known hardware... It loads the drivers for every computer hardware found... It creates interfaces for applications to communicate with the computer hardware... It starts all system services. Its waiting for user make the command

# The binary code: base 2, digits only 0 and 1 
## "*There are only 10 kinds of people: the people how knows the binary code, and the people how doesnt know the binary code*"
nth position of the number is the power of base 2, and the number (0 or 1) mutiply the 2^n
| Number base 2 | Number base 10 | 1 x 2^n or 0 x 2^n | 
|:-------------:|:--------------:|:--------------------------------------:|
| 0 | 0 | 0x2<sup>0</sup> |
| 1 | 1 | 1x2<sup>0</sup>  | 
| 10 | 2 | 1x2^<sup>1</sup>  0x2<sup>0</sup>  |
| 11 | 3 | 1x2^<sup>1</sup>  + 1x2<sup>0</sup> |
| 101 | 5 | 1x2<sup>2</sup> + 0x2<sup>1</sup> + 1x2<sup>0</sup> | 
| 111 | 7 | 1x2<sup>2</sup> + 1x2<sup>1</sup> + 1x2<sup>0</sup> | 
| 10001 | 17 | 1x2<sup>4</sup> + 0x2<sup>3</sup> + 0x2<sup>2</sup> + 0x2<sup>1</sup> + 1x2<sup>0</sup> | 
| 11111 | 31 | 1x2<sup>4</sup> + 1x2<sup>3</sup> + 1x2<sup>2</sup> + 1x2<sup>1</sup> + 1x2<sup>0</sup> | 
| 1001010 | 74 | 1x2<sup>6</sup> + 0x2<sup>5</sup> + 0x2<sup>4</sup> + 1x2<sup>3</sup> + 0x2<sup>2</sup> + 1x2<sup>1</sup> + 0x2<sup>0</sup> |
| 11111111 | 255 | 1x2<sup>8</sup> + 1x2<sup>7</sup> + 1x2<sup>6</sup> + 1x2<sup>5</sup> + 1x2<sup>4</sup> + 1x2<sup>3</sup> + 1x2<sup>2</sup> + 1x2<sup>1</sup> + 1x2<sup>0</sup> | 


A byte is a set of 8 bits (and a bit is a binary code, 0 and 1): 
2^0 = 1 = 1 bit                                    10^0 = 1 = 1 bit
2^3 = 8 = 8 bits = 1 byte
2^10 = 1,024 b = 1 KIBIbit                         10^3 = 1,000 kb = 1 KILObit
2^20 = 1,048,576 Kib =  1 MEGIbit                  10^6 = 1,000,000 Mb = 1 MEGAbit
2^30 = 1,073,741,824 Gib =  1 GIBIbit              10^9 = 1,000,000,000 Gb = 1 GIGAbit
2^40 = 1,099,511,627,776 Tib = 1 TEBIbit           10^12 = 1,000,000,000,000 Tb = 1 TERAbit

[Shift] + [Insert] = Ctrl V
green is the terminal and. ~ is the way to your user terminal. / is the root, and below that, we have a top-down tree
The prompt display tree things in the screen: the name of computer/server
                                              the name of currently directory ~ 
                                              the user name
<server> :~ <user_name> $
## Hierarchical structure
    Many sub directories which organize the files and sub directories of the system.
| Hierarchical filesystem structure | Whats means&Content | 
|:----------------------:|:---------------------------------------------------------------------------------------------------------------------------|
| /home | where user data lives, users home |
| /bin | - common programs - shared by the system - the system administrator and the users - executable files available to all users |
| /sbin | programs for use by the system and the system administrator |
| /boot | the startup files and the kernel. In some recent distributions also grub data. Grub is the GRand Unified Boot loader |
| /dev | contains references to all the CPU and peripheral hardware, which are represented as files with special properties, device drivers - screen, keyboard, disks, etc. |
| /etc | important system configuration files; administrative and information files | 
| /initrd | on some distributions, information for booting | 
| /lib | library files, includes files for all kinds of programs needed by the system  and the users, shared library files |
| /lost+found | every partition has a lost+found in its upper directory; files that were saved during failures are here |
| /mnt | standard mount point for external file systems, e.g. a CD-ROM or a digital camera; common place to mount external media |
| /net | standard mount point for entire remote file systems |
| /opt | typically contains extra and third party software |
| /proc | a virtual file system containing information about system resources |
| /root | the administrative user's home directory. Mind the difference between /, the root directory and /root, the home directory of the root user | 
| /tmp | temporary space for use by the system, cleaned upon reboot, used by many programs as a temporary file storage place | 
| /usr | programs, libraries, documentation etc. for all user-related programs. Originally intended to keep all user-related commands |
| /var | storage for all variable files and temporary files created by users, such as  log files, the mail queue, the print spooler area, space for temporary storage of  files downloaded from the Internet, etc. | 

## Files
Under UNIX, file extensions are arbitrary and do not have a particular meaning (Windows have tree letter extensions). So convencionaly in Linux have some cods to reference a kind of files
- <file>.sh = shell scripts, text files containing a series of shell commands
- <file>.pl = perl scripts, text files containing PERL commands
- <file>.py = python scripts, text files containing PYTHON commands
- <file>.txt = text files with no particular format
- <file>.csv = text files with Comma-Separated Values, generally used in tables
- <file>.fasta = text files containing sequences in FASTA format

| ABSOLUTE PATH - starts at the root '/' | RELATIVE PATH - starts at the current directory |
|:----------------------------------------|------------------------------------------------:|
|/home/user/<directory>/<folder>/<file>.txt | <file>.txt |
| ~/<directory>/<folder>/<file>.txt | ./<file>.txt | 

| CURRENT DIRECTORY | PARENT DIRECTORY |
|:---------------------------|---------------------------:|

###################################################################################################################################################################################################################
Standard input (stdin) is represented by number 0, where data comes from to enter the program
Standard output (stdout) is represented by number 1, where data goes when it gets out of the program
Standard error (stderr) is represented by number 2,  where program errors (or warnings or diagnostic messages) go to when issued
List of commands accept only stdin : less, more, tail, head 
List of commands accept only stdout : rev , colrm
List of commands use to redirect the stdin : 
List of commands use to redirect the stdout : 
List of commands dont accept either: mkdir , cd , wget , 
 > : redirect STDOUT to the file named after the sign / can create new files OR OVERWRITE AN EXIST FILE, so be carefull
<command> <file> > <other_file> = make a direction of the archive to save in "other_file"
 2> : redirect STDERR to the file / only the erro will and redirect to the file / can create new files OR OVERWRITE AN EXIST FILE
 >> : redirect, appending STDOUT to the file
 2>> : redirect, appending STDERR to the file (Redirect standard error from program to file, appending)
<file> 2>> <other_file> = redirect JUST A STARDAR ERROR (STDERR), appending to a existing file
 < : redirect STDIN from a file to a programm
<new_file> < <file> = redirect the standard input (STDIN)
 << : redirect STDIN as a here-document,
 <<< : redirect STDIN as a here-string to a program
 && :
 & : 
<command_line> > <file> 2>&1 = It is possible to merge STDOUT and STDERR and send them to the same file
<command_line> &> <file> = the same above / send the two streams to the same file 
<command_line> >> <file> 2>&1 = Appending, without overwrite, the STDOUT and STDERR in the previous exist file
<command_line> &>> <file> = 
<command> && <command> = 
<command> & <command> = 
. = currently directory
.. = directory above currently directory

######################################################## Metacharacter ##########################################################################################################################################
. = Any character. You represent a caracther with dot
^ = anchor the beggin of line 
$ = anchor the end of line
[  ] = enclose a character list so its a OR b OR c ... Can be used as a range or a 
[^ ] = is the same above but negation the content among the brackets
ls [XYZ]* = show list files with started X OR Y OR Z
* = quantifier zero or more occurrences
\ = remove the metacharacter "special power" and belong a normal characher, therefore is the literal value of the character
\ = in some programms make the normal character change the mean and gives new power for them
 | = concatenate 2 or more commands in one line (its a pipe), redirect STDOUT of one program to STDIN of the next program.
<command1> | <command2> | <command3>  =  STDERR does not get in the pipe, by default, so use |& to have the STDERR go along with STDOUT
+ = match the preceding element one or more times
? = match the preceding element zero or one time
( ) =  group some parts of the regex, and save the match in a special variable

################################################################# Securities ###################################################################################################################
Access rights in Linux are defined by WHO can take the acess and WHAT KIND of acess (see chmod command)
user: the user who owns the file                                    | read: permission to display the content of the file
group: other users in the same group as the user who owns the file  | write: permission to modify the content of the file - add or remove some content
others: all the other users in the system                           | execute: permission to run a file - scripts or compiled programs

~$ ll <file>
<type_of_file><permissions> <number_of_> <owner_of_the_file> <gruop> <size_file> <modification_time> <file_name>
-             rwx rwx rwx   62          fssalles             LDG                 Month Day Hour      file
             user group others
r = Read the file
w = Write the file
x = eXecute the file
file type d = Directory
file type l = Link
###################################################################################################################################################################################################################
make list and viewr the conttents of a directory
ls = list show ; -l = in list way | -a = show hidden files in the shell that start the name with dots "." | -h = print size with parameters | -s = size | -r = reverse the list
[work with a list, similar in python and there is a commands to work as a strings]
ls - l [abcdef] OR ls - l [a-f] = make a list of all files start with 'a' to 'f' exist
ls abc[defghi] OR ls abc[d-i] = make a list of all files have the letters d to i after 'abc', so the files are abcd , abce , abcf , abcg , abch , abci PAY ATENTION DONT WORKS FOR NUMBERS just 1-9
ls abc? = wild-card character to represent exactly one of any kind of character after 'abc'
ls abc{d,e,f,g,h,i} or ls abc{d..i} = PAY ATENTION ON DOTS BETWEEN 'd' AND 'i' MEANS YOU WANNA GET A RANGE LIKE IN [ ] and the resutl is te same as "ls abc[d-i]"
ls abc{$((10*5)),$[2**5]} = show list (literaly) of "abc50" and "abc32". the coma ( , ) separate the lists
ls {*.jpg,*.jpeg,*.png} = show all files with respectives ending
ls /abc/d*f = takes all files in 'abc' directory start to 'd' and finish with 'f' (litteraly) doesn't matter the length name, therefore the * menas zero or more characters 
ls /abc/defg[h-o]* = shows all files in 'abc' directory with name 'defg' follow with letter 'h' to 'o' and doesn't matter the  length name | SAME OF ls /abc/defg{h..o}*
ls /abc/defg[hijl]* = shows all files in 'abc' directory with name 'defg' follow with letter 'h' to 'l' and doesn't matter the legnt name
ls /abc/defg[hijl]? = shows all files in 'abc' directory with name 'defg' follow with letter 'h' to 'l' and have just one more letter after the string variate, therefore just a file with 6 letters
ls abc??* = shows all files start with 'abc' following any 2 characteres, and more or equal than 5 letters _ _ _ _ _ ...
ls -l [a-f] | wc -l > new_file = create a list of files start with a to f, pipe with counter, then count the lines was created by ls -l and finely appeding to a new_file 
ls -R * = show all files with content recursivaly, therefore 
ls -r * = show all files in reversed sort way
ls -t * = show all files with sorted by modification time, newest in the top| (-t) --time
ls -l *[!txt] = show all files in a list except files ending with 'txt'
ls A*[!4-9].txt = show all files started with 'A' and DONT HAVE the numberes 4,5,6,7,8,9, and ending with txt
 
file command determine file type. It tests each argument in an attempt to classify it.
file </PATH/file> = show the kinds of file is   | ASCII text = American Standard Code for Information Interchange, is the most common format for text files in computers
                                                | gzip compressed data = show the name of file without the .gz
                                                | symbolic link to <open sistem>/<file>
                                                | ELF 64-bit LSB pie executable, x86-64, dynamically linked, interpreter <PATH of >, for GNU/Linux <version>, BuildID[sha1]=<cod>, stripped
                                                | HTML document, ISO-8859 text
                                                | JPEG image data, JFIF standard 1.01, resolution (DPI), density IxJ, segment length <INT>, baseline, precision <INT>, IxJ, components <INT>
                                                | 
file <directory> = print that is a directory
file -d <file> = show some debug inside the file
file -apple <file> = 

mkdir <PATH/name_directory> = make a directory / (-p) = creat a parent directory does not exist 
mkdir -p new_direc{src,doc/{mail,ref},data} = creat "new_direc" with other 3 directories (src , doc and data) and inside doc/ we have 2 more directories (mail and ref)

cd <name_directory> = change directory

apropos <some_word>= find a word that describre a command, so you can find all commands you wanna with the some_word 
apropos -e <key_word> = find some describe command that exactly have the word you want | (-e) = exactly
apropos <pattern> -a <other_key_word> = you add more words, concatenete | (-a) = --and 

kill literely kill the programm, or command 
which -a <filename> = locate a command, returns the pathnames

help = 

touch <nameoffile.txt> = create a text with name <nameoffile.txt> 

alias is a buitl programm that allow manage aliases. Create shortcut of programms
alias <shortcut>='<programm with options>'
alias ll='ls -alF'
alias la='ls -A'
alias l='ls -CF'
alias gc='grep -c'
alias gv='grep -v'
alias wl='wc -l'
alias usort='sort -u'
alias hn='head -n'
alias tn='tail -n'
alias cAt='cat -A'

nano .profile
nano .bashrc
###################################################################################################################################################################################################################
pwd = check you directory, print work directory 

df check the disk free, i.e. system resource
in this order : Filesystem     1K-blocks   Used    Available    Use%     Mounted on
df ./ = see the disk space in the disk in the curently directory
df -h ./ = see the numbers used and available disk in "huma`n-redable", print the size of powers of 1024 (e.g 

du see how much space each directory is taking 
du ./ = see how much space it in the currently directory
du -sh = look the number of memory used | (-s) total space | (-h) human redable
du -b = look the number in BYTES | (-b) --bytes or --apparent-size 

free Display amount of free and used memory in the system in kibibytes (as default)
free = you can see : total        used        free      shared  buff/cache   available
free -h = look a human readable numbers

lscpu Display information about the CPU architecture. 
Architecture: CPU op-mode(s); Address sizes; Byte Order
CPU(s): On-line CPU(s) list
Vendor ID: CPU family;  Model; Thread(s) per core; Core(s) per socket; Socket(s); Stepping; BogoMIPS; Flags. 

top - display Linux processes
htop - similar to top but is a interactive process viewe - Percentage of CPU cores and memory being used by each program

who Show a list of who is currently in the system, logged on, in which terminal, and from which original address (IP number or not)
w Show who is logged on and WHAT they are doing, i.e. what program each user is running 

whoami prints our username

id command prints our userid, username, primary groupid, primary group name and secondary group(s) id

env run a program in a modified environment. Set each NAME to VALUE in the environment and run COMMAND. 

printenv print all or part of environment

groups prinnt the groups that a user is in.

man <command_you_wanna_learn> = MANUAL OF THE COMMAND, extremy usable 

history shows a list of all previusly command by the shell, can acess by [UP ARROW] and with start with blank space, the command or line wont be save
Another way is to use the [Ctrl+r] combination. The prompt will wait for us to type some characters and it will find the matching command by searching in reverse order through the history list.
history = show a list of previusly command 
!534 = plays the 534th command in the list

info <command_you_wanna_learn> or <documentation> = Read documantion and info of commands
export [biult programm] and define the PATH (absolute and relative) or change the PATH. Each directory in the list is separated from the next by a colon (:)
There is set of environmental variables whose names start with LC {LC_NUMERIC, LC_TIME, LC_MONETARY} the locale of the systemm, which defines aspects related to language, time/date format, currency, numbers. 
The code en_US.UTF-8 define American English, pt_BR.UTF-8 define Brasilian features.
export PATH=$PATH:~/<directories> = 
export LC_TIME=pt_BR.UTF-8 = define the time of brasilian locate
export LC_MONETARY=pt_BR.UTF-8 = define the currency Real (R$)

date - print or set the system date and time
date = <day_week> <month> <day> <hour> <  > <year>
echo "This is the $date of the CPU"

screen = Multiplexes a physical terminal between several processes. It creates a single window with a shell in it and then gets out of your way so that you can use the program as you normally would.
         You can create new (full-screen) windows with other programs in them (including more shells), kill existing windows, view a list of windows, turn output logging on and off, 
         copy-and-paste text between windows, view the scrollback history.  All windows run their programs completely independent of each other.
         Programs continue to run when their window is currently not visible and even when the whole screen session is detached from the user's terminal.

uname print system information
uname -s -p OR uname -sp = print the kernel name (nucleus of the PC) | (-s) = default --kernel-name 

cal display a calendar (december 9999 is the boundery)

bg 
###################################################################################################################################################################################################################
more AND less viewrs, not editors, pagers presentation on scree. Do not read the complete file before. Display the contents of a file in a terminal
zmore AND zless = variants of more and less, respectively, that deal with compressed data (.gz)
more +5 <file> = just show the line 5 to the end
more +/<pattenr_in_file> <file> = start displaying content after a specific piece of text is first found. Filter for  paging  through text one screenful at a time
less <file> = show the file just in the limit of the screen, press SPACE to roll down, or the "inside" less use <crtl B "> = divide the screen in two and you can see the command line and the less window
                     . use /<parttner_in_file> = can find a specific word after press the / and press N to next match
less +/<pattenr_in_file> <file> = same as more, but the less display, after finding the first match, you can see the next by typing n (next match)
less -S <file> = do not want the lines to be wrapped ("break") on the screen, but to be chopped instead. Easier to see "tables"

fold wrap each input line to fit in specified width. Wrap input lines in each FILE. have just 3 options
fold -b -s -w <INT> <file> = (-b) = count bytes rather than columns | (-s) break at spaces | (-w) use WIDTH columns instead of 80

head see just the beginning (10 lines) of the file or the standard output (STDOUT)
head -n x <file> = shows the first X lines you want | (-n) --lines
head -c <files> = show the bytes of the files | (-c) --bytes
head -n -x <file> = print all lines but the last X lines from file.
tail see just the end (10 lines) of the file or the standard output (STDOUT)
tail -f <file> = it gets to the end and then waits for new data to arrive, then shows that, and so on. Output appended data as the file grows. | (-f) --follow

conCATenate files and print on the standard output, show the strings in text
zcat = variant of cat that deals with compressed data (.gz)
cat <file1> = just print the standard output in the screen
cat <file1> <file2> <file3> > new_files = take all the files and concatenate in a new_file in the same other as given
cat <file1> - <file3> = read the contents of file1, then the contents of STDIN, then the contents of file3 will be sent to STDOUT; finally, it will send everything, in that order, to STDOUT
cat -A </directory/file> OR cat -vET </directory/file> = -E show the $ in the end of each line, and display a TAB charactares with ^I
cat -bvn /etc/passwd = make a list of user informations | (-b) --number-nonblank, only the non-empty lines show up numbered | (-v) --show-nonprinting | (-n) --number show the number all output lines
cat -b <PATH/file> = show just the nonblank lines and numbered that one, so  
cat </PATH/file> | more +5 = print the number 5 to the end of lines
cat </PATH/file> | less +9 = print the number 9 to the end of lines, but in the full screen, if smaller than the screen = (~) complete every line
cat -s </PATH/file> = the consecutive repeated empty lines are not shown, suppress repeated empty output lines
cat -n </PATH/file> = print together with the content of the file the number of lines (until the empyts)
cat -E <PATH/file> = print $ at the end of line after the content of the line | (-E) --show-ends display the $ in the end
ls -l /usr/ | cat </PATH/file1> - </PATH/file2> > ~/<output_file>

tac concatenate and print files in reverse, reverse of cat
tac <options> <file> = inverse the lines of the text file

rev <file> = reverse the intery line, but not the lines each

print world count, newline count, and byte count for each FILE, and a total line count if more than one FILE is specified them. wc will tell you some basic statistics about the text file
wc -w <file> = how many words the file have (e.g fsdf235 is a word because non-zero-length sequence of characters delimited by white space)
wc -l -L <file> = how many lines the file have and how lentgh is the biggest one | (-L) --max-line-length
wc -c <file> = how many bytes have
wc -m <file> = print the character counts
sort -u <file> | wc -l = how many unique lines there are in file

uniq lines, report or omit repeated lines SORTED FILES
sort <file> | uniq -c -i <file> <output_file> = see the number of occurrences of each kind of line, doesnt matter differences in case | (-c) --count, show the number of occurrences each line | (-i) --ignore-case
sort <file> | uniq -d <file> <output_file> = show the lines exit more than 1 time | (-d) --repeated only print duplicate lines, one for each group
sort <file> | uniq -D <file> <output_file> = | (-D) print all duplicate lines
sort <file> | uniq -u <file> <output_file> = show unique lines, so with have repeative lines, dont print | (-u) --unique

grep Global Regular Expression Print prints all lines that contain a certain piece of text (or text pattern) provided
grep -c "<pattern>" <file> = count the number of lines with pattern
grep -v -i "<pattern>" <file> = show the lines DONT HAVE the pattern, invert the sense of matching and the case became insensitive | (-v) --invert-match | (-i) --insensitive
grep -w "<pattern>" <file> = the string or pattern given by the user can be part of a word | (-w) --word-regexp
grep -e "<patter1>" -e "<pattern2> -e "<pattern3>" -i <file> = show the lines with those patterns, and ignoring the case distinctions | (-e) --regexp=PATTERN
grep -l "<pattern>" <file*> = show the name of files have the pattern | (-l) --files-with-matches 
grep -L "<pattern>" <file*> = same above but oposite sense | (-L) --files-without-match
grep -w xaxa <file> | cut -f X | sort -u = take all lines in file with have the pattern "xaxa" (can be a part of a word), cut and show only the X position (column), and finally show unical line
grep '^<pattern>' <file> = following the matches lines started with just with those pattern
grep '<pattern>$' <file> = following the matches lines ended with just whit those pattern
grep '[^abi]' <file> = match lines that contain at least one character that is different from a, b OR i (which could match even if the lines also happen to have one of those characters!)
grep '^[abi]' <file> = anchor the begging of line, should be a, b OR i. Match lines started with a, b OR i
grep '...[abi]$' <file> = anchor the end of line, the line have 4 characters and end with a OR b OR i
grep '[i^g]..aa <file> = match lines that contain i, g or ^ followed by two characters of any kind, followed by "aa"
grep -i '^..j.r$' <file> = show just the lines with the last position "r" and the third "j" (^ anchor the begginig and $ anchor the end)
grep -E '<pattern1>|<part2>|<part3>' <file> = Interpret PATTERNS as extended regular expressions | (-E) --extended-regexp
grep -E '(<pattern>){x}' <file> = match the line pattern with x (INT) repetitions
grep -E '(<pattern>){,x}' <file> = 
grep -E '<pattern>{,x}' <file> = without paretheses
grep -E '(<pattern>){y,x}' <file> =
grep -F 

sed filter and transform text, allows do in-place editing: you can change the “original file” if you want. Create a 'temporary file' and send output to this file rather than to the standard output
PROCESS LINE BY LINE
Stream EDitor is a line editor, i.e., it edits contents line by line, independently {non-interactive editor}
sed '<command>' <file*> = the commands most commonly are '/<pattern>/<replacement>/<flag>/', so substitute the first part for the second following some options
                                                          /<pattern>/d/ = delete lines containing “pattern” 
                                                          /<pattern>/p/ = print lines containing “pattern”
                                                          /<pattern>/<replacement>/s/ = substitute the "pattern" with "replacement"
                                                          /<pattern>/a/ = appending the "pattern"
                                                          /<pattern>/<replacmente>/c/ = change the "pattern" with "replacement"
                                                          /<pattern>/<replacement>/g/ = change all occurrences
                                                          /<pattern>/<replacement>/I/ or i/ = case insensitive
                                                          /<pattern>/<replacement>/<INT>/ = command in the Nth occurrence
                                                          /<pattern>/<replacement>/x,y,z/ = command at only lines xth , yth and zth
                                                          /<pattern>/<replacement>/x,y!/ = command at all lines except xth to yth 
sed '<N>d' <file> = delet Nth first lines for the file, could be a header
sed '<N>,<P>d' <file> = delet the Nth to Pth lines
sed '<N>,<P>!d' <file> = delet all lines except the Nth to Pth
sed '/^$/d' <file> = delet all blank lines, using the (^) to anchor the begging of the line and ($) the end of the line, so without something between then, means a blanked line
sed 'g/<pattern>/d' <file> = delet all lines with the pattern
sed '/<pattern>/,/[x-y]$/d' <file> = delet from the first line that have the pattern through the firt line end with digits between x to y
sed 'x,/<pattern2>/d' <file> = delet all lines with the pattenr2 from x to the first blank line
sed '/<pattern1>/s/<pattern2>/<pattern3>/' <file> = the most commum, substitute (s) the pattern2 by 3 following the lines with matches pattern1
sed -n 'x,y!p' <file> = print all file except x to y | (-n) --quite, suppress automatic printing of pattern space
sed -n '$=' <file> = Counts the number of lines,  
sed -n -f <script_file> <file> = use the script as a pattenr or a command to sed use in file
sed 's/<pattern1>/<pattern2> &/' <file> = replace the pattern1 to 2, but rewrite the pattern1 also | (&) replaced by the entire string matched in the regular expression for pattern
sed '<N>q' <file> = show all Nth first lines
sed -r  's/([0-9]{2})\/([0-9]{2})\/([0-9]{4})/\3-\1-\2/' <file> = substitute the YYYY-MM-DD to DD-MM--YYYY | (-r) = use the extended regular expression 
        's#([0-9]{2})/([0-9]{2})/([0-9]{4})#\3-\1-\2#'
(s#) substitution command with # separator | ([0-9]{2}) match 2 digits, put in \1 space | (/) match a single /, not more a Metacharacter | ([0-9]{4}) match 2 digits, put in \2 | 
        's*([0-9]{2})/([0-9]{2})/([0-9]{4})*\3-\1-\2*'
        's%([0-9]{2})/([0-9]{2})/([0-9]{4})%\3-\1-\2%'
        's|([0-9]{2})/([0-9]{2})/([0-9]{4})|\3-\1-\2|'
        's.([0-9]{2})/([0-9]{2})/([0-9]{4}).\3-\1-\2.'
        's ([0-9]{2})/([0-9]{2})/([0-9]{4}) \3-\1-\2 '
        's(\([0-9]{2})/\([0-9]{2})/\([0-9]{4})(\3-\1-\2('

awk is useful for manipulation of data files, domain-specific language developed to extract data out of text streams. Parses each input line using “blanks” as a delimiter 
A sequence of “blanks” is one delimiter, therefore empty fields (columns) will get collapsed by default. If the data is delimited using the space bar character, it could solve using a character list ([ ])
awk is a filter, but it can also get data from one or more files. The structure is very similar to that of sed
PROCESS FIELD BY FIELD
A from Aho, W from Weinberger, K from Kernighan        
awk [options] '<script>' <file> = the script most commonly are  '-f <script_file>', inside the single quots to specify this is a script 
                                                                '/<pattern> {print $0}' = print all lines and collumns contain the pattern
                                                                '/<pattern> {print $x $y $z}' = print all lines with pattern and just the collumns x y z in that order
                                                                '
                                                                '
                                                                '
                                                                '
                                                                '
awk -F "; " '/<pattern> {print $y '\t' $x}' <file> = print the columns y and x in this order, couting by every ';' as a delimitor of each collumn, and print a blanck space between the x and y by ('\t')
awk -F "'\t'" '/<pattern> {print $y "" $x}' <file> = the same above but you swith the way to print a blanck space
awk '<pattern> {print  $x " + " $y " = " $x+$y} <file> = 
    '{print $x + 200 " reais"} <file> = Print just the x collumn plus 200 , and complete the sentense with word " reais"
    '$x < p {print $0}' <file> = Print all collumns and just the lines with the 'xth' collumn lower than 'p' value
    'p < $x < n {print $3 $2 $1}' <file> = Print the collumns 3,2 and 1 in that order, with the value of 'xth' collumn among 'p' value and 'n' value
    '/^>/ {if (seqlen){print seqlen}; print ;seqlen=0;next; } { seqlen += length($0)}END{print seqlen}' <file>.fasta = print lentgh of FASTA files with 

awk -F "\s" '{sum+=$x} END {print sum}' <file>.xlsx = summ all the lines of Xth position in a "table"

###################################################################################################################################################################################################################
copy files and directories
cp <file> ~/<PATH>/<new_name> / 
cp -r /<directory/ <file1> <file2> <file3> -t ~/<PATH>/<target> = copy the directory you want and all files into directory | (-r) recursively | (-t) target where you would like to copy
cp -u -i -p <file> <new_file> = (-u) update, copy only missing information to new file | (-i) ask you sure make this copy because cp OVERWIRTE the new copy | (-n) oposite of -i | (-p) preserves the atributes
cp -l <file> <new_name> =  hard link files instead of copying
cp -f <file> <other_file> = --force
cp -s <file> <new_name> = --symbolic-link make symbolic links instead of copying, is almost the same ln

scp - speciall copy, when you would like to copy files from one server to other. Bidirectional.
scp <user>@<remote_computer>:</PATH/file> <local_desired> = take the file of remote compupter of user copy to the local desired
scp -P <door> <file> <server>/<usrer>/<PATH>/ 
scp -P <door> -r ./<directory> <serve/username/directory/folder> = copy a holy directory to other username | (-P) "port" the dor of server | (-r) Recursivally the kind of the file  

rysnc is a fast, versatile, remote (and local) file-copying tool

rm <file> = remove any archive or folder 
rm -r <directory> = remove the directory, (-r) remove recursively thing

translate (i.e. substitute) is the default, squeeze (i.e. eliminates repetitions), and/or delete characters from standard input, writing to standard output
tr a-z A-Z < <file> = all lower-case letters have been changed to upper-case
tr '[:lower:]' '[:upper:]' < <file> = same as above, use [:_____:] and inside "character class" (e.g alnum, alpha, blank, lower, punct, space, upper, xdigit)
tr -d -c '[:alnum:]' < <file> = delete everything in file that is not a letter or number, so gets the complement of the characters listed | (-d) --delete | (-c) --complement
tr -d '[:cntrl:]' < <file> = remove non-printing (invisible) characters from the file | (cntrl) all control characters
tr -s <file> = replace each sequence of a repeated character that is listed in the last specified | (-s) --squeeze-repeats  with a single occurrence of that character
tr " " "\\n" < <file>.csv | grep "<pattern>" | sort -u | wc -l = transform the space in a new line 
tr " " "\\n" < <file>.csv | grep "<pattern>" | sort | uniq -c | sort -nr | head -n <x> = 

rename files at time supplied according to the rule specified as the first argument
rename -v 's/<pattern>/<replacement>/' <files*> = replace the pattern literaly (like in sed), and verbose that | (-v) --verbose
rename -d 's/<pattern>/<replacement>/' <files*> = Do not rename directory with the same pattern in files | (-d)
rename 'y/A-Z/a-z/' <files*> = 
rename 's/\<pattern>$//' <files*>.<pattern> =  remove the pattern in the end of the name of all files.
rename 's/$/<replacement>/' <files>* = insert a new piece in the name at the end, with dollar sign $ showing where anchor the replacement
rename 's/__/<replacemente>/' <files> = insert a new piece in the name at the beggining, with  showing where anchor the replacement

move files and rename them, ACTUALLY you just move the content of the file with other, with annoter name
mv <PATH/file> <PATH/diretory/> = move the file to the directory you want | (-i) ask the intention | (-u) update, move only the missing information | (-n) not alowed to mv overwrite
mv <file_name> <new_name> = change the name of file in currently directory
for file in <files_name*>; do mv $file $file.<pattern>; done = add a pattern in the end of name, as the rename command above
mv -r <directory> <PATH/directory/> = move the entier directory to other plance 
mv <file1> <file2> <file3> -t <PATH/directory/> = move all those files to a directory targeted | (-t) --target-directory=<PATH/DIRECTORY>
mv -v <file> </PATH> = saying what happen | (-v) --verbose

###################################################################################################################################################################################################################
echo writes each given STRING to standard output (STDOUT), with a space between each and a newline after the last one
echo $((expr)) = STRDIN 0
echo $((2*30)) OR echo $[2*30] = 60
echo $((5*90/6)) OR echo $[5*90/6] = 75, because we have 90 divided by 6 and multiply for 5
echo $((5+6*8-90/5)) OR echo $[5+6*8-90/5] = 35, 5 + 48 - 18. Remainder 35
echo $((5+(6*8-90)/5)) OR echo $[5+(6*8-90)/5] = -3, 5 + (48-90)/5 = 5 + (-42)/5 = 5 - 8,4 = -3
echo $((5+(6*8-90)%5)) OR echo $[5+(6*8-90)%5]= 3, because the % means the remainder of the division, so (-42)/5 remainder -2. 
echo {x..y} OR {y..x} = will print the range x to y (decresment and incriscment)
echo {x..y..z} = will print the range x to y with the logical z
echo -n "<count_strings_in_a_text>" | wc -c
echo

tee command read the standardinput and redirect as a standardoutput

expr evaluate the arithimetic and ____ expressions
expr <arg> & <arg>
expr <arg> < <arg>
expr <arg> <= <arg>
expr <arg> = <arg> 
expr <arg> != <arg>
expr <arg> >= <arg>
expr <arg> > <arg>
expr (<INT>*<INT> + <FLOAT> - <INT>)/<INT> 

bc an arbitrary precision calculator language, rigth 'quit' to exit the 
bc  = print the version, copyright and move to a 'new terminal'
bc -l   = (-l) = --mathlib, create a math library
bc -i  = (-i) = --interactive, force the interactive mode 
echo "(5+7.5)3" | bc = print the arithimatic to bc 'terminal' and print the calculate
echo "10/3" | bc = print just the integral number division, example = 3
echo "scale=100, 10/3" | bc = now print 100 numbers after the cout ',', show the decimals places


###################################################################################################################################################################################################################
find search for files in a directory hierarchy. search for files, the output is a list of files or directories, you can concatenet with others commands (wc, head, less, tail, sort)
find / -name <file> 2> /dev/null
find ~ -name '*x.*' -size +5M
find ~ -name '*.sh' -size -50k
find ~ -name 'O*' -type d 
###################################################################################################################################################################################################################
column utility formats its input into multiple columns, provides a format tabel for data.
column -t <file> = display columns data (with fields separated by “white space”, such as tabs or spaces) in a table
column -s '<delimeter>' <file> = use something different from white space as the field delimiter
column -t -s $'\t' <file> | less -S = creat the less page of the table format with tab as a delimeter (cod of tab is $'\t')
column -tn <file> = make more close each other

cut, remove sections from each line of files, uses the TAB character as the default column delimiter. Print selected parts of lines from each FILE to standard output. 
cut -f <INT> <file> = print only the column you especify by INT number | (-f) = --fields=LIST, select only these fields
cut -f x,y,z <file> OR cut -f z,x,y <file> = both are the same thing, doesnt matter the order in input
cut -f x,y <file> = print only the column number x and column number y
cut -f <INT> -d <delimiter> <file> = print only the column number <INT> | (-d) --delimiter=<DELIM> use delimiter instead of TAB for field delimiter 
cut -s <file> = print the | (-s) = --only-delimited, do not print lines not containing delimiters
cut -f x,y <file> | sort -n -k 2,2 = get the columns x and y , and after pipe sort results numerically by the second column (originally, column y)
cut -f x,y <file> | sort -k 2 -nr | uniq | head -n 20 = show the first 20 lines of x and y columns, without repetition, sorted by bigger number to smaller number of second column (originally, column y)

colrm allows to delet columns from the file, specify 2 numbers (started ended), if just 1 number, remove all columns after the number. The TAB counts for 8 columns, and space count 1 column
colrm x y < <file> = remove the columns starting x position and finishing in y position
colrm x < <file> = anything after x position are discarded
colrm x y < <file1> > <file2> = send the content of file1 in colrm, which remove the columns starting x position and finishing at y position, and redirect to file2
split a file into pieces, the default size is 1000 lines. Break files into smaller subsets. Creates new files called fileaa, fileab, fileac
split -a X <file> = generate suffixes of length X 
split -n N <file> P = generate N pieces with same size (based on input size) and the output recive the name P... |(-n) = --number
split -n K/N <file> = output Kth of N to stdout, its means 
split -n l/N <file> = split into N files without splitting lines/records
split -n r/N <file> = like 'l' but use round robin distribution

nano is small, free and friendly editor
Vim is a text editor that is upwards compatible to Vi. It can be used to edit all kinds of plain text. It is especially useful for editing programs.
nano -Y <name> <file> = Specify the name of the syntax highlighting (change the colors) to use from among the ones defined in the nanorc files
nano -L <file> = open the editor and don't automatically add a newline when a file does not end with one | (-L) --nonewlines
nano -B <file> = When saving a file, back up the previous version of it, using the current filename suffixed with a tilde (~) | (-B) --backup
nano -H <file> = Save the last hundred search strings and replacement strings and executed commands, so they can be easily  reused  in  later  sessions | (-H) --historylog
-B, --backup
When saving a file, back up the previous version of it to the current filename suffixed with a ~.
-C <dir>, --backupdir=<dir>
Set the directory where nano puts unique backup files if file backups are enabled.
-D, --boldtext
Use bold text instead of reverse video text.
-E, --tabstospaces
Convert typed tabs to spaces.
-F, --multibuffer
Enable multiple file buffers, if available.

fold wrap each input line to fit in specified width, 
fold <big_file> = Convert the lines of the file to fit the width, for example, the maximum limit of screen

###################################################################################################################################################################################################################
sort lines of text files, ordenate the list of files or directories by differents parameters (numerical, alphabetical, month)
sort -b <file> = sort the lines of files ignoring the leading blanks. Search fields are separated by blank-space (spaces or TAB), but that can be changed using an option
sort -k <INT> -n <file> = sort according to numerical value and the x position you would like to sort | (-n) --numeric-sort | (-k) --key=KEYDEFF (for start and stop position), gives location and type
sort -g <file> = sort according the global numerical value, utility for numbers between 1 and 0 (0<x<1) | (-g) --global
sort -k x,x <file> = just sort by the x position
sort -k x,y <file> = sort by the x position to y position, like a dictionary 
sort -k x,xn -k y,yd -k z,zM <file> = sort by x position numerically, y position alphabetically, z position by Months (n , d , M are in KEYDEFF)       
sort -r <file> = sort the file but reverse the result of comparisons | (-r) --reverse
sort -M <file> = compare< 'JAN' < ... < 'DEC' | (-M) --month-sort
sort -h <file> = compare human readable numbers (e.g., 2K 1G)
sort -f -u <file> = sort the lines ignoring case character and output only the first of an equal run | (-f) --ignore-case | (-u) --unique
sort -R <file> = "sort" by random way | (-R) --random-sort
sort -r <file> = reverse order EXTREMELY USEFULL | (-r) --reverse
sort -t <file> = sort uses white-space (spaces or tabs) as field delimiters | (-t) --field-separator=SEP use SEP instead of non-blank to blank transition
sort -c <file> = simply check whether a file is sorted or not, and dont sort | (-c) --check, --check=diagnose-first
sort -t , -k x <file> = sort the data in x position after the comma ',' (separator) |

shuf generate random permutations. Write a random permutation of the input lines to standard output.
shuf -o <out_put> -r <file> = write result to FILE instead of standard output and allow the repeats lines | (-o) --output=OUTPUT | (-r) --repeat
shuf -n <INT> <file> = create a shuffle lines and delimited by the number you want of a file, if the number is higher than the lines, will use just the lines there are in file | (-n) --head-count=COUNT
shuf -i 0-9 = print digits 0 to 9, one per line, randomly
shuf -i 0-9 -r -n 50 = print 50 digits (0 to 9) randomly
shuf -e heads tails -r -n 50 = simulate 50 coin tosses | (-e) echo so its a like a print you would like to shuffle
shuf -e A T C G -n 10000 -r -z | fold -w 70 = creat a sequence of fasta file | (-z) --zero-terminated, line delimiter is NUL, not newline

paste put things together, so join different files into one, which will be present as a column in the new file, creating a table
paste <file1> <file2> <file3> = create a table out of files in the order
paste -d ',$' <file1> <file2> <file3> = create a table separating the column 1 and 2 by "," and the 2 and 3 by "$" | (-d) --delimiters=LIST
paste -s <file> = transpose the lines in columns and vice-versa, like in a matrice switing the i and j each other | (-s) --serial

join lines from two files based on one common column (on a common field) containing an identifier string. The files must be sorted based on that common column.
join j -1 <file1> <file2> = take the column 1 of the “join field” was construct, therefore, print the file1 and 2
join j -2 <file1> <file2> = take the column 2 of the "join filed" was construct, therefore, print file1 and 2
join -1 x -2 y <file1> <file2> = take the column X of file1, and take the column Y of file2
sort <file*> | join -1 2 -2 1 <file1> <file2> = sort files and create a table with 2 columns using the second column of the first file in first FIELD, and and the first column of the second file in second FIELD
join -a <INT> <file1> <file2> = print lines that did not have the join field found in both files | (-a) print unpairable lines coming from file x number, where x is 1 or 2, corresponding to <file1> or <file2>


###################################################################################################################################################################################################################
chmod Change Mode changes the file mode bits of each given file according to mode, which can be either a symbolic representation of changes to make, or an octal number representing the bit
The  format  of a symbolic mode is [ugoa...][[-+=][perms...]...], where perms is either zero or more letters from the set rwxXst, or a single letter from the set ugo. 
The letters rwxXst select file mode bits for the affected users: read (r), write (w), execute (or search  for  directories)  (x), execute/search  only if the file is a directory or already has execute permission
for some user (X), set user or group ID on execution (s), restricted deletion flag or sticky bit (t).
A combination of the letters "ugoa" controls which users' access to the file will be changed: u = users, g = other users inside the group, o = other users NOT in the file's group, a = all users
(+) plus add the permission, (-) minus remove the permission
chmod o-rx <file> = remove the permission of others of read and write
chmod a+rwx <file> OR chmod ugo+rwx= give the permission of all to write, read and execute
chmod ug+rw o-xw <file> = give the mermission only to group and user to read and write, and remove the execute and write permission of others 
A numeric mode is from one to four octal digits (0-7), derived by adding up the bits with values 4, 2, and 1.
read (r) recive value 4, write (w) recieve value 2, execute (x) recive value 1. And the itereation of them recieve the sum
r and x = 4 + 1 = 5 / r and w  = 4 + 2 = 6 / r, w and x = 4 + 2 + 1 = 7
chmod 750 <file> = remove the permission of others of read and write
chmod 777 <file> = give the permission of all to write, read and execute
chmod 664 <file> =  give the mermission only to group and user to read and write, and remove the execute and write permission of others
Multiple symbolic modes can be given, separated by commas.
chmod u=rwx,g=rx,o=rx <file> = user can read, write and execute/ group and others can only read and execute

chgrp 
chgrp -r <file> = change the group recursively down a directory | (-r) recursively
 
chown Generally can only be used by users with admin rights so you are unlikely to use this command

###################################################################################################################################################################################################################
wget is a non-interactive download of files from the Web (HTTP, HTTPS, FTP formats; htmml, xhtml, ccs pages). Can work in the background, while the user is not logged on. Create local versions of remote web sites
wget <httml/:___________________.com> = download the archive directly on terminal
wget -drc <httml/:____.com> OR wget -d -r -c <hhtml/:_____.com>
wget -l 1 -r -e robots=off -A "*.gz" <htmml/:_____.com> = 
wget -R <httml/:_______.com> = limit what kinds of file names you will reject while downloading
