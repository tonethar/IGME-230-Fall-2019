# Week 4B - More CSS

- Any questions about [Project 1](../projects/project-1.md)?
  - Reminder: Subject of tutorial is due today at 5:30
  - let's take a look at what our friends have posted to the discussion thread
- *LWD* Chapter 12 - *Formatting Text*
  - Font-related properties
  - Text line settings
  - Various text effects
  - List style properties
  - ID, class, and descendent selectors

## II. Demo
- increase `font-size` `rem` on `<body>` using CSS
  - demo this using JavaScript
- Selectors - we've already seen *type*, *class*, *id*, *universal*, and *grouped* selectors - here are some *contextual* selectors:
  - *descendant* selector (ex. kids, grandkids, great grandkids, ...)
    - `h1 em {color: red;}`
  - *child* selector (ex. just the kids)
    - `p > em {font-weight: bold;}`
  - *next-sibling* selector (ex. the next sibling element in the HTML source)
    - `h1 + p {font-style: italic;}`
  - *subsequent-sibling* selector (ex. 
    - `h1 ~ h2 {font-weight: normal;}`
- Specificity - more *specific* selectors have more weight: 
  - *Inline* styles with the `style` attribute are more specific than
  - *ID* selectors, which are more specific than
  - *Class* selectors, which are more specific than
  - *Element* selectors


## III. Homework Assignment

- [Holmes Part I](https://github.com/tonethar/IGME-235-Shared/blob/master/notes/holmes-part-1.md) & [Holmes Part II](https://github.com/tonethar/IGME-235-Shared/blob/master/notes/holmes-part-2.md)
 
## IV. Reference
- https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Selectors
- https://drafts.csswg.org/selectors-3/

## V. Other Relevant Resources
- [Marx](https://mblode.github.io/marx/) - Here's a possible stylesheet that you could add to your site that will improve the styling and general look of things simply by downloading it, adding it to your site structure, and linking to it as an external style sheet.
- [Bootstrap "Reboot"](https://getbootstrap.com/docs/4.3/content/reboot/) - A similar concept.  Not the full Bootstrap framework, but rather a CSS file to give (in their words) "an elegant, consistent, and simple baseline to build upon".

<hr><hr>

| <-- Previous Unit | Home | Next Unit -->
| --- | --- | --- 
| [**week-04A-notes.md**](week-04A-notes.md)     |  [**IGME-230 Schedule**](../schedule.md) | [**week-05A-notes.md**](week-05A-notes.md)

