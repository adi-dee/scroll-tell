# Video Scroller

This is a basic intro to multimedia scrollytelling using media from environmental activist [Mina Guli's #runblue campaign](https://twitter.com/minaguli) to demonstrate a couple of scrollytelling techniques.

## Step by step guide to Scrollytelling

Before remixing this glitch project, work through the Bill Shander LinkedIn Tutorial, [Step by step guide to Scrollama](https://www.linkedin.com/learning/scrollytelling-creating-a-one-page-web-experience)

You will want to understand exactly how the basic step interaction works and how the javascript interacts with the HTML elements on the page.
The html dataset will be very important for multimedia interactions, later, so do focus on this.

More complex animations are optional. You can come back to this later if you want to create more complex interactions e.g. progressive animations. (Optional)

The Shander tutorial example uses a float layout, which is very limited for more complex multimedia designs.

# Caveat

These examples are designed to introduce some multimedia scrolling techniques to media students.
These are not always suitable for responsive sites.
You will be investigating this issue for your reflection paper in the final assignment.

# What's in this project?

← `README.md`: That's this file, work in progress

## Example 1 - multimedia with flexbox layout and HTML dataset

← `flexbox.html`: Simple multimedia scrolling, flexbox layout.

This example linked below shows you how to

- integrate a flexbox layout and sticky positioning of various types of multimedia
- swop media using the HTML dataset techniques explained in the Bill Shander LinkedIn tutorial to change images, graphs and videos.

Here's an explanation of how CSS positionining with ```position:sticky``` makes this possible.

[Easier scrollytelling with position sticky](https://pudding.cool/process/scrollytelling-sticky/)

[Flexbox w basic scrollama](https://scrollytelling-tutorial.glitch.me/basic/)

Look through the code to locate the following:

- Styles for layout - This is a work in progress, and so I've included most of the styles needed to control layout of scrollytelling in the html file. This first example gives you a flexbox layout with a sticky image(figure) and variable length text(article). Figure and article are laid out side by side (adapted from Goldenberg's Sticky Overlay tutorial template).
- Intro section with title (hed), subtitle (dek) and background video
- Three separate scrollable sections ("scrolly")
  - Each section has both a figure section and an article section
  - Each section demonstrates how you can use a different type of object in the figure
    - images
    - svgs
    - iframes (for flourish charts)
    - video
- Figure section - images with captions
  - Figures (featured images, svgs, iframes or videos) with "sticky" positioning applied
  - Figcaptions (captions)
- Article section - For the scrollable article text/script (divided into steps)
- Outro section - Concluding text and credits
- Script - Javascript to setup the scrollama

```
<script type="text/javascript">
  const scroller = scrollama();
  const caption = document.getElementById("captionObj");
  scroller
  .setup({
      step: ".step",
      offset: 0.2,
  })
  .onStepEnter((response) => {
      console.log(response);
      document.getElementById(response.element.dataset.target).setAttribute(response.element.dataset.attribute,    response.element.dataset.value);
      if  (response.element.dataset.target== "imgObj"){
        let alt = response.element.dataset.text
        if( alt )
          {
          caption.innerText = alt;
          }
      }
	});
  window.addEventListener("resize", scroller.resize);
</script>
```

## Example 2 - multimedia with sticky side layout and HTML dataset

← `sticky_image.html`: Sticky side scrolling for charts and flexbox layout

The sticky side image example:

[Sticky side image layout](https://video-scroller.glitch.me/sticky_image.html)

The example uses Goldenberg's Sticky Side template. I would recommend this layout for scrollable charts, infographics etc where you need to be able to see the entire image.
Look through the code to locate the following:

- Styles for layout - This is a work in progress, and so I've included most of the styles needed to control layout of scrollytelling in the html file. A flexbox layout with image and text laid out side by side (adapted from Goldenberg's Sticky Overlay tutorial template)
- Intro section with title (hed), subtitle (dek) and background video
- Figure section - images with captions
  - Figures (featured images) with
  - Figcaptions (captions)
  - Paragraph elements - numbers superimposed on the images (for debugging purposes).
- Article section - For the scrollable article text/script (divided into steps)
- Outro section - Concluding text and credits
- Script - Various levels of Javascript

## Example 3 - multimedia with sticky overlay and HTML dataset

← `index.html`: Sticky overlay scrolling for large photos, layout with absolute positioning and hardcoded step sizes  

The sticky overlay example:

[Sticky overlay layout](https://video-scroller.glitch.me/index.html)

The example uses Goldenberg's Sticky Overlay template to implement scrolling interactions with video and images.
Look through the code to locate the following:

- Styles for layout - This is a work in progress, and so I've included most of the styles needed to control layout of scrollytelling in the html file.A flexbox layout with image and text laid out side by side (adapted from Goldenberg's Sticky Overlay tutorial template)
- Intro section with title (hed), subtitle (dek) and background video
- Figure section - images with captions, absolute positioning
  - Figures (featured images) with
  - Figcaptions (captions)
  - Paragraph elements - numbers superimposed on the images for debugging purposes.
- Article section - For the scrollable article text/script (divided into steps with fixed sizes)
- Outro section - Concluding text and credits
- Script - Various levels of Javascript

## Javascript

This exercise is intended to allow you to focus on multimedia storytelling and some simple scrolling interactions.
You will need to make some simple javascript edits in addition to customising the HTML content, media assets and CSS.
I recommend you use the Example 2 or 3, which have better functionality to handle resizing of the window - handleResize()

Depending on the level of changes you want to make to the functionality, you can edit the Javascript in the file to swop in your own images+captions and add functionality which triggers whenever the user enters a step.
It's entirely optional to change more complex aspects of the Scrollama setup, how the browser handles a resize event or any more complex animations and fades.

### Add your own images and captions

- You can swop in your own images and captions without changing the Javascript - just change the HTML data. If you want to caption other types of media, first check the script carefully to see how the HTML dataset is set up for that specific media object.

### Add simple functionality to handleStepEnter

- handleStepEnter() function - To add functionality (e.g. provide captions for media other than images) you will need to edit the javascript here.

### More complex 

- Scrollama setup() - here you can change details of how steps function or debug using the display lines. For example, if you set debug="false" you can get rid of the guidelines, and offset changes where handleStepEnter() is triggered.

Optional extras:
- handleReSize() function - handles resizing of display window
- handleStepEnter() - Visual effects to fade steps in and out

Rather than building an overly complex script, rather try out these basic layouts in combination with other techniques you've been taught e.g. scrollable background images and video.

## Javascript libraries

← `d3.min.js`: D3 library - Don't edit this - used in template 

← `scrollama.min.js`: Scrollama library - Don't edit this - basic scrollytelling functionality is here

## External styles

For ease of learning, most of the styles are in the HTML documents. There are a few in a separate stylesheet

← `style.css`: Basic styles (mostly typography and media queries)

## Links

The examples are all based on the templates and tutorials linked here.

Russel Goldenberg

- [Introducing Scrollama](https://pudding.cool/process/introducing-scrollama/)
- [Responsive Scrollytelling](https://pudding.cool/process/responsive-scrollytelling/)
  For more advanced projects and for those writing papers about scrollytelling and user experience
  [Sticky side template](https://russellgoldenberg.github.io/scrollama/sticky-side/) (captions scroll without obscuring image)

[Overlay template](https://russellgoldenberg.github.io/scrollama/sticky-overlay/) (captions scroll as overlay on sticky graphic)

Bill Shander LinkedIn Tutorial - [Step by step guide to Scrollama](https://www.linkedin.com/learning/scrollytelling-creating-a-one-page-web-experience)

This will help you understand exactly how javascript interacts with the HTML elements on the page.

[Mapbox example](https://glitch.com/~stellenbosch-heritage-tree-storymap) - For more complex map interactions
