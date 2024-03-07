---
created: 2023-12-31
status: 🔴
tags:
  - input
  - siat
links: "[[My Inputs]]"
professor: Helmine Serban
semester: Spring 2023
---
## Summary
### Context
- 
### Main Takeaways
- flexbox is god
### Questions/Connections/Thoughts
- 
## Notes
Week 1: Intro to Key Concepts and HTML 

  

Key Pillars of Course:

1. Web is a Fluid Medium
    

-website = structure + styling + content

-fluid for varied devices and users

  

2. Document-Object Model (DOM)
    

-collection of objects that resemble document it is modeling

-use HTML/XML to structure and assemble

  

3. Semantic Markup
    

-reinforce meaning/structure of content with HTML

-letting browser know what content is so it displays properly

  

4. Atomic Design
    

1. atoms: smallest component that makes sense on its own (button, label)
    
2. molecules: combinations of atoms (search bar)
    
3. organisms: combinations of molecules
    
4. templates: reusable parts of pages
    
5. pages: populated with smaller units to convey content
    

  

A Dao of Web Design:

-web started as thoughtless borrowing from print

-in web designer isn’t god

-need to make adaptable pages to each user/device, customizable for each user

-design formed from function of pages

  

Creating Style Guides:

Style Guide/Pattern Library: outlines all elements coded in site/application + visual language

1. foundations (visual structure)
    
2. patterns (basic objects + markup to make them)
    
3. interactivity (animations + java to make them)
    

Allows you to:

-document the design

-test elements across browsers

-avoid duplicates/standardize components

-create common language

-easy teamwork and learning

  

HTML Structure:

|   |   |
|---|---|
|Code|Meaning|
|<!doctype html>|tells browser that it’s HTML code to follow|
|<html lang= “en”>|opens HTML file and tells browser english is default language|
|<head></head>|declare information about the document (no content)|
|<title> Title </title>|set title in browser window|
|<body></body>|where the page content that users see goes|
|<h1></h1> <br><br><h2></h2><br><br><h3></h3><br><br><h4></h4>|heading sizes, hierarchy is used for browser and search engine rankings|
|<p></p>|paragraph text|
|<em></em>|emphasis in inflection|
|<abbr title=“full title”>abbreviation</abbr>|include full title for abbreviation|
|<nav></nav>|major grouping of navigational items and links|
|<a href=“#id”> Title</a>|anchor referencing section in document with id|
|<a href=“url”> Title</a>|anchor referencing external link with url|
|<section id= “name”><br><br></section>|defines section with heading and content, use id to refer to it|
|<figure></figure>|allows relationship of media and caption|
|<img src=“source” alt=“describe image”>|image with alt text for screen readers|
|<figcaption> caption </figcaption>|caption with image|
|<ol></ol>|ordered list (numbered, otherwise list is bulleted)|
|<li> put list element here </li>|list element|
|<code></code>|code piece|
|<br>|line break in code piece|
|<samp></samp>|how code will look on execution|
|<form method= “post” action= “#”>|form has collection of form elements, needs method and action|
|<label for= “id”> name shown</label>|clarifies what form elements are semantically for, associated with form elements using id|
|<input type= “text” id= “form-name” placeholder= “text in form”>|allows variety of inputs within forms, self-closing because no content, one line of text, placeholder is what appears in text box before user interaction|
|<textarea id= “form-comment” placeholder= “placeholder text”></textarea>|allows more than one line of text entry, not self-closing|
|<input type= “submit” value= “submit your comment”>|button with text on it|

  
  

Week 2: Styling the Web

  

Atomic Design Chapter 1: Designing Systems

-pages aren’t independent entities, more about systems that create underlying structure

Modularity: started with car manufacturing, makes it easier to create consistency, relevant to reconfigurable components to suit different users and screen sizes

-redoing everything in website makes users have to relearn it, consistent iteration and upkeep are more sustainable and user-friendly

Pattern-Based Workflow = Modularizing Content:

-making code, visual identity and content of site into reconfigurable chunks

Responsive Web Design:

1. Fluid Grids
    
2. Flexible Media
    
3. CSS Media Queries
    

Frameworks: predone layouts and features

- save time and effort
    

- time/effort modifying them, sameness, bloat from unused aspects
    

Style Guides: cornerstone of good design systems

1. Brand Identity: assets, colours, messaging, collateral
    
2. Design Language: general design philosophy and approach
    
3. Voice/Tone: levels seriousness suiting different aspects of site/brand
    
4. Writing: for consistent written content
    
5. Code: creating code conventions and context)
    

Pattern Library: creates consistency and cohesion, needs context and methodology

-shared vocabulary/naming conventions

-education, demonstrating intent

-easy testing by separating components

-faster development

  

Styling the Web:

  

HTML: semantic focused

  

|   |   |
|---|---|
|<section>|title + content that makes sense on its own|
|<nav>|groups navigational links|
|<article>|like section but groups page section that can be individually distributed|
|<header> <footer>||

  
  

False Assumptions: everyone has:

- high-speed internet, fast computer
    
- mouse and/or touchscreen
    
- 1 pixel = 1 pixel
    

Software Pixel/CSS Pixel: unit of measurement

Hardware Pixel: dot of light onscreen

- will view on IE6 (certain browser), (test on many browsers)
    

  

Goal: user engagement

- fulfilling a need is priority
    
- less than 10 seconds to convince to stay on site
    

