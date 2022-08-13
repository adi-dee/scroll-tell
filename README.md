# Video Scroller

This is a basic intro to multimedia scrollytelling using media from environmental activist [Mina Guli's #runblue campaign](https://twitter.com/minaguli) to demonstrate a couple of scrollytelling techniques.
![MinaGuli](https://pbs.twimg.com/profile_banners/111631792/1659954268/1080x360)

## Understand Scrollytelling

Before remixing this glitch project, start with the Bill Shander LinkedIn Tutorial, [Step by step guide to Scrollama](https://www.linkedin.com/learning/scrollytelling-creating-a-one-page-web-experience)
The tutorial example uses a float layout, which is very limited for more complex multimedia designs but working through it will help you understand exactly how javascript interacts with the HTML elements on the page. 
You can come back to it later if you want to create more complex interactions e.g. progressive animations. (Optional)
 
## Add a flexbox
This example linked below shows you how to use the HTML dataset techniques explained in the Bill Shander LinkedIn tutorial to change images, graphs and videos.

Note - uses a flexbox layout instead of float (as in the tutorial).
Basic scrollama
https://scrollytelling-tutorial.glitch.me/basic/


First work through the sticky side image example
[Sticky image](https://video-scroller.glitch.me/sticky_image.html)

After that try the sticky overlay example
[Sticky image](https://video-scroller.glitch.me/index.html)


## What's in this project?

← `README.md`: That's this file, work in progress

← `sticky_image.html`: Sticky side - start here
The example uses Goldenberg's Sticky Side template. The layout is more suitable for scrollable charts, infographics etc.
Look through the code - to locate the following:
- Styles for layout - This is a work in progress, and so I've included most of the styles needed to control layout of scrollytelling in the html file.A flexbox layout with image and text laid out side by side (adapted from Goldenberg's Sticky Overlay tutorial template)
- Intro section with title (hed), subtitle (dek) and background video
- Figure section - images with captions
  - Figures (featured images) with 
  - Figcaptions (captions) 
  - Paragraph elements - numbers superimposed on the images (for debugging purposes). 
- Article section - For the scrollable article text/script (divided into steps)
- Outro section - Concluding text and credits
- Script - Various levels of Javascript

← `index.html`: Sticky overlay
The example uses Goldenberg's Sticky Overlay template to implement scrolling interactions with video and images.
Look through the code - to locate the following:
- Styles for layout - This is a work in progress, and so I've included most of the styles needed to control layout of scrollytelling in the html file.A flexbox layout with image and text laid out side by side (adapted from Goldenberg's Sticky Overlay tutorial template)
- Intro section with title (hed), subtitle (dek) and background video
- Figure section - images with captions
  - Figures (featured images) with 
  - Figcaptions (captions) 
  - Paragraph elements - numbers superimposed on the images for debugging purposes. 
- Article section - For the scrollable article text/script (divided into steps)
- Outro section - Concluding text and credits
- Script - Various levels of Javascript

## Javascript
This exercise is intended to allow you to focus on storytelling but you will need to make some simple javascript edits in addition to customising the HTML content, media assets and CSS. 
Depending on the level of changes you want to make to the functionality, you can edit the Javascript in the file:
### Add your own images and captions 
- You can swop in your own images and captions without changing the Javascript - check the code to see how the HTML dataset is set up for differnt types of media.
### Add simple functionality to step enter
- handleStepEnter() function - To add functionality (e.g. provide captions for media other than images) you will need to edit the javascript here 
### More complex functionality (optional)
- Scrollama - Fading steps in and out and to handle resizing of the display window.
- Scrollama setup() - here you can change details of how steps function. 
Useful for debugging - Display lines help you debug scrolling and other usability issues. Set debug="false" to get rid of the guidelines.

You can see this layout in combination with other techniques you've been taught in this more complex example.

← `style.css`: Basic styles (mostly typography and media queries)

← `d3.min.js`: D3 library used for  

← `scrollama.min.js`: Scrollama library - You don't need to edit this - basic scrollytelling functionality is here

## Links

The examples adapt the templates and tutorials below for multimedia storytelling.

Russel Goldenberg 
- [Introducing Scrollama](https://pudding.cool/process/introducing-scrollama/) 
- [Responsive Scrollytelling](https://pudding.cool/process/responsive-scrollytelling/)
 For more advanced projects and for those writing papers about scrollytelling and user experience 
[Sticky side template](https://russellgoldenberg.github.io/scrollama/sticky-side/) (captions scroll without obscuring image)

[Overlay template](https://russellgoldenberg.github.io/scrollama/sticky-overlay/) (captions scroll as overlay on sticky graphic)

Bill Shander LinkedIn Tutorial - [Step by step guide to Scrollama](https://www.linkedin.com/learning/scrollytelling-creating-a-one-page-web-experience)

This will help you understand exactly how javascript interacts with the HTML elements on the page.

[Mapbox example](https://glitch.com/~stellenbosch-heritage-tree-storymap) - For more complex map interactions