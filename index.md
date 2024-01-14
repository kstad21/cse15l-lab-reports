# Katy's CSE15L Lab Reports
## Lab 1
### Example of the `cd` command: 
---
![cd command with NO arguments](cdnoArg.jpg)
- Working directory: `home`
- When `cd` is used with no arguments (meaning there's nothing after `cd` in the prompt), the user is returned to their home directory. Lack of output isn't an error, since we're changing directories without having to print any output. So when I write the command `pwd`, which prints our working directory, we're shown the path `/home`.

---

![cd command with DIR argument](cdDirArg.jpg)
- Working directory: `home`
- When we use `cd` with an argument that matches one of our directories, we move into that directory. Again, there's nothing printed after the command executes, but we can see that the prompt has changed on the next line to show that we are now in `lecture1`. Again, when I use `pwd`, `/home/lecture1` prints, showing us that we have moved into `lecture1`.
  
---

![cd command with FILE argument](cdFileArg.jpg)
- Working directory: `lecture1`
- When we use `cd` with an argument that matches one of our files or a path to one of our files, we see an error message: `messages/en-us.txt: Not a directory`. This is because the `cd` command is meant for the user to navigate through directories, and it's impossible to "navigate through" a file. 

---
### Example of the `ls` command:
---
![ls command with NO arguments](lsNoArg.jpg)
- Working directory: `lecture1`
- When I type in `ls` with no arguments, that means the files in our current working directory will be listed as output. Indeed, we can see 4 files and/or directories listed, separated by spaces. `messages` is bold and in blue, which is Edstem's way of distinguishing a directory.
  
---
![ls command with DIR argument](lsDirArg.jpg)
- Working directory: `home`
- Typing `ls` with a argument matching a directory/path to a directory results in the files in that directory being printed. In the example above, I provided `lecture1/messages`, which was the path (relative to my working directory, home) to the directory `messages`. Output was as expected: 4 language files are listed.

---
![ls command with FILE argument](lsFileArg.jpg)
---
### Example of the `cat` command:
---
![cat command with NO arguments](catNoArg.jpg)
---
![cat command with DIR argument](catDirArg.jpg)
---
![cat command with FILE argument](catFileArg.jpg)
---