Offerings:

- Content (pages: text, images, video, audio)
    
- Structure (templates: layout, grid, hierarchy)
    
- Accessibility (clean markup, flexibility across devices)
    
- Usability (interaction, utility, ux)
    

  

Language Interaction: keep them separate for easy changing

1. HTML (.html): structure and meaning of content
    
2. CSS (.css): presentation and appearance of content
    
3. JavaScript: interactivity
    

- no HTML to define styling
    
- no CSS inline styling
    

  

CSS: Cascading Style Sheets

- stylesheet language not markup language
    
- applied from external style sheet ending in .css extension
    

  

|   |   |
|---|---|
|<link rel= “stylesheet” href= “styles.css”>|Link stylesheet to HTML document in <head> with relationship tag|

  

Syntax:

1. Selector: element to style (can use HTML tag)
    

- purpose-oriented naming convention
    

2. Declaration Block: styling to apply
    

  

|   |   |
|---|---|
|body{<br><br>background: lightblue;<br><br>}|Make body section background light blue|

  

Selector:

1. Type Selector: using HTML element name
    

  

|   |   |
|---|---|
|h2{<br><br>color: yellow;<br><br>}|all h2s are yellow|

  

2. Class Selector: self-defined value able to be used multiple times
    

  

|   |   |
|---|---|
|<p class= “highlighted”> Paragraph content </p><br><br>  <br><br>.highlighted{<br><br>background: yellow;<br><br>}|In HTML define class<br><br>  <br><br>In CSS apply style to selected class|

  

3. ID Selector: self-defined value that can only be used once
    

  

|   |   |
|---|---|
|<li id= “list-item”> list content </li><br><br>  <br><br>#list-item{<br><br>colour: brown;<br><br>}|In HTML define unique id<br><br>  <br><br>In CSS apply style to selected class|

  
  

Units:

1. Absolute: not affected by any other factor
    

Pixel: absolute unit

- not the same on all screens
    
- no decimal values (inconsistent handling)
    
- default body text size 16px
    
- headings are larger/smaller depending on h level
    

2. Relative: calculated in relation to parent/ancestor
    

em: relative unit

- 1 em = height of closest parent font size (what it’s embedded in)
    
- used to measure horizontal width initially, from M
    
- if no size declared 1em is 16 px (default browser font)
    
- can use decimals
    

rem: relative unit

- introduced 2011
    
- 1 rem = 1 em
    
- only relative to root element (size specified in HTML tag in head, if not specified takes default 16px)
    

  

HTML Elements:

1. Block Level: block of content (div, p, ul)
    

- same h as content contained in tags
    
- span entire container w
    
- -start on new line, definable size
    

2. Inline: within block of content (em, span, strong)
    

- w/h of content
    
- align to left side-by-side in line
    
- act like text, size dictated by content
    

  

Box Model: size of elements in browser are configured using content boxes

1. Height/Width: size of actual content
    
2. Padding: distance from content to border (still part of element)
    
3. Border: surrounds element
    
4. Margin: space to other elements
    

  

Week 3: 

  

Atomic Design

1. Atoms: basic HTML elements that can’t be broken down any more while retaining their unique function (button, label, input)
    
2. Molecules: atoms forming together as a reusable unit with purpose (label + input = search bar), one single functionality (single functionality principle), design each to be responsive
    
3. Organisms: molecules together into distinct interface sections (header)
    
4. Templates: page level underlying component structure for dynamic content
    

-template needs to adapt to page variability (character count, permissions, account, user actions)

5. Pages: specific instance of a template filled with content
    

Advantages:

- allow to see and test whole/part relationship
    
- not a sequence (do not design each in isolation)
    
- separation of content and structure
    

  

Week 3: Building Blocks (Responsive Design)

  

Adaptive: static states with breakpoints

Responsive: fluid layout that remains continuous between screen sizes

Elements:

1. Relative Units: dimensions are relative to container (no specific value)
    

- percentage-based dimensions or rems
    
- set constraints for fluid sizes 
    

|   |   |
|---|---|
|max-width: 400px;<br><br>  <br>  <br><br>width: 50%;|biggest width (of element applied) is 400px, can be smaller<br><br>  <br><br>making width 50% of screen no matter size|
|min-width: 200px;|smallest width is 200px, can be bigger|

  

2. Fluid Grids:
    

1. Box Model: set values for margin/padding
    
2. Flexbox: fluid container from parent that only impacts direct child
    

- define parent element as container
    
- direct children become flex items
    
- use flexbox properties to control orientation (horizontal or vertical), size (priority), spacing (how to allocate leftover space), alignment (top, bottom, centered)
    

Main/Cross Axis: flex container has flow direction for content inside

1. Rows: horizontal main axis
    
2. Columns: vertical main axis
    
3. Cross Axis: perpendicular to main axis
    

|   |   |
|---|---|
|.container1 {<br><br>display: flex;<br><br>}|set container one as parent flex element|
|flex: 1;<br><br>flex: 3;|setting how many column on page and how many each flex item takes up|
|flex-grow:<br><br>flex-shrink:<br><br>flex-basis;||
|order: 1;<br><br>order 2;|set order of children flex items|
|flex-direction: row; (default)<br><br>flex-direction: row-reverse;<br><br>flex-direction: column;<br><br>flex-direction: column-reverse;|right to left<br><br>left to right<br><br>top down<br><br>bottom up|
|align-items: flex-start<br><br>align-items: flex-end<br><br>align-items: center<br><br>align-items: stretch<br><br>align-items: baseline|align at top<br><br>align at bottom<br><br>align in center<br><br>stretch to fill space<br><br>align at baseline|
|.box1{<br><br>  flex: 1;<br><br>  order: 3;<br><br>}|set child element to last in order of boxes shown|

  

