# JavaScript, HTML, and CSS

##  Purpose & Outline

The goal of this folder is to provide helpful resources and suggestions to lab members learning JavaScript/HTML/CSS for the first time, as well as designating some general conventions and best practices to ensure that members use relatively similar coding styles.

## JavaScript

[JavaScript](http://javascript.info/intro) is a dynamic language, which you will use if you are making MTurk experiments or creating a website with interactive features. While HTML provides the basic structure of a site and CSS the formatting, JavaScript can allow you to present stimuli, record reaction times, and respond to user inputs, etc.

Recommended:
* Free Online [JavaScript Textbook](https://javascript.info/)
* [JQuery](https://jquery.com/)
* [jspsych](https://www.jspsych.org/)

Others:
* Duke's [coursera course](https://www.coursera.org/learn/duke-programming-web)
* Free/generic [coursera course](https://www.coursera.org/learn/javascript)
* Codecademy's JavaScript [course](https://www.codecademy.com/learn/introduction-to-javascript)
* w3schools.com's [tutorial](https://www.w3schools.com/js/) - not as good as the textbook (I tried both).
* [pluralsight.com JS course](https://www.pluralsight.com/paths/javascript?utf8=%E2%9C%93&query=javascript) - potentially good but requires $$
* As always, remember to look up problems you have on [stack overflow](https://stackoverflow.com/)!

>Note: If you have never programmed before, start with the resources under 'Others'. They are more approachable and will teach you the basics of programming along with JavaScript.

## HTML

## CSS

CSS, or 'Cascading Style Sheets', is a language that allows you to modify the output of HTML content. Usually this is nothing more than creating a 'styles.css' file in which you specify default fonts, formatting, and spacing of your html content. See here (put in link for some css file) for an example.

Recommended Resources:
* https://www.w3schools.com/css/
* https://htmlcheatsheet.com/css/

**Selector Reference:** How do you refer to different HTML elements? See [here](https://www.w3schools.com/cssref/css_selectors.asp) for a detailed description of selectors.

- To refer to a specific html element, reference that element's id using `.htmlId{}`.
- To refer to an entire class of html elements, use `#htmlClass{}`.
- To refer to an every single html tag of a certain type, use `**htmlTagName{}**`. For example, to change the default for everything in the `body` tag you would type `body{}`.

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

## Programming Experiments for MTurk

Coding experiments specifically with MTurk in mind requires several additional considerations. For example, the code must be able to integrate with MTurk's website. For more general MTurk resources, go to the MTurk Folder (link TBD).

Here are some MTurk-specific JavaScript resources:

* Tim Brady at UCSD gave an excellent [MTurk Programming Lecture](https://bradylab.ucsd.edu/ttt/)
*

## Atom

If you are using [Atom](https://atom.io/) as your code editor, here are some useful installs that will make your life a lot easier (and help you learn faster!)

* [Useful Atom Packages](http://voidcanvas.com/12-must-have-atom-extensions-to-work-in-javascript/)

If you use another code editor, such as [Sublime Text](https://www.sublimetext.com/) or another, feel free to update this editor with similarly useful information.
