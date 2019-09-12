# Week 3B - More HTML

## I. Topics & Overview
- [Project 1](../projects/project-1.md) requirements posted:
  - there is a myCourses discussion thread to post your idea
- *Learning Web Design* chapters 11-14 have been assigned:
  - there are active "Study Quizzes" in mycourses for you to take
  - the quizzes can be taken as many times as you want - and they are all open for at least a week
  - **IMPORTANT**: These are open book,  but you need to work **SOLO** on them, and without any outside help. Making these quizzes a group effort or just giving the answers to a friend will end up hurting people in the near term because they won't know the material
- Review of `.htaccess` Authentication
  - see this link for more options: https://www.rit.edu/webdev/people/htaccess
- Semantic markup demo - see **Section II** below
- Finish LWD Chapter 5 - *Marking Up Text* slides
- LWD Chapter 6 - *Adding Links*
  - The `a` element
  - External links with absolute URLs
  - Links with relative pathnames
  - Linking within a page (fragments)
  - Targeting browser windows
  - Mail links
- Project 1 questions / work on HW

## II. Semantic Markup Demo

**unix-not-so-semantic.html**

- what elements should have been used instead?

```html
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="utf-8" />
	<title>Unix and Web Practice</title>
</head>
   <body>
	<h1>Unix and Web Practice</h1>

	<h2>-a</h2>
	<p>Show all</p>
	<h2>-ls</h2>
	<p>list</p>
	<h2>ls -al</h2>
	<p>Print all the lists in detail</p>
	<h2>man</h2>
	<p>Command help</p>
	<h2>cd</h2>
	<p>Move directory: cd/adc -> Move from root directory to abc directory</p>
	<h2>pwd</h2>
	<p>Check current directory path</p>
	<h2>mkdir</h2>
	<p>Create new directory: mkdir /test1/test11 -> Create test11 folder in test1 folder</p>
	<h2>rmdir</h2>
	<p>Delete directory (No files in directory when deleting) </p>
	<h2>rm</h2>
	<p>Delete file or directory</p>
	<h2>mv</h2>
	<p>Rename and move file</p>
	<h2>touch</h2>
	<p>Create file of capacity 0</p>
	<h2>cat</h2>
	<p>Output text file</p>
	<h2>chmod</h2>
	<p>Change file mode / characteristics / permissions</p>
	<h2>nano</h2>
	<p>edit</p>
	<h2>cp</h2>
	<p>copy</p>
	<h2>wc</h2>
	<p>Count lines, words, bytes, and characters</p>
	<h2>echo</h2>
	<p>Write arguments to standard output</p>
	<h2>cal</h2>
	<p>Output the calendar</p>
	<h2>*</h2>
	<p>ALL</p>
	<h2>?</h2>
	<p>Any letter(count as one)</p>
	<h2>/</h2>
	<p>cd / : go home</p>
	<h2>..</h2>
	<p>Go upper level (parent)</p>

   </body>
</html>
```

**unix-semantic.html**

- better - which elements were used instead?
- but there's still an issue, can you see it?
- let's style the page a little too