3. Media Queries: tying specific CSS styles to conditions
    

- can be used for screen size or specific devices
    

Media Type: devices that can display HTML documents

1. all (default): all devices
    
2. print: printers
    
3. screen: all screens
    
4. speech: screen reader
    

Media Feature:

|   |   |
|---|---|
|@media (width-min 40px) {<br><br>  body{<br><br>    background-color: blue;<br><br>}<br><br>}|when condition is met (bigger than min) body background changes colour|
|width 400px|only if it is 400px|
|width-min 400px|if it is 400px or larger|
|width-max|if it is 400px or smaller|

Breakpoints: allow layout to change between sizes

  

|   |   |
|---|---|
|@media screen and (max-width 900px){<br><br>  body{<br><br>    background-color: yellow;<br><br>}}|when screen is 900px or less background is yellow|
|@media screen and (max-width 600px){<br><br>  body{<br><br>    background-color: blue;<br><br>}}|when screen is 600px or less background is blue|

  

Week 5: Utility Belt

  

Version Control:

Git: distributed version control system (VCS)

- coordinated work between multiple developers
    
- tracking changes: who/what/when
    
- reverting to previous version at any time
    
- local and remote repositories
    

VCS: tracks changes in text files

  

Git: version history, take/view file snapshots, stage and commit files

GitHub: web-based git repository hosting service

- access control and collaboration features
    

GitKraken: desktop client

- intuitive ui, makes Git easy to learn
    

  

New Repository: folder icon > init > name + give template/location

Toggle hidden files: command + shift + .

.gitignore: *.jpg (don’t want version control to waste time tracking img)

  

UI:

Left: repository list (local/remote)

Middle: commit graph window (as add more graph grows)

Right: workflow

1. WIP: working uncommitted directory (files)
    
2. Staging: where you put files when getting ready to commit
    
3. Commit: backup files, add descriptive title and description (so can search by later)
    

Reverting:

1. not yet committed: discard hunk/discard changes
    
2. committed: revert or commit
    

  

Search:

1. keyword (title/description)
    
2. filename/fuzzy search (command+p): search various actions
    

  

Branching: work on different versions at same time (helpful for multiple developers)

Merging: put work together into a main

  

Push: put it on remote repository (share with others)

Pull: update yours to match remote repository

  

Reading Week 5: Responsible Responsive Design

Responsible Responsive Design:

1. Usability: how UI is presented and responds to user (touch, stylus, mouse and keyboard)
    

1. Breakpoints: based on smallest screen, expand and add breakpoint when looks awkward
    

1. Major: adding columns/changing layout
    
2. Minor: small tweaks (changing font size)
    

- informed by content
    
- single column reading = 45-75 char (best 66)
    
- double column reading = 40-50 char
    

2. Smaller Screens:
    

Progressive Disclosure: showing content on demand instead of all at once

- toggle
    
- off-canvas layout (offscreen until cued by user)
    

3. Designing for Touch:
    

- hover content should be accessible on touch
    
- space around buttons (negative and tappable 44x44px)
    
- use touch and click simultaneously, provide both options (event listeners for both, Tappy.js library)
    

Web-Safe Gestures: tap, 2-finger tap, horizontal drag, horizontal flick (not interfering with native functions of devices)

2. Access: ability for all users to access content (screen readers)
    

- read on all browsers
    
- start with HTML because backward compatible
    
- always do x-ray view, as much in HTML as possible for max semantics
    

3. Sustainability: ability for site to work in present and future browsers
    
4. Performance: speed and efficiency of site (no redundant code, optimized image sizing)
    

  

Week 6: Responsive Web Review

  

Responsive Web Design:

- responds and behaves in fluid manner to different size options
    

1. Why is it responsible? responsible to different user contexts (screen size, internet access/speed, device, ability)
    
2. Designing for usability? applicable to different screen sizes/interaction methods (mouse, touch, screen, screen reader)
    
3. Progressive disclosure? showing content on demand instead of seen/displayed all at once (for smaller screen sizes)
    

Pros:

1. Write code only ONCE for variety of devices (same HTML/CSS, no mobile only site)
    
2. Easy to maintain (if modular)
    
3. Modularity (atomic design and HTML/CSS/Java are separate)
    

  

1. Flexible Grids: respond to small changes in shape/size of viewport using proportions
    

- text containers change shape/size, text reflows
    
- designed in terms of proportions (not percentage or pixel value)
    

Proportions: divide target (content) by context (window size)

- high fidelity mockup can help with this
    
- measure page element and divide by full width of page
    

- when width of browser becomes too small use media queries
    

2. Media Queries: respond to large changes in size using conditional CSS
    

- change relative/absolute positions of elements and many other options
    
- set <meta name viewport default> to device size in <head> to initialize defaults
    

  

|   |   |
|---|---|
|body{<br><br>  background-color: yellow;<br><br>  }<br><br>@media screen and (orientation: portrait){<br><br>  body{<br><br>    background-color: red;<br><br>}<br><br>}<br><br>  <br><br>@media screen and (orientation: landscape){<br><br>   body{<br><br>    background-color: blue;<br><br>}<br><br>}|default background colour<br><br>  <br>  <br><br>if portrait|

  

