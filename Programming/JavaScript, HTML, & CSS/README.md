# JavaScript, HTML, and CSS

##  Purpose & Outline

The goal of this folder is to provide helpful resources and suggestions to lab members learning JavaScript/HTML/CSS, as well as designating some general conventions and best practices for coding styles.

## JavaScript

[JavaScript](http://javascript.info/intro) is a dynamic language which can be used to make MTurk experiments or creating websites with interactive features. While HTML provides the basic structure of a site and CSS the formatting, JavaScript allows you to present stimuli, record reaction times, respond to user inputs, etc.

Recommended:
* Free Online [JavaScript Textbook](https://javascript.info/)
* [jquery](https://jquery.com/)
* [jspsych](https://www.jspsych.org/)
    * Alternative to jquery. It is easier to use in general but offers less flexibility and power.
* [Canvas tutorial](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial)
    * Canvas is a special HTML element which you can use to show stimuli with scripting. It is more flexible/dynamic than using html elements. Definitely worth checking out.
* [MTurk Tutorial](https://bradylab.ucsd.edu/ttt/) by Timothy Brady.
    * This is slightly MTurk specific, but great all around resource for learning the basics of JavaScript/HTML/CSS.

Others:
* This [comprehensive tutorial](https://crumplab.github.io/programmingforpsych/web-experiments.html)
    * Looks really good, haven't tried it.
* Duke's [coursera course](https://www.coursera.org/learn/duke-programming-web)
* Codecademy's JavaScript [course](https://www.codecademy.com/learn/introduction-to-javascript)
* w3schools.com's [tutorial](https://www.w3schools.com/js/) - not as good as the textbook (I tried both).
* As always, remember to look up problems you have on [stack overflow](https://stackoverflow.com/)!

>Note: If you have never programmed before, start with the resources under 'Others'. They are more approachable and will teach you the basics of programming along with JavaScript. There are hundreds of basic these tutorials out there, find one you like!

## HTML

## CSS

CSS, or 'Cascading Style Sheets', is a language that allows you to modify the output of HTML content. Usually this is nothing more than creating a 'styles.css' file in which you specify default fonts, formatting, and spacing of your html content. See here (link pending) for an example.

Recommended Resources:
* https://www.w3schools.com/css/
* https://htmlcheatsheet.com/css/

**Selector Reference:** How do you refer to different HTML elements? See [here](https://www.w3schools.com/cssref/css_selectors.asp) for a detailed description of selectors.

- To refer to a specific html element, reference that element's id using `.htmlId{}`.
- To refer to an entire class of html elements, use `#htmlClass{}`.
- To refer to an every single html tag of a certain type, use `htmlTagName{}`. For example, to change the default for everything in the `body` tag you would type `body{}`.

**Specificity:** In the following example, how what color will the `Header2` text be?

Html:

    <body>
      <div id='allMyHeaders'>
        <h1 id='header1' class='headerClass'>
          This is header 1.
        </h1>
        <h2 id='header2' class='headerClass'>
          This is header 2. What color will I be?
        </h2>
      </div>
    </body>

CSS:

```
body{
  color: black;
}

.allMyHeaders{
  color: blue;
}

#headerClass{
  color: green;
}
```

Answer: Since `header2` belongs to `body`, div `allMyHeaders`, AND class `headerClass`, any one of these references could change the font color. In this case `header2` would appear as **green**, for two reasons:

1. CSS always runs top to bottom, so the bottom reference gets priority.
2. CSS also works by specificity. `headerClass` is more *specific* than div `allMyHeaders`, so it gets priority.

Specificity can get confusing pretty quickly, so make sure to always check your code! See [here](https://developer.mozilla.org/en-US/docs/Web/CSS/Specificity) for a detailed description of specificity.

## Mechanical Turk

Coding experiments specifically with MTurk in mind requires several additional considerations. For example, the code must be able to integrate with MTurk's website, and you need to handle specific issues that might arise when working with MTurkers.

Recommended:

* [MTurk Tutorial](https://bradylab.ucsd.edu/ttt/) by Timothy Brady.
    - This is also a great tutorial for JavaScript/HTML/CSS as well!  
* MTurk has a [developer guide](https://www.mturk.com/resources)
* [MTurk code samples](https://github.com/aws-samples/mturk-code-samples), including JavaScript code.

Other:
* Lab at Stanford's [tutorial](http://cocolab.stanford.edu/mturk-tools.html)
* If you're using jsPsych - see this [MTurk guide](https://www.jspsych.org/overview/mturk/)

>Note: These are just programming resources, not MTurk resources more generally. See the MTurk Folder (link TBD) for information about using MTurk.
