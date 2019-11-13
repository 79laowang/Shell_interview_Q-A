# Shell interview Q&A

The purpose of this documentation is to document common interview questions and answers about Linux shell script.

## Q&A

* [Q1: What is Shell?](#Q1)
* [Q2: What is a Shell Script? Can you name some of its advantages?](#Q2)
* [Q3: What are the different types of variables used in Shell Script?](#Q3)
* [Q4: How do you create a shortcut in Linux?](#Q4)
* [Q5: What are the various stages of a Linux process it passes through?](#Q5)
* [Q6: How to pass an argument to a script?](#Q6)
* [Q7: How to calculate the number of passed arguments?](#Q7)
* [Q8: How to get script name inside a script?](#Q8)
* [Q9: How to check if the previous command was run successfully?](#Q9)
* [Q10: How to get the last line from a file using just the terminal?](#Q10)
* [Q11: When debugging a Bash script, what command would you use to stop the execution of the program until the Enter key is pressed?](#Q11)
* [Q12: How to get the first line from a file using just the terminal?](#Q12)
* [Q13: How to get the first line from a file using just the terminal?](#Q13)
* [Q14: How to redirect both standard output and standard error to the same location?](#Q14)
* [Q15: What is difference between ‘ and ” quotes?](#Q15)
* [Q16: What is the difference between $* and $@?](#Q16)
* [Q17: Write down the Syntax for all the loops in Shell Scripting.](#Q17)
* [Q18: When should shell programming/scripting not be used?](#Q18)
* [Q19: What are the default permissions of a file when it is created?](#Q19)
* [Q20: Determine the output of the following command:](#Q20)
* [Q21: Determine the output of the following command:](#Q21)
* [Q22: Determine the output of the following command:](#Q22)
* [Q23: How booleans are used in a shell script?](#Q23)
* [Q24: How to get part of string variable with echo command only?](#Q24)
* [Q25: How to print all the arguments provided to the script?](#Q25)
* [Q26: How to print PID of the current shell?](#Q26)
* [Q27: How to print all array elements and their respective indexes?](#Q27)
* [Q28: How to print the first array element?](#Q28)
* [Q29: How many fields are present in a crontab file and what does each field specify?](#Q29)
* [Q30: How to debug the problems encountered in the shell script/program?](#Q30)
* [Q31: How to declare a readlone variable?](#Q31)
* [Q32: What are the different commands available to check the disk usage?](#Q32)
* [Q33: What is the commands to check a directory space usage?](#Q33)
* [Q34: How to open a read-only file in the Shell?](#Q34)
* [Q35: Write a shell script to get current date, time, user name, file name and working directory?](#Q35)
* [Q36: How to find all the files modified in less than 7 days?](#Q36)
* [Q37: Print a given number, in reverse order using a Shell script such that the input is provided using command Line Argument only.](#Q37)
* [Q38: How to calculate a real number calculation in shell script?](#Q38)
* [Q39: How to get the value of pi till a 20 decimal places?](#Q39)
* [Q40: Write a script to print the first 10 elements of Fibonacci series.](#Q40)
* [Q41: What is the difference between $$ and $!?](#Q41)
* [Q42: What are zombie processes?](#Q42)  
* [Q43: Print the 10th line without using tail and head command.](#Q43)
* [Q44: How will you find the total disk space used by a specific user?](#Q44)
* [Q45: Find all the files modified in less than 2 days and print the record count of each.](#Q45)


---

### Q1.
**What is Shell?**
### *Answer:* 
**The Shell is a Command Line Interpreter. It translates commands entered by the user and converts them into a language that is understood by the Kernel. The shell interprets a command typed in at the terminal, and calls the program that you want.**

---

### Q2.
**What is a Shell Script? Can you name some of its advantages?**
### *Answer:*
**A shell script is a command-containing text-file that contains commands in order of their execution. Typical operations performed by shell scripts include printing text, file manipulation, and program execution.**

   **Following are the two main advantages of shell scripting:**
+  **It facilitates developing your own custom OS with relevant features which best suit your needs.**
+  **It facilitates designing software applications according to their respective platforms.**

---

### Q3.
**What are the different types of variables used in Shell Script?**
### *Answer:*
**A shell script has two types of variables :**

  +  **System-defined variables are created/defined by the Operating System(Linux) itself. These variables are generally defined in Capital Letters and can be viewed by “set” command.**
  +  **User-defined variables are created or defined by system users and the values of variables can be viewed by using the command “echo”.**

---

### Q4.
**How do you create a shortcut in Linux?**
### *Answer:*
**This can be done with the help of links present in Linux OS.**

  +  **Hard Link: Hard links are linked to the inode of the file and have to be on the same file system as of the file. Deleting the original file does not affect the hard link.**
  +  **Soft Link: Soft links are linked to the file name and can reside on a different file system as well. Deleting the original file makes the soft link inactive.**

---

### Q5.
**What are the various stages of a Linux process it passes through?**
### *Answer:*
**A Linux process generally passes through four stages:**

  +  **Waiting: The Linux process waits for the resource.**
  +  **Running: The Linux process is currently being executed.**
  +  **Stopped: The Linux process is stopped after successful execution.**
  +  **Zombie: The process has stopped but is still active in the process table.**

---

### Q6.
**How to pass an argument to a script?**
### *Answer:*
```Bash
# cat test.sh
#!/usr/bin/env bash
echo ${1}

# bash test.sh p1
p1
```

### Q7.
**How to calculate the number of passed arguments?**
### *Answer:*
```Bash
# cat test.sh
#!/usr/bin/env bash
echo "Number of Parameters passed:$#"

# ./test.sh p1 p2 p3 p4
Number of Parameters passed:4
```
---

### Q8.
**How to get script name inside a script?**
### *Answer:*
```Bash
# cat test.sh
#!/usr/bin/env bash
echo "Script Name:$0"

# ./test.sh
Script Name:./test.sh
```
---

### Q9.
**How to get script name inside a script?**
### *Answer:*
```Bash
# cat test.sh
#!/usr/bin/env bash
var=$?
if var=0 ;then
    echo "Script was Run successfully!"
else
    echo "Script was Run failed!"
fi

# ./test.sh
Script was Run successfully!
```
---

### Q10.
**How to get the last line from a file using just the terminal?**
### *Answer:*
```Bash
# tail -1 /var/log/messages
Oct 18 03:42:46 ke-ol7vm1 nm-dispatcher: req:1 'dhcp4-change' [eth0]: start running ordered scripts...
```
---

### Q11.
**When debugging a Bash script, what command would you use to stop the execution of the program until the Enter key is pressed?**
### *Answer:*
```
read
```
---

### Q12.
**How to get the first line from a file using just the terminal?**
### *Answer:*
```Bash
# head -1 /var/log/boot.log-20190716
[  OK  ] Started Show Plymouth Boot Screen.
```
---

### Q13.
**How to get the 3rd element/column from each line from a file?**
### *Answer:*
```Bash
# cat test.sh
#!/usr/bin/env bash
cat > test.txt <<EOF
col11 col12 col13 col14 col15
col21 col22 col23 col24 col25
col31 col32 col33 col34 col35
EOF

awk '{print $3}' ${1}

# ./test.sh test.txt
col13
col23
col33
```
---

### Q14.
**How to redirect both standard output and standard error to the same location?**
### *Answer:*
The two methods to redirect standard output and standard error to the same location are the following;
```Bash
    2>&1(# ls /usr/share/doc > out.txt 2>&1 )
    &>(# ls /usr/share/doc &> out.txt )
```
---

### Q15.
**What differentiate between ‘ and ” quotes?**
### *Answer:*
  +  **Single Quotes: Used in case evaluation of variables to values is undesired.**
  +  **Double Quotes: Used in case evaluation of variables to values is required.**
---

### Q16.
**What is the difference between $* and $@?**
### *Answer:*
$@ treats each quoted arguments as separate arguments but $* will consider the entire set of positional parameters as a single string

---

### Q17.
**Write down the Syntax for all the loops in Shell Scripting.**
### *Answer:*
For Loop:
```Bash
for var in word1 word2 ... wordN
do
   Statement(s) to be executed for every word.
done
```
While Loop:
```Bash
while command
do
   Statement(s) to be executed if command is true
done
```
Until Loop:
```Bash
until command
do
   Statement(s) to be executed until command is true
done
```
---

### Q18.
**When should shell programming/scripting not be used?**
### *Answer:*
It is not advisable to use Shell scripting in the following cases;

  +  **When the task is very much complex, e.g. writing the entire payroll processing system.**
  +  **Where there is a high degree of productivity required.**
  +  **When it needs or involves different software tools.**
---

### Q19.
**What are the default permissions of a file when it is created?**
### *Answer:*
On Linux and other Unix-like operating systems, new files are created with a default set of permissions. The umask or user mask command is used to determine the default permissions for newly created files. It is a 4-digit Octal number which is set and expressed using symbolic values. The default permission of a file when it is created is **664** i.e. **rw-rw-r-**. The table for file permissions is given below;

|  0    |   0   |  No permissions       |
| :--- | :--- | :--- |
| 1     | 1      | execute      |
| 2     | 2     | write     |
| 3     | 1+2     | execute + write     |
| 4     | 4     | read     |
| 5     | 1+4    | execute + read     |
| 6     | 2+4     | write + read      |
| 7     | 1+2+4     | execute + write + read     |

---

### Q20.
**Determine the output of the following command:
$ name=Bob && echo 'My name is ${name}'**
### *Answer:*
```Bash
$ name=Bob && echo 'My name is ${name}'
My name is ${name}
```
---

### Q21.
**Determine the output of the following command:
$ [ -z "" ] && echo true || echo false**
### *Answer:*
```Bash
$ [ -z "" ] && echo true || echo false
true
```
---

### Q22.
**Determine the output of the following command:
$ echo ${new:-variable}**
### *Answer:*
```Bash
$ echo ${new:-variable}
variable
```
---

### Q23.
**How booleans are used in a shell script?**
### *Answer:*
In bash, true is 0 and false is any value but 0. There exist two commands, true and false that deliver true or false, respectively:
```Bash
$ true; echo $?
0

$ false; echo $?
1
```
```Bash
#!/usr/bin/env bash
#bool.sh
bool=true
if ($bool);then
    echo true
fi
bool=false
if !($bool);then
    echo false
fi

$ ./bool.sh
true
false

```
---

### Q24.
**How to get part of string variable with echo command only?**
### *Answer:*
To extract substrings in a shell script is to use a Bash variable with the substring syntax, just likes python slice.
```Bash
#!/usr/bin/env bash
#echo ${var:x:y}
#x - start position
#y - length

var="My name is Bob, and I work at Oracle."
#From left extract string
echo ${var:11:3} # will display Bob
echo ${var::2} # will display My
echo ${var:19} # will display I work at Oracle.

#From right extract string 
echo ${var:0-7:6} # will display Oracle
echo ${var:0-7} # will display Oracle.
```
---

### Q25.
**How to print all the arguments provided to the script?**
### *Answer:*
```Bash
#!/usr/bin/env bash
for i;do echo $i ;done

# ./test.sh a b c d e f
a
b
c
d
e
f
```
---

### Q26.
**How to print PID of the current shell?**
### *Answer:*
```Bash
#!/usr/bin/env bash
for PID in $$; do
    echo ${PID}
done

# ./test.sh
3950
```
---

### Q27.
**How to print all array elements and their respective indexes?**
### *Answer:*
```Bash
#!/usr/bin/env bash
array=("This" "is" "a" "test")
echo "Array elements:${array[@]}"
echo "Array element index:${!array[@]}"

# ./test.sh
Array elements:This is a test
Array element index:0 1 2 3
```
---

### Q28.
**How to print the first array element?**
### *Answer:*
```Bash
#!/usr/bin/env bash    
array=("This" "is" "Shell" "Scripting" )    
echo "First element:${array[0]}"    
echo "All elements:${array[@]}"

$ ./test.sh
First element:This
All elements:This is Shell Scripting
```
---

### Q29.
**How many fields are present in a crontab file and what does each field specify?**
### *Answer:*
The crontab file has six fields.
The first five fields contain information on when to execute the command and they are as follows;

  +  minute(0-59)
  +  hour(0-23)
  +  day(1-31)
  +  month(1-12)
  +  day of the week(0-6, Sunday = 0).
  
The sixth field contains the command to be executed.

---

### Q30.
**How to debug the problems encountered in the shell script/program?**
### *Answer:*
Given below are some common methods used to debug the problems in the script.

  +  Debug statements can be inserted in the shell script to output/display the information which helps to identify the problem.
  +  Using set -x we can enable debugging in the script.
---

### Q31.
**How to declare a readlone variable?**
### *Answer:*
```Bash
#!/usr/bin/env bash    
declare -r var1=1
echo "var1 = $var1"   # var1 = 1
(( var1++ ))          # x.sh: line 4: var1: readonly variable
```
---

### Q32.
**How to declare a readlone variable?**
### *Answer:*
There are three different commands available to check the disk usage.
  +  **df: It is used to check the free disk space.**
  +  **du: It is used to check the directory wise disk usage.**
  +  **dfspace: It is used to check the free disk space in terms of MB.**
 ---

### Q33.
**What is the commands to check a directory space usage?**
### *Answer:*
```Bash
[ke@ke-linux ~]$ du -s ~ -m
1501    /home/ke
```
---

### Q34.
**How to open a read-only file in the Shell?**
### *Answer:*
A read-only file can be opened using the below command:
```diff
#vi –R <File Name> 
```
---

### Q35.
**Write a shell script to get current date, time, user name, file name and working directory.**
### *Answer:*
```Bash
#!/usr/bin/env bash
echo "Hello, $LOGNAME"
echo "Today's date is `date`"
echo "Username is `who i am`"
echo "Current file name is $0"
echo "Current directory is `pwd`"

$ ./test.sh
Hello, ke
Today's date is 2019年 10月 26日 星期六 19:46:46 CST
Username is ke       pts/0        2019-10-26 19:41 (10.0.2.2)
Current file name is ./test.sh
Current directory is /home/ke
```
---

### Q36.
**How to find all the files modified in less than 7 days?**
### *Answer:*
```Bash
$ find . -type f -mtime -7 -exec ls -l {} \;
```
---

### Q37.
**Print a given number, in reverse order using a Shell script such that the input is provided using command Line Argument only.**
### *Answer:*
```Bash
#!/usr/bin/env bash
Usage(){
    echo "Usage: $0 number"
    echo " Reverse of the given number will be printed"
    echo " For eg. $0 0123, 3210 will be printed"
    exit 1
}

[ $# -ne 1  ] && Usage

n=$1
rev=0
sd=0

while [ $n -gt 0  ]
do
    sd=$(( n % 10 ))
    rev=$(( rev * 10 + sd ))
    n=$(( n / 10 ))
done
echo "Reverse results:$rev"

[ke@ke-linux ~]$ ./test.sh 12345
Reverse results:54321

[ke@ke-linux ~]$ ./test.sh 123456789
Reverse results:987654321
```
---

### Q38.
**How to calculate a real number calculation in shell script?**
### *Answer:*
```Bash
$  echo "1.6+2.5" | bc
4.1

$  echo "1.6*2.5" | bc
4.0

$ echo "scale=3;3/2" | bc
1.500

$  echo "scale=2;1.6^2" | bc
2.56

$  echo "scale=2;sqrt(2.56)" | bc
1.60
```
---

### Q39.
**How to get the value of pi till a 20 decimal places?**
### *Answer:*
```Bash
$ echo -n "π=";echo "scale=20; 4*a(1)" | bc -l
π=3.14159265358979323844
```
---

### Q40.
**Write a script to print the first 10 elements of Fibonacci series.**
### *Answer:*
```Bash
#!/usr/bin/env bash
for i in {1..10}; do
    if [[ ${i} -eq 1 || ${i} -eq 2 ]]; then
	a=1
	b=1
	echo 1
    else
	c=$b
        b=$((a + b))
	a=$c
	echo $b
    fi
done

$ ./test.sh 
1
1
2
3
5
8
13
21
34
55

```
---

### Q41.
**What is the difference between $$ and $!?**
### *Answer:*
$$ gives the process id of the currently executing process whereas $! Shows the process id of the process that recently went into the background.

--- 

### Q42.
**What are zombie processes?**
### *Answer:*
These are the processes which have died but whose exit status is still not picked by the parent process. These processes even if not functional still have its process id entry in the process table. 

---

### Q43.
**Print the 10th line without using tail and head command.**
### *Answer:*
```Bash
#!/usr/bin/env bash
sed –n '10p' file1
```
---

### Q44.
**How will you find the total disk space used by a specific user?**
### *Answer:*
```Bash
#!/usr/bin/env bash
du -s /home/<user home path>
```
---

### Q45.
**Find all the files modified in less than 2 days and print the record count of each.**
### *Answer:*
```Bash
# find . –mtime -2 –exec wc –l {} \; 
```
---