```html
<!DOCTYPE html>
<html lang="en" xmlns="http://www.w3.org/1999/xhtml">
<head>
    <meta charset="utf-8" />
    <title>Unix Commands</title>
</head>
<body>
<h1>Unix Commands for Dummies</h1>

<h2>Basic Commands</h2>
<dl>
<dt><b>pwd</b></dt>
<dd> This command tells you where you are in the unix directory</dd>
<dt><b>man commandName</b></dt>
<dd>This command shows the manual for any command ux command you need</dd>
<dt><b>cp file1 file2</b></dt>
<dd>copies a file and gives the copy a new file name</dd>
<dt><b>mv file1 file2</b></dt>
<dd>moves a file into a different directory and changes the name</dd>
</dl>

<h2>List Commands</h2>
<dl>
<dt><b>ls</b></dt>
<dd>list the files in the current directory</dd>
<dt><b>ls -l</b></dt>
<dd>list a long version of your files. includes who owns the files and who is allowed to see and modify it</dd>
<dt><b>ls -la</b></dt>
<dd>list all the files from the root</dd>
</dl>

<h2>Directory Commands</h2>
<dl>
<dt><b>mkdir folder1</b></dt>
<dd>makes a new directory and names it</dd>
<dt><b>cd folder</b></dt>
<dd>moves you from the directory you are currently in into the specified folder</dd>
<dt><b>cd ..</b></dt>
<dd>moves you to the parent directory of whatever file you're in</dd>
<dt><b>cd/</b></dt>
<dd>moves you to the root directory</dd>
<dt><b>cd</b></dt>
<dd>puts you in the directory that you were in when you booted up Unix, known as the "login" directory</dd>
</dl>

<h2> Permissions Commands</h2>
<dl>
<dt><b>chmod 755 folder1</b></dt>
<dd>chmod changes the permissions of any folder or directory. 755 means the creator can read, write, and execute, but the group and anyone else can only read and execute </dd>
<dt><b>chmod 644 file1</b></dt>
<dd> changes permissions so the owner can read and write in the file, while the group and anyone else can only read</dd>
<dt><b>chmod 700 folder1</b></dt>
<dd>changes the permissions so only the owner has full control of the directory</dd>
</dl>

<h2> Deletion Commands</h2>
<dl>
<dt><b>rmdir folder1</b></dt>
<dd>deletes the specified directory along with anything else that's in it</dd>
<dt><b>rm file1</b></dt>
<dd>deletes any file in the directory</dd>
<dt><b>rm proj?.html</b></dt>
<dd>deletes any file that is named proj?.html with the ? representing any single character</dd>
<dt><b>rm*</b></dt>
<dd>deletes everything on your computer</dd>
</dl>

<h2>Calander Commands</h2>
<dl>
<dt><b>cal</b></dt>
<dd>displays the a calander of the current month</dd>
<dt><b>cal 5 2016</b></dt>
<dd>uses the calander to display may 2016</dd>
</dl>

<h2>Content Commands</h2>
<dl>
<dt><b>cat file1</b></dt>
<dd>reads the contents of the specified file</dd>
<dt><b>cat file1 file2 >> file3</b></dt>
<dd>add or "appends" the contents of file1 and file2 to the end of file3</dd>
<dt><b>echo "goop" >> file3</b></dt>
<dd>echo returns whatever was stated when declared. In this case it will append goop to file3</dd>
<dt><b>nano file1.txt</b></dt>
<dd>nano is a file editor that can be used to open and edit files. using nano would open the file stated(in this case file1.txt)</dd>
</dl>

<h2>Network Commands</h2>
<dl>
<dt><b>telnet towelblinkenlights.nl</b></dt>
<dd>telnet is a command used to connect to a server in order to communicate with host in another server(in this case towelblinkenlights.nl)</dd>
<dt><b>w</b></dt>
<dd>this command tells who is in your network and what they are doing in it.</dd>
<dt><b>finger userName</b></dt>
<dd>finger gives you information on the user connected to your network including when they last came on and the last email they read</dd>
<dt><b>wc -l < file </b></dt>
<dd>prints out the line count in a file</dd>
<dt><b>wc -w < file</b></dt>
<dd>prints out the word count in a file</dd>
<dt><b>wc -c < file</b></dt>
<dd>prints out the byte count in a file</dd>
<dt><b>write userName</b></dt>
<dd>let's you send a message to a person in your network</dd>
</dl>
</body>
</html>
```
<hr><hr>

| <-- Previous Unit | Home | Next Unit -->
| --- | --- | --- 
| [**week-03A-notes.md**](week-03A-notes.md)     |  [**IGME-230 Schedule**](../schedule.md) | [**week-04A-notes.md**](week-04A-notes.md)
