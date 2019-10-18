# Shell interview Q&A

The purpose of this documentation is to document common interview questions and answers about Linux shell script.

## Q&A

* [Q1: What is Shell?](#Q1)
* [Q2: What is a Shell Script? Can you name some of its advantages?](#Q2)
* [Q3: What are the different types of variables used in Shell Script?](#Q3)
* [Q4: How do you create a shortcut in Linux?](#Q4)
* [Q5: What are the various stages of a Linux process it passes through?](#Q5)
* [Q6: What are the different types of variables used in Shell Script?](#Q6)
* [Q7: What are the different types of variables used in Shell Script?](#Q7)
* [Q8: What are the different types of variables used in Shell Script?](#Q8)
* [Q9: What are the different types of variables used in Shell Script?](#Q9)
* [Q10: What are the different types of variables used in Shell Script?](#Q10)
* [Q11: When debugging a Bash script, what command would you use to stop the execution of the program until the Enter key is pressed?](#Q11)

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

### Q11.
**When debugging a Bash script, what command would you use to stop the execution of the program until the Enter key is pressed?**
### *Answer:*
```
read
```
---