3. Flexible Images: resize and crop images as needed applying CSS to image or image frame
    

- browser information needed to display images properly (browser has no prior image knowledge before loading HTML and CSS file but has all device/environment knowledge)
    

  

|   |   |   |
|---|---|---|
|Variables|Developer Knows|Browser Knows|
|Viewport dimensions|no|yes|
|Image size relative to viewport|yes|no|
|Screen density|no|yes|
|Source file dimensions|yes|no|

Need to add in missing information to have images display properly

  

1. srcset attribute: source file dimensions
    

Device-Pixel Ratio: relationship between device physical pixels (dots on screen) and logical pixels (dpp) (CSS pixel)

- physical pixels/logical pixels = device-pixel ratio
    

|   |   |
|---|---|
|<img src = “img/image-x1.jpg<br><br>  <br><br>srcset = img/image-x1.jpg 1x,<br><br>img/image-x2 2x,<br><br>img/image-x3 3x”>|default fallback for old browsers that do not support srcset<br><br>  <br><br>x descriptor used to define device-pixel ratio<br><br>  <br><br>x=1: device-pixel ratio = 1, use image-x1.jpg<br><br>  <br><br>x=2: device-pixel ratio = 2, use image-x2.jpg<br><br>  <br>  <br><br>x=3: device-pixel ratio = 3, use image-x3.jpg|

srcset Width Descriptor: telling browser width of image in pixels before it fetches the image, use widths to decide which to fetch based on window size

- fetches image with smallest width still larger than viewport width
    

  

|   |   |
|---|---|
|<img srcset=”img1.jpg 400w, img2.jpg 800w, img3.jpg 1200w”<br><br>  <br><br>src=”img1.jpg”>|telling set of images with different widths to use based on screen size<br><br>  <br><br>still including default src for older browsers|

  

2. sizes: image file relative to viewport
    

- CSS parsed after HTML at runtime, browser does not know final display size when running (default image is 100% of viewport)
    
- allows to tell display size before fetched
    

  

|   |   |
|---|---|
|<img <br><br>srcset= “img1.jpg 400w, img2.jpg 800w”<br><br>  <br><br>src=”img1.jpg”<br><br>  <br><br>sizes=”50vw”|image options with width sizes<br><br>  <br>  <br>  <br><br>image source for old browsers<br><br>  <br><br>50% of viewport max|

  

3. <picture> element: encloses img tag with multiple source files
    

- container providing multiple sources to contained img element
    
- allow author to declaratively control or give hints of which image to use (based on resolution or device-pixel ratio)
    
- based on screen pixel density, viewport size or image format, represents its children
    

  

|   |   |
|---|---|
|<picture><br><br>  <br><br><source media”(min-width: 1200px)” srcset=”img3.jpg 1x:><br><br>  <br><br><source srcset=”img-cropped.jpg 1x, img-cropped2.jpg 2x”><br><br>  <br><br><img src=”image.jpg”<br><br>srcset=”image2.jpg 2x, image3.jpg 3x”?<br><br>alt=”alt text”><br><br></picture>|all encompassing picture tag|

  

Reading Week 7: Considering Accessibility:

- team effort, should be part of design not add-on afterthought
    

Excuses:

- accessibility is boring
    
- we can’t tell if anyone benefits
    
- we don’t know what to do
    
- it’s hard
    

Inclusion:

1. Accessibility:
    

1. Physical: degree to which environment is usable to as many people as possible (the law)
    
2. Web: degree website is usable to as many people as possible
    

Accessible Design: explicitly considering people with disabilities (usually afterthought added to normal design)

2. Inclusion: Universal Design (Ronald L. Mace): design of products/environments to be usable for all to greatest extent possible without need for adaptation
    

Empathy: have diverse team

Diverse Web Access:

1. Screen Reader: reads screen aloud via braille or output device
    

Keyboard Navigation: person uses only keyboard to access site (up/down = scroll, tab = between interactive elements, space/enter = interact)

2. Navigation Hardware: touchpad/touchscreen/vertical/foot-operated mouse to navigate
    

1. Switch Input: moves through operations on screen and trigger switch when desired option is highlighted
    
2. Eye Tracker: camera analyzes eye movements and makes selections accordingly
    

4. Speech Recognition: mic to understand spoken commands
    
5. Screen Magnifier: zoom in on certain element or whole screen
    

Disabilities/Impairments:

Disability: umbrella term covering impairments (problems in body function or structure), activity limitations (difficulty at specific tasks) and participation restrictions (problems in involvement in life situations)

1. Visual Impairment:
    

1. Colour Blindness
    
2. Eyesight Loss
    

3. Auditory Impairment:
    

1. Conductive: quieter sounds
    
2. Sensorineural: distorted sounds
    

5. Motor Impairment
    
6. Cognitive Impairment
    

1. Memory
    
2. Attention
    
3. Problem Solving
    
4. Text/Math/Visual Processing
    
5. Learning Disabilities
    
6. Literacy
    

8. Vestibular Disorders/Seizures
    

1. Vestibular: dizziness/vertigo or visual/hearing disturbances (triggered by motion/animations)
    
2. Seizures: triggered by fast flashing light (more than 3x per second)
    

Environmental Factors:

1. Browsers (old, new, render differently)
    
