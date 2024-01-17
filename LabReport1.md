**Lab Report 1 - Remote Access and File System**

---

**`cd`**

> *No arguments* 

Command: `cd`

Output: Sets prompt to `[user@sahara ~]$`

Working directory: The working directory is the `home`.

Explanation: With no arguments, the working directory defaults to `home`.

> *Directory as an argument*

Command: `cd lecture1`

Output: Sets prompt to `[user@sahara ~/lecture1]$`

Working directory: The working directory is `home`.

Explanation: The `lecture1` folder is a directory and was set to be the working directory.

> *File as an argument*

Command: `cd Hello.java`

Output:  `bash: cd: Hello.java: No such file or directory`

Working directory: The working directory is `home`.

Explanation: `Hello.java is a file`, which cannot be set to be a directory. 

---

**`ls`**

> *No arguments* 

Command: `ls`

Output: `lecture1`

Working directory: The working directory is `home`.

Explanation: This command lists the files in the workspace, which contains only the 'lecture1' directory. 

> *Directory as an argument*

Command: `ls lecture1`

Output: `Hello.class  Hello.java  messages  README`

Working directory: The working directory is `lecture1`.

Explanation: This command lists the files in the `lecture1` directory.

> *File as an argument*

Command: `ls Hello.java`

Output: `ls: cannot access Hello.java: No such file or directory`

Working directory: The working directory is the `Hello.java` file.

Explanation: A file cannot be used as a directory, so the error is given.

---

**`cat`**

> *No arguments:* 

Command: `cat`

Output: No output

Working directory: `/home`

Explanation: `cat` is used to display what is in a file. With no argument, there is nothing to display. 

> *Directory as an argument*

Command: `cat /home/lecture1/messages`

Output: `cat: /home/lecture1/messages: Is a directory`

Working directory: `messages`

Explanation: The error is given because `cat` displays what is inside a file, not what is in an entire directory.

> *File as an argument*

Command: `cat /home/lecture1/messages/el.txt`

Output: `Γειά σου Κόσμε!`

Working directory: `messages`

Explanation: The `cat` command displays the text in the el.txt file.








