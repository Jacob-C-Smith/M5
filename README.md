# web-dev-starter

This is a starter project for web development with no frameworks and minimal
dependencies. It is intended to be a starting point for web development projects
that are written in plain HTML, CSS, and JavaScript.

## Getting Started

To get started, clone this repository and run the following commands:

```bash
npm install
```
This will install the necessary dependencies for the project.

## Development

It is recommended to use the VSCode Live Server extension to run the project
locally. This will allow you to see changes in real-time as you make them. There
is no need to run a build process or refresh the page manually. Additionally,
you do not need to setup a local server to run the project.

## Testing

To run the tests for the project, run the following command:

```bash
npm test
```

## Accessibility Lab Answers
### Color
**The text is difficult to read because of the current color scheme. Can you do a test of the current color contrast (text/background), report the results of the test, and then fix it by changing the assigned colors?**

Contrast is the difference between two luminance values. The background of the website is #008000, so the luminance is  at %25. The foreground is #000000, so the luminance is at %0. The difference in luminance (contrast) is only %25; Rather low. I think a better value for the background color might be #ffffff; Pitch white. This value gives a luminance of %100, making the contrast an even %100. 

### Semantic HTML
1. **The content is still not very accessible — report on what happens when you try to navigate it using a keyboard.**

    When I try to navigate using tab, the selected element goes from the navbar to the search, and then to the \<audio> element at the foot of the page. I would've expected that, after navigating off the search bar, it would select the first \<li> in the \<ul> on the \<aside>, but this makes sense. One might expect that, a user would read the article before directing her attention to the aside

2. **Can you update the article text to make it easier for screen reader users to navigate?**
    
    Yes. I added tab indexes.

3. **The navigation menu part of the site (wrapped in ```<div class="nav"></div>```) could be made more accessible by putting it in a proper HTML semantic element. Which one should it be updated to? Make the update.**

    The *nav* \<div> element should be replaced with a \<nav> element.

### The Images
4. **The images are currently inaccessible to screen reader users. Can you fix this?**
    
    Yes. I added an "alt" attribute to both images.

### The Audio Player
1. **The \<audio> player isn't accessible to hearing impaired (deaf) people — can you add some kind of accessible alternative for these users?**
    
    Sure. I added a \<track> tag, and wrote a WebVTT transcript.

2. **The \<audio> player isn't accessible to those using older browsers that don't support HTML audio. How can you allow them to still access the audio?**

    Maybe provide a link to download the file directly? I used the anchor element.

###  The Forms
1. **The \<input> element in the search form at the top could do with a label, but we don't want to add a visible text label that would potentially spoil the design and isn't really needed by sighted users. How can you add a label that is only accessible to screen readers?**

    I used the aria-label attribute to hint that this text input is for search queries

2. **The two \<input> elements in the comment form have visible text labels, but they are not unambiguously associated with their labels — how do you achieve this? Note that you'll need to update some of the CSS rule as well.**

    To resolve the ambiguity, I added \<label> elements with "name" attributes.

### The Show/Hide Comment Control
**The show/hide comment control button is not currently keyboard-accessible. Can you make it keyboard-accessible, both in terms of focusing it using the tab key and activating it using the return key?**

Easy peasy. I changed the control from a \<div> element to a \<button> element, and I added a tab index. The latter may not have been neccesary, but HTML is no exact science.


### The Table
**The data table is not currently very accessible — it is hard for screen reader users to associate data rows and columns together, and the table also has no kind of summary to make it clear what it shows. Can you add some features to your HTML to fix this problem?**

I used aria roles to make the table easier to parse for screen readers. I also updated the \<thead> element to contain \<th> elements

### Other Considerations?

**Can you list two more ideas for improvements that would make the website more accessible?**

1. Some people don't speak English. Maybe one could add more audio files / transcripts for say, German?
2. ... I thought about this for a good 30 minutes, and I couldn't come up with anything. I don't know if I'm stupid or what... The best idea I had was to change the colors to be accessible for color blind people, but that doesn't actually matter here.