2. Mobile device/game console/non desktop access
    
3. Low internet/bandwidth
    
4. Sites not in familiar language 
    

1. make sure fonts have extra characters needed
    
2. write in plain language
    

6. Light/rain
    
7. Noisy/quiet environment
    

  

Lecture Week 7: Usefulness

  

Hierarchy of Needs for Design

|   |
|---|
|pleasurable|
|usable|
|reliable|
|functional|

  

Usability: how easy/pleasant it is to use

Utility: whether you get features you need

Usefulness: usability + utility

  

Feedback and Responsiveness:

- 0.1s: feels instantaneous
    
- 1s: keep flow of thought
    
- 10s: keep user attention
    

  

Accessibility: “accessible by default”

Tools for Accessibility:

- screen
    
- screen reader
    
- speaker
    
- refreshable braille devices
    
- keyboard/mouse
    
- zoom tools
    

Limitations:

- visual (blind/low vision/colour blindness)
    
- hearing (deaf/hard of hearing)
    
- motor (limited motor control, hand tremors)
    
- cognitive (learning/disability, unable to process a lot of information, dyslexia)
    

Making Site Navigable by Keyboard

|   |   |
|---|---|
|a:hover<br><br>a:active<br><br>a:focus|when hovering over<br><br>when press down<br><br>when selected with keyboard|
|<input tabindex=”1” value=”field#1”><br><br>  <br>  <br><br><input tabindex=”-1” value=”ignored”>|tabindex assigns order of field navigation using tab key<br><br>  <br><br>value of -1 means ignored|

  

Fitt’s Law: tells how easy it is to reach target

t (time to reach) = a+b (constants determined by environment) x id (index of difficulty)

id = 2d(distance to target) / w (width of target)

Ways to Decrease Time:

- bigger target (w up)
    
- decrease distance (d down)
    

  

Keeping Accessibility:

Browsers don’t ‘see’, only use structural elements to make sense of page

- semantic elements
    
- let users control interface
    
- clear and consistent interaction points
    
- rich media with descriptors
    

  

ARIA: Accessible Rich Internet Application

1. Roles: purpose of events
    

Roles:

|   |   |
|---|---|
|complementary<br><br>contentinfo<br><br>form<br><br>main<br><br>navigation<br><br>region<br><br>search||

Live Region Roles:

|   |   |
|---|---|
|alert<br><br>log<br><br>marquee<br><br>status<br><br>timer||

  

2. Properties: actions elements can do (draggable)
    
3. States: describe interaction (checkbox checked/unchecked)
    

Usage: use HTML tags first, then ARIA tags if needed (no HTML tag)

  

Reliability: user must be able to complete task repeatedly

Usability: user can complete task with relative ease repeatedly

  

Accessibility Audit:

1. use of semantic elements
    

1. header: defines major headings and website info
    
2. nav: contains links to navigate to different pages/sections of website
    
3. section: contains logical sections of content most likely with heading
    
4. footer: contains meta information about page (copyright/company information)
    

3. setting of language attribute <html lang=”en”>
    
4. appropriate ordering of headings (h1, h2, h3, h4)
    
5. recognizable and focusable links (tell what is link, visual interaction cue)
    
6. appropriate uses of alt text (descriptive of function and content)
    
7. associating labels to inputs (using for in label and id in input)
    
8. navigating with keyboard only (tab and enter keys)
    

  

Reading Week 10: Javascript

Javascript: communication with page contents using Document-Object Model (DOM) API, allowing Javascript to read, alter and remove aspects

Purposes:

1. Translating page into map JS can understand
    
2. Providing JS with methods to access mapped nodes
    

CH1: Getting Set Up:

- embed scripts with <script> </script>
    
- import scripts in head from file with <script src=”js/script.js”></script>
    

- accepts any HTML5 global attributes (class, id, data)
    

  

|   |   |
|---|---|
|<script async>|execute script asynchronously (not for dependencies as may execute script before page is fully loaded)|
|<script defer>|scripts requested in parallel with page parsing|

- ensure document completely parsed before scripts run
    

Dev Tools:

  

|   |   |
|---|---|
|alert()<br><br>confirm()<br><br>prompt()|dialog box with ok<br><br>dialog box with ok or cancel<br><br>dialog box allowing user input|
|console.log()<br><br>console.warn()<br><br>console.alert()|print to console<br><br>print warning to console (yellow)<br><br>print alert to console (red)|

  

Rules:

1. camelcase and case sensitive
    
2. semicolon at end of each line
    
3. whitespace ignored
    
4. comments /* */ = multiline, // = single line
    

  

CH2: Understanding Data Types:

Primitive Types:

undefined: no predefined type in JS

null: defined but no value assigned

typeof: method to return type

1. Number: all numbers
    

NaN: not a number

Infinity/-Infinity: infinity

2. String: enclosed in brackets
    
3. Boolean: true or false
    

Object Types: mutable collection of variables and methods

1. Variable: var f = s;
    

Identifier: name of variable (must start with letter, underscore or $, no special characters, no spaces)

Scope: local or global

2. Array: multiple variables together
    

|   |   |
|---|---|
|var array1 = [1, 2, 3];<br><br>var array2 = new Array(1, 2, 3);<br><br>  <br><br>var array3 = new Arrray(3);<br><br>array30] =0;<br><br>array3[1] = 1;<br><br>array3[2] = 2;|two arrays of 1,2,3<br><br>  <br>  <br><br>array of 1,2,3 initialized after|

Object Properties:

1. object contains String values as properties
    

  

|   |   |
|---|---|
|var myObject{<br><br>“name”:”John”, “color”:”red”<br><br>};|initializing object with key value pairs for properties|

  

2. defining new Object
    

  

|   |   |
|---|---|
|var myObject = new Object();<br><br>var myObject = {};|two ways of defining new Objects (brackets are for adding properties off the bat)|

  

3. accessing properties
    

  

|   |   |
|---|---|
|myObject.color;<br><br>myObject[“name”];|accessing color property<br><br>accessing name property (can pass variable in)|

  

Function: reusable code to perform repetitive task

  

Lecture Week 9: Content and Javascript

  

Content: right for user and context (device/environment)

Allow working on same task across devices:

1. Content Parity (same content regardless of device)
    
2. Consistent Navigational Tools
    
3. Consistent Search (and search results)
    
4. Handy Tools 
    

1. consistent URLs
    
2. save progress when logged in
    
3. email/send link to desktop/mobile site
    

Consuming the Content: Banner Blindness: users ignore anything resembling an ad

Kinds of User Reading:

1. Quick Scan (for keywords)
    
2. Quick Reading (of sentences to get jist)
    
3. Deep Reading (reading all content)
    

Content to support all 3 user behaviours:

- content fulfills a clear/specific purpose
    
- content is user-centered
    
- content is concise/concrete
    
- headers, links, bulleted lists and highlighted text to enhance scanning
    

  

Javascript: behavioural script language allowing interactivity

- created in 1995, run by interpreter built into browser
    

- more engaging websites
    
- react to user input, validate user input, dynamically modify HTML page
    

Inserting:

1. <head> scripts are run before the page is displayed (define functions and variables used by scripts within the body)
    
2. <body> scripts are run as the page is displayed
    

  

|   |   |
|---|---|
|<script src=”myscript.js”></script>|adding external script to document, reuse scripts in several documents|

  

Variables: can be global or local

|   |   |
|---|---|
|var name  = “myvar”;|var keyword|

  

Operators and Constructs:

|   |
|---|
|Arithmetic: +, -, /, %<br><br>Assignment: =, +=, -=, *=, /=, %=, ++, --<br><br>Logical: &&, \|, !<br><br>Comparison: <, >, <=, >=, ==|

  

Basic User Interaction:

|   |   |
|---|---|
|alert(“message”);<br><br>confirm(“message”);<br><br>prompt(“message”, default);|alerts user with box<br><br>asks user to confirm/cancel something<br><br>asks user to enter something|

  

Functions:

|   |   |
|---|---|
|function name(){<br><br>return; }|function keyword<br><br>return keyword|

  

Arrays:

