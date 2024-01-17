**Lab Report 1 - Remote Access and File System**

---

**`cd`**

> *No arguments* 

Command: `cd`

Output: Sets prompt to `[user@sahara ~]$`

Working directory: The working directory was the entire workspace.

Explanation: The output set the prompt to the default. With no arguments, the working directory defaults to the entire workspace.

> *Directory as an argument*

Command: `cd lecture1`

Output: Sets prompt to `[user@sahara ~/lecture1]$`

Working directory: The working directory is the entire workspace.

Explanation: The `lecture1` folder is a directory and was set to be the working directory.

> *File as an argument*

Command: `cd Hello.java`

Output:  `bash: cd: Hello.java: No such file or directory`

Working directory: The working directory was the entire workspace.

Explanation: `Hello.java is a file`, which cannot be set to be a directory. 

---

**`ls`**

> *No arguments* 

Command: `ls`

Output: `lecture1`

Working directory: The working directory is the entire workspace.

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

Command:

Output: 

Working directory:

Explanation:

> *Directory as an argument*

Command:

Output:

Working directory:

Explanation:

> *File as an argument*

Command:

Output:  

Working directory: 

Explanation:








