# Week 6A - Media Queries

## I. Overview
- Today we'll finish up LWD Chapter 14 - *Thinking Inside the Box*
- And get started on media queries - see LWD Chapter 17 - *Responsive Design*
- ***Reminder: the midterm written exam is on Thursday 10/10/2019 - what's on it?***
  - LWD: Chapters 1-15 - the study guides & study quizzes will give you a good idea of the kind of questions that will be asked
  - everything we did (see notes) from Week 1A to Week 7A
  - be able to write HTML fragments  - ex. "red", "green", and "blue" displayed in an ordered list)
  - be able to write CSS rules - ex. make all text contained in a &lt;div> of `id="advert"` green in color
  - don't forget about the stuff we did at the beginning of the course (the HTTP protocol, .htaccess files, Unix commands, etc)

## II. The CSS Box Model

- Review Chapter 14 Slides - "Thinking Inside the Box"
- **We've already utilized much of this chapter in the "Holmes" exercise, but let's go ahead and make sure that we've hit all of the core concepts:**
  - Every element in a document (both block-level and inline) generates a rectangular element box
    - The amount of space taken up by an element includes the *content area*, plus the total amount of padding, borders, and margins applied to the element
    - the `width:` and `height:` of a block element are calculated automatically by the browser (the default `auto` value)
    - the box will be as wide as the browser window or other containing block element, and as tall as necessary to fit the content
    - you can use the `width:` and `height:` properties to explicitly set the element to a specific width or height
  - There are two ways to specify the size of an element:
    - `box-sizing: content-box` is the default method - it applies the `width` and `height` values to the *content box*. That means that the resulting size of the element will be the dimensions you specify plus the amount of padding and borders that have been added to the element. 
    - `box-sizing: border-box` is the other method - it applies the `width` and `height` values to the *border box*, which includes the content, padding, and border. *With this method, the resulting visible element box, including padding and borders (but not margins), will be exactly the dimensions you specify.*
  - `height:` of a box - if an element is sized too small for its contents, you can specify what to do with the content that doesn’t fit by using the `overflow` property:
    - possible values are `visible`,  `hidden`, `scroll` or `auto`
  - `padding:` is space between the content area and the border 
  - `border:` is drawn around the content area and the padding
  - `margin:` is space added on the outside of the border
    - margins of adjacent elements (top and bottom) "collapse"
  - `display:` - `block`, `inline`, and `none` are the most commonlyn used
  - `box-shadow` 

## III. Demo - Responsive Design with Media Queries

- For Project 1 - we are skipping past LWD chapters 15 & 16 for now - and focusing in on media queries from chapter 17
- Today let's try some of this out in the Holmes HW
- The slides cover this pretty well, so we'll go through those - but here's some HTML & CSS we'll need later:


### III-A. Preview your web page on a mobile browser 

- you can do this by uploading the files to banjo and opening them up on your phone
- or use can use Chrome to simulate a browser
- **once you have loaded the page in you should see that the text is very small, and if you added the text sizing buttons, they are too small to be usable**

### III-B. The viewport &lt;meta> tag

*To fit standard websites onto small screens, mobile browsers render the page on a canvas called the viewport and then shrink that viewport down to fit the width of the screen (device width). For example, on iPhones, mobile Safari sets the viewport width to 980 points so a web page is rendered as though it were on a desktop browser window set to 980 pixels wide. That rendering gets shrunk down to the width of the screen (ranging from 320 to 414 points, depending on the iPhone model), cramming a lot of information into a tiny space.*

*Mobile Safari introduced the viewport &lt;meta> element, which allows us to define the size of that initial viewport.* - LWD Page 487 

**Add this to &lt;head> section**

```html
<meta name="viewport" content="width=device-width, minimum-scale=1.0, maximum-scale=1.0" />
```

- better, but not perfect, let's move on 

### III-C. CSS Media Queries

- Media queries apply different styles based on characteristics of the browser: its width, whether it is vertically or horizontally oriented, its resolution, and so on




<hr><hr> 

| <-- Previous Unit | Home | Next Unit -->
| --- | --- | --- 
| [**week-05B-notes.md**](week-05B-notes.md)     |  [**IGME-230 Schedule**](../schedule.md) | [**week-06B-notes.md**](week-06B-notes.md)


