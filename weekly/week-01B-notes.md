# Week 1B - How the web works / *banjo.rit.edu* & FTP

## Topics
- I. How the web works
- II. A Simple Web Page
- III. Demo: FTP & Setting up your `230` directory

## I. How the web works
- Follow along with the instructor as we explore the headers sent by browsers and servers.
    - Legacy Notes: [HTTP Protocol Intro](https://github.com/tonethar/IGME-235-Shared/blob/master/notes/http-protocol-intro.md)
    - Demo: [HTTP Protocol Demo](https://github.com/tonethar/IGME-235-Shared/blob/master/notes/http-protocol-demo.md)
    
## II. A Simple Web Page

1) Fire up a text editor such as NotePad++, Visual Studio Code, or Brackets and create and save the following file. NOTE: *Be sure to use **type** "plain text" or "HTML", do NOT create web pages of type "rich text"*

- Note: We will give a quick explanation of what's going on here in class, but LWD chapters 3 & 4 will also walk you through the creation of a simple web page and give additional information

**hello.html**
```
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="utf-8" />
	<title>Hello Page</title>
	<style>
	h1{
	  font-family:sans-serif;
	}
	
	p:first-of-type{
		font-style:italic;
	}
	</style>
</head>
   <body>
      <h1>Week 1 in 230!</h1>
      <p>We will be learning a lot this semester!</p>
      <p>Course GitHub is here: <a href="https://github.com/tonethar/IGME-230-Fall-2019">IGME-230 Fall 2019</a></p>
      <!-- 	This simple page actually has a lot going on in it! -->
      <!-- 	These are HTML comments that is not visible in the browser window -->
   </body>
</html>
```

2) Now open the page up in a web browser, it should look something like this:

![screenshot](_images/hello-page.jpg)



## III. FTP Demo
FTP demo and review (we will do this together in class):
   - Create a local 230 directory, and put you *hello.html* file in it
   - **Reminder:** always keep backups, bring a flash drive to class; the `230` folder on people.rit.edu is where course work will usually be posted


 
1. connect to **`banjo.rit.edu`** with an FTP client - instructions are here: [How to post to RIT's *banjo* web server](https://github.com/tonethar/IGME-230-Master/tree/master/notes/posting-to-banjo.md)
1. create a **`230`** folder and place it in your **`www`** folder
1. post *hello.html* to your banjo **`230`** folder
1. review file/folder permissions to be sure they are correct
1. **Reminder:** **`banjo.rit.edu`** is the FTP name, but the browser will access the URL **`people.rit.edu`**
1. navigate a browser to that directory - **`http://people.rit.edu/~abc1234/230/hello.html`** and you should see your *hello.html* page
1. remember CSS? Let's add some CSS style rules to the page!


<hr><hr>

| <-- Previous Unit | Home | Next Unit -->
| --- | --- | --- 
| [**week-01A-notes.md**](week-01A-notes.md)     |  [**IGME-230 Schedule**](../schedule.md) | [**week-02-notes.md**](week-02-notes.md)
