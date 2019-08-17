# Week 3A - Review of HTML

## I. Topics & Overview
- HTML Basics
- Structural and semantic tags
- Paths
- HTML validation

## II. The layers of Web design
1. Content
1. Structure
1. Presentation
1. Behavior

## III. Review and Demo
Together, we'll build a Web page, reviewing the following:
- Basic markup and structure
- Structural and semantic elements
   - Structural markup is using to encode information about the structure of a document. Examples: `<header>, <footer>, <div>, and <span>`. Structural markup such as `<div>` delineates major sections of the document and are also block-level elements that sit on their own line. 
   - Semantic markup means using tags that add meaning to the content. Examples: `<cite>, <quot>, <ul>, <ol>, <em>`. Semantic markup such as `<cite>` adds extra information without altering the structure of a document, and may be either inline or block elements.
- HTML5 structural tags enhance our structure and give us more to work with later on:
   - `<header>, <main>, <nav>, <aside>, <figure>, <footer>`, etc. These are also called *Content Sectioning Elements*.
   - https://www.w3schools.com/html/html5_new_elements.asp
- *Container* tags describe textual content contained within them. Ex: `<p>, <a>, <span>, <div>`
- *Standalone* tags do not have a closing tag that contains text. Ex: `<img>, <link>`
- Both kinds of tags commonly have one or more *attributes* that modify the tag in some way - for example an `<a>' tag needs an `href` attribute with a value, or it's pretty much useless. Ditto for and `<img>` tag without a `src` attribute.
- Tags to know:
   - h1, h2, etc.
   - p
   - a
   - ul, ol, li
   - img
   - comments: `<!-- This is a comment. -->`
- Paths for linking between pages and other resources. 

Here are some examples *relative* paths. When you are linking to other pages and files that are located within your banjo account, you will usually use a relative path:
``` 
<a href="personal-bio.html">Bio Page</a>
<a href="proj/p1/proj1.html">P1</a>
<a href="../../index.html">P1</a>
```

And here are *absolute* paths. When you are linking to other pages and files that are **outside** of your banjo account, you will usually use an absolute path:

```
<a href="http://www.google.com">Go to Google</a>
<img src="http://igm.rit.edu/designcraft/IGM_logo.png" alt="IGM Logo" />
```

Ocassionally you may need use *absolute* paths to files located within your banjo account. This is how to do it:
```
<img id="hypno" src="/~abc1234/230/error/hypnotoad.gif" alt="hypnotoad"/>
```

- Other path tips:
   - Be careful about starting a path with `/` (This goes to the root, usually WAY above your user account)
   - No spaces in path names (use %20) - better yet, don't have spaces in your file names - and use dashes in filenames instead of underscores
   - No special characters (?, !, *, etc.)
   - Avoid caps (case-sensitive)

## IV. Note on using images
- Images should always be integrated into your page at their native resolution. Resizing via HTML or CSS eats bandwidth and leads to long load times. It also uses up unnecessary space on our server.
- See our in-class demo for a refresher on proper image optimization.

## V. HTML Skeleton
This is the bare minimum needed for a valid HTML document:

```
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="utf-8" />
	<title></title>
</head>
<body>

</body>
</html>
```

## VI. Validation
https://validator.w3.org/

## VII. Presentations
- [Welcome to HTML](https://github.com/tonethar/IGME-230-Master/tree/master/presentations/HTML-1.pdf)
- [More About HTML](https://github.com/tonethar/IGME-230-Master/tree/master/presentations/HTML-2.pdf)

## VIII. Demo Files
- [It Was a Dark and Stormy Night](https://github.com/tonethar/IGME-230-Master/tree/master/other-files/stormy-files.zip)

## IX. Reference
- [developer.mozilla.org HTML Element Docs](https://developer.mozilla.org/en-US/docs/Web/HTML/Element) - All the HTML elements grouped by function
- [Lynda.com HTML Essential Training, Lessons 4-5.](https://www.lynda.com/HTML-tutorials/HTML-Essential-Training/170427-2.html?org=rit.edu) - discusses structuring content, and linking to distinct parts of your page.
- [W3Schools](https://www.w3schools.com) - a reference for all things Web (HTML, CSS, JavaScript, etc.)

## X. Exercises
- [Basic Markup/CSS - Recipe](https://github.com/tonethar/IGME-230-Master/blob/master/exercises/week-3/recipe.md) - Note: This exercise covers material from both today and next class. If you want to work ahead, that's fine.
- [230 Home Page](https://github.com/tonethar/IGME-230-Master/tree/master/exercises/week-2/230-home-page.md)

<hr><hr>

| <-- Previous Unit | Home | Next Unit -->
| --- | --- | --- 
| [**week-02-notes.md**](week-02-notes.md)     |  [**IGME-230 Schedule**](../schedule.md) | [**week-03B-notes.md**](week-03B-notes.md)
