# Katy's CSE15L Lab Reports

## Lab 2
### I wrote a web server called `ChatServer` that takes in message and user arguments and maintains and displays an ongoing chat between users. I also added a "clear" path so that the user can clear the chat if they'd like to.
---
Here is my code for `ChatServer`. Instead of an error message, I changed that to be a corrective prompt for the user. I also added a corrective message in case the user forgets to use an `&` to separate message and user.

![Lab2 code](Lab2Code.jpg)

###First example of `ChatServer` uainse:
![ChatServer example](ChatServerUse1.jpg)
- Methods called in my code: `main` starts up the server which eventually calls my `handleRequest` method. 
- Relevant args or fields:
  - `chat`, the ongoing `user: message` String. It currently has the value of an empty string.
  - `url `, a URI object containing information about the url in our browser. We can use methods like `getQuery()` and `getPath` to get a String value of the query and path respectively. For reference, `getPath` would yield `/add-message` and getQuery would yield `s=Hello&user=jpolitz`.
- How do these values change from the request?

###Second example of `ChatServer` use:
![ChatServer example](ChatServerUse2.jpg)
- Methods called in my code:
- Relevent args or fields:
- How do these values change from the request?


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
- Working directory: `home`
- `ls` with a file argument results in the file's path, relative to our working directory, being printed. This isn't an error because, though we normally use `ls` to display files within a directory, it's programmed to just output the information it knows about a file if a file is passed in as an argument. In the screenshot above, I give a path to a file and that path is also outputted.

---
### Example of the `cat` command:
---
![cat command with NO arguments](catNoArg1.jpg)
- Working directory: `home`
- If we use the `cat` command with no arguments, it recognizes that there is no file provided for it to read from, and it reads from `stdin` (the "standard input device") instead. Anything I type after entering `cat`, no args, will just be printed again on the next line after I press enter. To exit the loop of typing, entering, and having what you typed outputted, you can press `control + d`, and we return to the normal prompt.
  
---
![cat command with DIR argument](catDirArg.jpg)
- Working directory: `home`
- Using `cat` with a directory argument displays an error message: `cat: lecture1: Is a directory`. There are ways for you to use `cat` to print every file within a directory, but `cat` can't print a directory. The example below shows how `cat` prints the contents of a file.
  
---
![cat command with FILE argument](catFileArg.jpg)
- Working directory: `home`
- Using `cat` with a file path argument outputs the contents of that file without risking changing anything in the file. If we open the file `en-us.txt`, we see the contents "Hello World!", and those contents are correctly printed when we use the command `cat lecture1/messages/en-us.txt`.

---




