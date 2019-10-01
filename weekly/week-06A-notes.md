# Week 6A - Media Queries

## I. Overview
- Today we'll finish up LWD Chapter 14 ("Thinking Inside the Box")
- And get started on media queries

## II. The CSS Box Model

- **We've already utilized much of the below in the "Holmes" exercise, but let's go ahead and make sure that we've hit all of the core concepts:**
  - Every element in a document (both block-level and inline) generates a rectangular element box
    - The amount of space taken up by an element includes the *content area*, plus the total amount of padding, borders, and margins applied to the element
    - the `width` and `height` of a block element are calculated automatically by the browser (the default `auto` value)
    - the box will be as wide as the browser window or other containing block element, and as tall as necessary to fit the content
    - you can use the `width` and `height` properties to explicitly set the element to a specific width or height
  - There are two ways to specify the size of an element:
    - `box-sizing: content-box` is the default method - it applies the `width` and `height` values to the *content box*. That means that the resulting size of the element will be the dimensions you specify plus the amount of padding and borders that have been added to the element. 
    - `box-sizing: border-box` is the other method - it applies the `width` and `height` values to the *border box*, which includes the content, padding, and border. *With this method, the resulting visible element box, including padding and borders (but not margins), will be exactly the dimensions you specify.*
  - `height` of a box - if an element is sized too small for its contents, you can specify what to do with the content that doesn’t fit by using the `overflow` property:
    - possible values are `visible`,  `hidden`, `scroll` or `auto`
  - `padding` is space between the content area and the border 
  - `border` is drawn around the content area and the padding
  - `margin` is space added on the outside of the border
    - margins of adjacent elements (top and bottom) "collapse"
  - `display` - `block`, `inline`, and `none` are the most commonlyn used
  - `box-shadow` 




<hr><hr> 

| <-- Previous Unit | Home | Next Unit -->
| --- | --- | --- 
| [**week-05B-notes.md**](week-05B-notes.md)     |  [**IGME-230 Schedule**](../schedule.md) | [**week-06B-notes.md**](week-06B-notes.md)