|   |   |
|---|---|
|var array = new Array();<br><br>i[0] = “red”;<br><br>i[1] = “orange”;<br><br>i[2] = “yellow”;<br><br>  <br><br>for (var i in array){<br><br>//do something for each<br><br>}|put elements each in an array by index<br><br>  <br>  <br>  <br>  <br><br>loop through array|

  

Events:

|   |   |
|---|---|
|onload/onunload<br><br>onfocus, onblur, onchange<br><br>onsubmit<br><br>onmouseover, onmouseout|when page is first visited or left<br><br>events pertaining to form elements<br><br>when form is submitted<br><br>for “menu effects”|

  

Exception Handling:

|   |   |
|---|---|
|try{<br><br>runCode();<br><br>} catch (err) {<br><br>var txt = “There was an error “ <br><br>- “Error description: “<br>    <br>- err.description +”\n\n”<br>    <br><br>alert(txt);}|try, catch and throw keywords|

  

JavaScript Objects: object-oriented, uses same method-calling syntax as Java

|   |
|---|
|String: String object is created every time you use string literal (like Java)<br><br>Methods: charAt, concat, indexOf, lastIndexOf, match, replace, search, slice, split, substr, substring, toLowerCase, toUpperCase, valueOf<br><br>HTML Specific Methods (for appearance): do not use, use CSS instead<br><br>Date<br><br>Array<br><br>Boolean<br><br>Math|

  

Document Object Model (DOM): specification determining mapping between programming language objects and elements of HTML document, used to access all elements on page

DOM Objects:

1. Environment: window, navigator, screen, history, location, document
    
2. HTML Objects: anchor, area, base, body, button, event, form, frame, frameset, iframe, image, checkbox, fileupload, hidden, password, radio, reset, submit, text, link, meta, object, option, select, style, table, tablecell, tablerow, textarea
    

Collections: anchors, forms, links

Properties: body, cookie, domain, lastModified, referrer, title, URL

Methods: getElementById, getElementsByName, getElementsByTagName, write, writeIn, open, close

  

Changing DOM with JavaScript: 

1. change/add/remove all HTML elements/attributes
    
2. react to existing HTML events in the page
    
3. create new HTML events in the page
    
4. change all CSS styles
    

  

|   |   |
|---|---|
|‘use strict’;|prevents you from breaking any rules/ensures clean code|

  

Console: console object refers to developer tools console

|   |   |
|---|---|
|console.log(“message”);||

  

Window: window object gives information about browser window

|   |   |
|---|---|
|var width = window.innerWidth;||

  

Selecting Elements from DOM: Casting elements into variables:

|   |   |
|---|---|
|var nameOfVariable = object.method(argument);<br><br>  <br><br>var navToggle = document.querySelector(“#nav-toggle”);|method convention syntax<br><br>  <br>  <br><br>returns first HTML object in DOM that it finds with given CSS selector|

  

Event Listener Adding: tie event listeners to object so they react to user interaction

|   |   |
|---|---|
|if (condition) { //things to run }<br><br>  <br><br>if (width < 500) {  }||

  

ARIA Accessibility: make sure element properties and aria attributes match

|   |   |
|---|---|
|navToggle.setAttribute(“aria-hidden”, “false”);<br><br>  <br><br>navItems.classList.add(“hidden”));||

  
  

Lecture Week 10: Portfolio, More Javascript and Challenges of Modern Web

  

Portfolio:

1. what makes you different?
    
2. who do you want to work for?
    
3. what makes you unique (but employable)?
    

Ethos: argument appealing to audience by emphasizing speaker’s credibility and authority *understanding, characteristics, definition of self as ___)

Showcasing Work:

- use lots of visuals but explain them, 250-300 words max
    

1. what is the project? (brief 1 paragraph description)
    
2. what was the context? (academic, work, personal)
    
3. who was involved and what did you do?
    
4. process analysis: (different depending on different audiences)
    

1. describe project
    
2. analyze and explain project
    
3. identify problems and resolutions
    
4. evaluate effectiveness/reflects on solutions
    

6. why it matters (what was learned, accomplished, reflection/improvements if were doing it again)
    

Purpose:

1. reflective practice
    
2. employers look at portfolio website for the longest, want custom, non-template website with clear branding
    

  

Javascript 2:

Browser: sees webpage as one object

HTML DOM: structured hierarchical representation of everything within document in document trree, access to change document structure (HTML), document style (CSS), document content

- interactive experience, responding to user events, validating forms, image galleries
    

  

|   |   |
|---|---|
|getElementById()<br><br>getElementsByTagName()<br><br>getElementsByClassName()|one element<br><br>multiple elements<br><br>multiple elements|

  

Make text bold/change text:

  

|   |   |
|---|---|
|var selectedClass = document.getElementsByClassName("myclass");<br><br>console.log(selectedClass.length);<br><br>  <br><br>for (var i = 0; i < selectedClass.length; i++) {<br><br> console.log(selectedClass[i]);<br><br> selectedClass[i].innerHTML =<br><br> '<B>' + (i+1) +". Class for this element is MYCLASS </B>";<br><br>}||

  

Change styling of elements with class name:

  

|   |   |
|---|---|
|var rowElement = document.getElementsByClassName("row");<br><br>console.log(rowElement.length);<br><br>  <br><br>for (var i = 0; i < rowElement.length; i ++){<br><br>   // rowElement[i].classList.add('new-look');<br><br>   rowElement[i].className += ' new-look';<br><br>}||

  

Create new element:

  

|   |   |
|---|---|
|var ul = document.getElementById('mylist');<br><br>var li = document.createElement('li');<br><br>li.appendChild(document.createTextNode("List F"));<br><br>li.setAttribute("id", "listF");<br><br>li.classList.add("listClass");<br><br>ul.appendChild(li);||

  

Event Listeners:

  

|   |   |
|---|---|
|var myButton = document.getElementsByClassName('btn');  //gets all buttons<br><br>var myOutput = document.getElementById('output'); //gets output area (div)<br><br>  <br><br>for (var i=0; i<myButton.length; i++){<br><br> var btnClick = function(){<br><br>   myOutput.textContent = "You clicked " + this.id;  //adding text content to output div<br><br>   };<br><br> myButton[i].addEventListener("click", btnClick);||

  

React to mouse events:

  

|   |   |
|---|---|
|for (var i=0; i<myButton.length; i++){<br><br> var btnClick = function(){<br><br>   myOutput.textContent = "You clicked " + this.id;  //adding text content to output div<br><br>   };<br><br> myButton[i].addEventListener("click", btnClick);<br><br>  <br><br> //mouse events<br><br>var myOutput1 = document.getElementById('output1');<br><br>var myArea = document.getElementById ("myImage");<br><br>var mouseMover = function(e){<br><br>     console.log(e);<br><br>     console.log(e.x);<br><br>     myOutput1.textContent = "x: " +e.x, " y: "+e.y;<br><br>   };<br><br>myArea.addEventListener("mousemove", mouseMover);<br><br>  <br><br>}||

  

Challenges of Modern Web: Web Ethics

- ethics, morality and duty associated with web issues, how they relate to work as designers or developers
    

1. Privacy: how is this understood
    
2. Data and Ownership: how is data owned?
    
3. New Neutrality: how do we balance access?
    

  

Sass for Designers

  

Sass: CSS preprocessor between filesheets you author and browser (scss to css), allows more functionalities than css, converts itself to css

Syntax:

1. SCSS: superset of CSS, can write normal CSS that works in it, can gradually convert to Sass, doesn’t require code format shift
    

  

|   |   |
|---|---|
|$pink: #ea4c89;<br><br>  <br><br>p {<br><br>  font-size: 12px;<br><br>  color: $pink;<br><br>}<br><br>p strong {<br><br>  text-transform: uppercase;<br><br>}|defines variable to use in block|

  

2. Original Indented Sass Syntax: no curly braces or semicolons, otherwise the same
    

  

Styles of CSS Conversion:

1. nested (default)
    
2. expanded
    
3. compact
    
4. compressed
    

  

Sass Syntax:

- can do nested properties reflecting HTML to not rewrite same code repeatedly
    
- nest properties (if all start with same word)
    
- reference parent selectors with &
    
- comments: // (not included in final /* or /*! (included in final)
    
- variables: $name: value;
    
- color: darken/lighten by percentage
    
- mixins: define and reuse blocks of styles (@mixin), can also take arguments)
    
- import common scss into all projects with common mixins, puts it all in one file (that’s used)
    
- @extend classes to add to them
    
- % placeholder selector (interface equivalent)
    

Lecture Week 11: Preprocessing and CSS Animation

  

Preprocessing with Sass: 

Sass: CSS preprocessor, scss > sass (converts) > css

- step between what we write (scss) and what browser sees (css) that transforms css into normal coding language with variables and reusable blocks
    
- allows Don’t Repeat Yourself (DRY) code
    

  

Benefits:

1. Variables: across stylesheets instead of rewriting values
    

  

|   |   |
|---|---|
|$brand-color: #fc3;<br><br>a{color: $brand-color;}|set colour variable<br><br>use colour variable|

  

2. Repeated Blocks (Mixins): shared rules put into one reusable block 
    

  

|   |   |
|---|---|
|@mixin default-type{<br><br>//css}<br><br>  <br><br>p{<br><br>@include default-type; }|setting mixin<br><br>  <br>  <br><br>using mixin|

  

3. Nesting: allows you to nest properties like you would in HTML
    

  

|   |   |
|---|---|
|ul{<br><br>color:red;<br><br>  <br><br>li{<br><br>padding: 5px;}<br><br>}|li items within ul will have this styling applied|

  
  

Workflow:

1. edit stylesheet with scss syntax
    
2. use prepross (sass) to monitor file/folder
    
3. use sass to convert scss to css that browser can parse
    

- can use prepross or command line
    

  

Outcome: CSS file, formatting depends on what stage we are at (done versus in progress)

1. Nested: reflect structure of HTML
    
2. Expanded: similar to manually written CSS
    
3. Compact: each declaration on own line, selectors emphasized
    
4. Compressed: removes all spaces and line breaks, smallest file size
    

  

Using Sass: Prepross

- add project to Prepross, will watch scss files for changes
    
- on save automatically converts into css files
    

  

Speed Optimization:

1. render blocking: anything in head must be loaded before page rendering
    
2. prepross/compress: minify all files 
    
3. critical render path: consider what is necessary and what can wait (head v. body)
    

  

CSS Animations:

- objects in DOM are static, flat, rectangular objects, animations can move object or change shape
    

Transformations: 

1. Translate: move along 1+ axis
    

Units: ems, pixels, percentages (of object size)

1. Skew: changing line of symmetry with number of degrees
    
2. Rotate
    
3. Scale
    

|   |   |
|---|---|
|transform: translate(200px, 50px) skew(20deg) scale(2deg) rotate(45deg);|apply multiple transformations<br><br>  <br><br>**order written are order applied|

Transform Stacking Order: order written is order applied

  

3D Transformations: add perspective (z axis), effect of close or far away

- larger value = far, smaller value = close
    

  

CSS Transitions:

  

|   |   |
|---|---|
|transition: background .6s ease-in, transform .2s ease-out;||

  
  

CSS Keyframe Animation:

Keyframes: list of steps in animation, assign values for properties as keyframes

1. define animation
    

  

|   |   |
|---|---|
|@keyframes slide{<br><br>from {transform: translateX(0);}<br><br>to {transform: translateX(500px);}<br><br>}|naming and creating animation with keyframes<br><br>- use from, to or 0%, 100% (for more than two steps)|

  

2. assign animation to specific element
    

  

|   |   |
|---|---|
|.cat{<br><br>animation-name: slide;<br><br>animation-duration: 2s;<br><br>animation-timing-function: ease-in;<br><br>animation-iteration-count: 2;<br><br>}|assign animation and give properties|

  

- steps can be done in either order (good to define first though)
    

  

Animation Control:

  

|   |   |
|---|---|
|animation-delay|waiting time before animation executes|
|animation-fill-mode<br><br>  <br><br>none: default<br><br>backward: applied style from first keyframe before animation starts<br><br>forward: applies style from last keyframe at end<br><br>both: applies styles both before start and after end of animation|defines what element will do outside interval of animation|
|animation-direction:<br><br>normal/reverse<br><br>alternate/alternate-reverse: will alternate direction (only use if animation iteration count greater than 1)|manipulate order of keyframes|
|animation-timing-function:<br><br>Easing: how speed of element is distributed across animation<br><br>  <br><br>Predefined Keywords:<br><br>1. linear: uniform speed<br>    <br>2. ease (default): slow start, fast, slow end<br>    <br>3. ease-in: slow start<br>    <br>4. ease-out: slow end<br>    <br>5. ease-in-out: slow start and slow end<br>    <br><br>  <br><br>Cubic Bezier Functions: custom easing effect<br><br>cubic-bezier(x1, y1, x2, y2);||

  

Scalable Vector Graphics (SVG): used to define vector based graphics on web

- defined in XML format, every element and attribute in SVG can be animated
    
- do not lose any quality if zoomed/resized
    
- integrates with DOM
    

Animating SVG: can animate fill, opacity, use CSS transforms if you have SVG code for element

