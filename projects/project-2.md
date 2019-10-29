# Project 2 - Web Service Application - DRAFT

## I. Overview

For this project you and a partner) are creating a single-page JavaScript driven Web application that utilizes a Web service.
- Your goal is to create an application that is easy to use, functional, and aesthetically pleasing.
- Ideally the experience will run in all modern browsers, but at a bare minimum it must run in recent versions of Chrome.
- The objective of this project is for you to demonstrate your mastery of HTML5/CSS/JS programming in a [web browser DOM](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model/Introduction) context. 
- You will be evaluated on:
    - your creativity
    - the quality of the experience you create
    - the soundness of your programming
    - how far you went beyond what we did in class, as described below
    
- Resources:
    - Our entire Web apps series: [Web Apps 0 - About this Web App Tutorial Series](https://github.com/tonethar/IGME-230-Master/blob/master/notes/web-apps-0.md)
   - This HW pulls together most of what you need to know into a working example -> [GIF Finder HW](https://github.com/tonethar/IGME-230-Master/blob/master/notes/HW-gif-finder.md) 
   - Here are some working web service examples for you to look at - you can use any of these APIs in your project except for GIPHY: [web-service-app-starters.md](https://github.com/tonethar/IGME-230-Master/blob/master/notes/web-service-app-starters.md)
   - https://developer.mozilla.org/en-US/docs/Web/JavaScript

## II. Requirements

### A. Functional
1. Your application will utilize a web service from this list:
    - https://github.com/toddmotto/public-apis
        - try to use an API that supports *CORS* (Cross-origin resource sharing) - if the API says **NO** in the **CORS** column then it will definitely **NOT work** for this project
        - **DO NOT** use any API that requires *OAuth* authentication
        - if an API requires an API Key, be sure that there is a "free tier", and that the API does not have a short trial period
    - You may optionally utilize an API from this list (although these have not been as extensively curated):
      - https://github.com/abhishekbanthia/Public-APIs
    - Finally, these APIs will definitely work, and there is code to get you started (although you are not allowed to use the GIPHY API for this project): [web-service-app-starters.md](https://github.com/tonethar/IGME-230-Master/blob/master/notes/web-service-app-starters.md)
    - Here are the "Blacklisted" APIs that you **MAY NOT** use for this project:
      - Any API from GIPHY - https://developers.giphy.com/docs/
      - The iTunes Search API - https://affiliate.itunes.apple.com/resources/documentation/itunes-store-web-service-search-api/
- **Important note:** Most of the "sports score" APIs have strict rate limits and/or short trial periods. In the past, most students attempting to use these APIs on their projects ended up having to change their project idea to something else at the last minute. Use such APIs at your own risk.

2. You will save the last term searched by the user in the browser local storage - this was covered here: [Web Apps 9 - WebStorage API](https://github.com/tonethar/IGME-230-Master/blob/master/notes/web-apps-9.md):
    - we are going to test this capability by typing in a search term, doing a search, and then closing the browser window. When we re-open the window, the user's last search term should still be in the field.
    - ideally this will also be true of the other controls, but we won't require it.

3. Required controls - there will be a MINIMUM of 3 controls that a user can use to filter and display the results. Search buttons or similar don't count towards the 3 controls. For example, GIF Finder has these controls:
    - a search button (which doesn't count)
    - a search term field (&lt;input>) that the user types into
    - a pulldown (&lt;select>) that the user can use to limit the number of results

  -  **So you will need at least one additional kind of control. What kind of control to use depends on what parameters the web service will allow you to search it on. Here are some ideas:**
  
     - a **rating** pulldown - if we had this on the GIPHY HW then a user would be able to choose between viewing "G" and "PG" videos for example
     - a **sort by** pulldown to allow the user to view the results sorted A->Z, Z->A, by date, etc 
     - a **date** chooser to filter the results by date - jQuery has a Datepicker Widget that would help with this -> https://jqueryui.com/datepicker/
     - **next** and **previous** buttons - another really nice option is to allow the user to "page" through large numbers of results. In the GIPHY HW did you notice that we always get the same 100 "cat" GIFs back when we search?
       - This is because there are ***thousands*** of cat GIFs on GIPHY, and if we don't otherwise specify we will always get them returned from the web service starting at index 0, which means we always get the first 100 (index 0-99) back.
       - We can instead write code that requests a higher starting index.
       - In the GIPHY API this can be done by tracking and adding an `offset` value to the query string that is sent over to the API.

4. Finally, there will be no JavaScript errors or exceptions thrown by the app.

### B. Design & Interaction
1. Pleasing graphic design:
  - with a custom interface coded in HTML/CSS, by you
  - this interface does not resemble the GIPHY homework's UI
2. Widgets are well labeled and follow interface conventions, for example:
  - radio buttons are for mutually exclusive options, checkboxes are for when you want to let the user choose *multiple* options - https://delib.zendesk.com/hc/en-us/articles/203430309-Radio-button-vs-checkbox-what-s-the-difference-
  
3. Users should be able to figure out how to use the app with minimal instruction:
  - be sure to provide instruction and tooltips if necessary
4. User errors must be handled gracefully:
  - for example, if the user forgets to type in a search term before clicking the Search button, the app should tell the user something like "Please enter a search term first"
5. Users must know what *state* the app is in at all times:
  - for example, when they click the search button, there should some indication that a search is happening:
    - text that says "Searching for 'Tacos' near you" and so on
    - a "spinner" or other "indeterminate progress" animation - [Google search "indeterminate progress"](https://www.google.com/search?q=indeterminate+progress&client=safari&rls=en&source=lnms&tbm=isch&sa=X&ved=0ahUKEwj-sNCal4neAhVr34MKHWKqA98Q_AUIDigB&biw=1036&bih=583)
    - here are some "spinner" images you could use (show them when the search starts, and hide them when the search ends): http://ajaxloaders.net/2012/10/spinner-loading-animations-set-1/

### C. HTML
1. Structural tags like `<header>`, `<section>`, `<article>`, `<nav>`, and `<footer>` should be used appropriately.
2. Inline text marked up as appropriate
3. Valid HTML5 - https://validator.w3.org


### D. CSS
1. the CSS 100% done by you - no CSS libraries or templates are allowed on this project
2. CSS selectors and rules will be used for text formatting: 
  - Most of the style rules will be located in an **external style sheet**
  - There will be at least 5 style declarations (rules) in your **external style sheet**
  - Avoid using **inline styles**
3. use a variety of CSS selectors with your project - at a minimum use at least one of each of the following selectors: *class*, *type*, *id*, and *descendant*
4. Valid CSS - https://jigsaw.w3.org/css-validator/

### E. Layout
1. use CSS Grid and/or CSS Flexbox layout (see chapters 16 & 17)
  - you will most likely have a multi-column layout on the desktop version
  - you will most likely have a single-column layout on the mobile version
2. you will need to have distinctive styles for at least 3 screen size "breakpoints":
  - at least one of these breakpoints must target smart phones
  - the distinct styles for the breakpoints must be done for an aesthetic or usability reason, and not merely be done to "meet requirements". For example, changing the background (for no particular reason) from blue to green for the mobile version of your site would NOT meet this requirement
3. be sure to use the "viewport meta tag"

### F. Media
1. **A *custom font*** is utilized for the site - see https://fonts.google.com
2. the dimensions of all image files must be *optimized*:
  - this means they are in the proper format and are no larger than necessary
  - the image files must be saved in a web friendly format and then compressed to save file size
  - jpegs and pngs should be no larger that 50kB (and can often be much smaller)

### G. Code Conventions
- 1. DO NOT use any JavaScript libraries (ex. jQuery) - instead - this code will be 100% created by you
- 2. All JavaScript code is an external JavaScript file
- 3. *inline* (attribute) event handlers are NOT allowed - ex. `<button onclick="doStuff">Click Me!</button>`
- 4. `let` and `const` must be used to declare variables (no `var`!)
- 5. `querySelector()` and `querySelectorAll()` must be used for DOM traversal (DO NOT use the older methods such as `document.getElementsByTagName()` or `document.getElementById()`)
- 6. **D.R.Y. - Don't Repeat Yourself.** Repeated blocks of nearly identical code must be factored out and placed in a separate function.
- 7. Variable and function names must begin with a lowercase letter.
- 8. Well-commented code. Each and every function gets a comment indicating what it does.
- 9. Delete or comment out any `console.log()` calls.

## III. Milestones
- Project proposal with mockup - see myCourses for due date/time. One submission per team please. Make sure both team members' names are included.
- Final project deliverable - see myCourses for due date/time. One submission per team please. Again, make sure both team members' names are included.

## IV. Documentation
- In your myCourses submission, include documentation (as a PDF file) where you document your process, cite any sources (tutorials, images, code fragments, etc), tell me where to find anything special you want me to see, and also explain how you met the requirements
- Detail what each team member did
- Finally, give yourselves a grade for the project that you feel fairly represents what its worth.


## V. Grading
- *Both* partners must contribute *both* JavaScript code AND HTML/CSS to the project. This is NOT a project where team members are allowed to specialize into "Art Director" and "Software Developer" roles! Both team members shall be "Artist/Coders" (doing both) for this project.

Your project will be graded on the following criteria:  
(note:  This rubric is subject to change prior to 3/30/2019, after that date, it will no longer change)

| Criteria | Weight | Your Score |
| -------- | ------ | ---------- |
| **Functionality** | **40** | |
|  - Is useful and/or entertaining | |
|  - Demonstrates creativity | |
|  - Runs without errors | |
|  - *Does not remember last search term* | *(-10)* |
|  - *Missing controls* | *(-15 each)* |
| **Design & Interaction** | **20** | |
|  - Visual design is pleasing | |
|  - Interface is clear and well labeled | |
|  - Standard interface conventions followed | |
|  - The *state* the application is in is obvious | |
|  - Prevents and handles errors well | |
|  - *Interface looks like GIF Finder HW* | *(-10)* |
|  - *Interface "broken" at 1024x768 or lower resolutions* | *(-10)* |
| **HTML/CSS/Media**  | **10** | |
|  - HTML and CSS validate | |
|  - CSS is primarily in a single external stylesheet | |
|  - Makes proper use of structural tags, etc. | |
|  - *Image dimensions and/or file size unnecessarily large* | *(-5)* |
| **Code**  | **10** | |
|  - Code is well formatted and commented | |
|  - Code is located in an external JavaScript file | |
|  - Code follows coding standards detailed above | |
| **Documentation** | **10** | |
| **Above and Beyond (see below)** | **10** | |
| **Possible Total Points** | **100** | |
| Deduction if proposal is not submitted to dropbox on time | -10 | |

Note:
- **Good** (Meet all requirements above reasonably well) = 90%
- **Better** (Go beyond expectations in 2 or more areas) = 95%
- **Best** (Go significantly beyond expectations in 2 or more areas) = 100%

## VI. Submission
- ZIP and post the completed project and documentation page to to the mycourses dropbox
- Post the project to Banjo and link it from your 230 home page

<hr><hr>

**[Table of Contents <- About this Web App Tutorial Series](../notes/web-apps-0.md)**
