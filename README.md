# Video Scroller

This is a basic intro to multimedia scrollytelling using media from environmental activist [Mina Guli's #runblue campaign](https://twitter.com/minaguli) to demonstrate a couple of scrollytelling techniques.
![MinaGuli](https://pbs.twimg.com/profile_banners/111631792/1659954268/1080x360)

## What's in this project?

← `README.md`: That's this file, work in progress

← `index.html`:
The example uses Goldenberg's Sticky Overlay tutorial to implement scrolling interactions with video and images.
Look through the code - you should find examples of the following:
- A background video

- Styles for layout
This is a work in progress, and so I've included most of the styles needed to control layout of scrollytelling in the html file.

- A flexbox layout with image and text laid out side by side (adapted from Goldenberg's Sticky Overlay tutorial template)

- Javascript  
The Javascript in the file combines several techniques:

- Scrollama - HTML dataset techniques (to swop images and captions) as explained in a Bill Shander LinkedIn tutorial on Scrollytelling
- Scrollama - Fading steps in and out and to handle resizing of the display window.
- Scrollama The example has lines to help you debug scrolling and other usability issues. Set debug="false" to get rid of the guidelines.

You can see this layout in combination with other techniques you've been taught in this more complex example.

← `style.css`: Basic styles (mostly typography and media queries)

← `scrollama.min.js`: Scrollama library - You don't need to edit this - basic scrollytelling functionality is here

## Links

The examples adapt these templates for use with images and video.

Russel Goldenberg 
- [Introducing Scrollama](https://pudding.cool/process/introducing-scrollama/) 
- [Responsive Scrollytelling](https://pudding.cool/process/responsive-scrollytelling/)
 For more advanced projects and for those writing papers about scrollytelling and user experience 
[Sticky side template](https://russellgoldenberg.github.io/scrollama/sticky-side/) (captions scroll without obscuring image)

[Overlay template](https://russellgoldenberg.github.io/scrollama/sticky-overlay/) (captions scroll as overlay on sticky graphic)

Bill Shander LinkedIn Tutorial - [Step by step guide to Scrollama](https://www.linkedin.com/learning/scrollytelling-creating-a-one-page-web-experience)

This will help you understand exactly how javascript interacts with the HTML elements on the page.

