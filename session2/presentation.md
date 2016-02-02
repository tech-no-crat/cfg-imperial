class: middle, center

# Session 2: CSS and Version Control
CodeFirst: Girls

---

# Goals
- Recap
- CSS Basics
- Selectors and attributes
- **Worksheet chapters 1-2**
- Version Control
- Github
- **Use github to upload your website!** 

[Worksheet link](/cfg/session2/worksheet.pdf)

---
class: middle, center

# Recap

---

**Structure of an HTML document:**

```html
<!DOCTYPE html>
    <head>
      <!-- nothing written in the head section will show up when you open your browser, also this is a comment -->
    </head>
    <body>
      <p> Everything that is written here will appear on your screen when you open the file in a browser. </p>
    </body>
  </html>
```

---

**Things to remember:**

- The last tag open is the first one you must close
- There are paired tags such as `<p> hello </p>` and unpaired tags such as `<br> or <hr>`
- Make sure to indent your code properly 
- Always name the main page of your website index.html 
- Keep your code as clean as possible as in real life other people will read it and they need to understand what you did
- Sometimes that person could be you! 
- Just ignore the notification to buy Sublime 

**Plus:** a useful link - [HTML validator](http://validator.w3.org/#validate_by_input)

---

# Additional Resources 

- [HTML Color Picker](http://www.w3schools.com/colors/colors_picker.asp)
- [CSS Tricks](https://css-tricks.com/how-css-selectors-work/)
- [Flat UI Colors](http://flatuicolors.com)
- [Flat UI Color Picker](http://www.flatuicolorpicker.com/all)
- [Verify CSS](http://jigsaw.w3.org/css-validator/#validate_by_input)

---
class: middle, center

# CSS Introduction

---
# CSS Introduction

* CSS is a language that allows us to format and style an HTML document.
* **HTML defines the content of a document**
* **CSS defines the formatting of a document**

---

Three ways to include CSS in an HTML file
1. Inline in an HTML tag:
```html
<a href='http://w3.org' style='color: red; font-style: italic;' > W3C </a>
```

2. In a `<style>` tag in the `<head>` section of the html document.
```html
<html>
	<head>
		<style>
			a {
				color: red;
				font-style: italic;
			}
		</style>
	<head>
	<body>
		<a href='http://w3.org'>W3C</a>
	</body>
</html>
```

3. Link to a seperate .css file in the head with the `link` tag.
```html
<link rel='stylesheet' type='text/css' href='my_stylesheet.css'>
```
	This loads a file `my_stylesheet.css` located at the same directory.

---

# Writing CSS

CSS a made up of *rule-sets*. 

```css
a {
	color: red;
}

h1 {
	font-size: 18px;
	font-syle: italic;
}
```
This defines two *rule-sets*:

1. One that applies to all hyperlinks, and makes them red.
2. One that applies to all `h1` titles, and makes them 18 pixels big and italic.

The `h1` and `a` above are called *CSS selectors*. The part inside the `{` `}` is called the *declaration block* of the *rule-set*, and contains the *declarations*. Each declaration has a *property* and a *value* seperated by a colon (`:`), and must end with a semicolon (`;`).

Like with HTML, whitespace and indentation doesn't matter, but aids in code readbility.

---

# Some CSS properties:

*	`font-size`
* `border`
* `text-align`
* `color`
* `background`
* `margin` and `padding`
* `width` and `height`
* `list-style`
* `cursor`
* `position`
* ... and many, many others. A complete reference is available [here](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference).

Many of these properties take values in various formats or units. You can't learn them all by heart, use the reference!

CSS concepts:
* **The CSS box model**.
* CSS positioning.
* Animations.
* Colors.

---

# CSS Selectors

* Most of the times, we'd like to be more specific and apply CSS declarations only to a *subset* of tags.
	* i.e. A cancel `<button>` should be styled differently than a `submit` button.
* We can use the **ID** and **class** selectors for this purpose:
```html
<button class='dangerous'>Cancel</button>
<button class='success'>Submit</button>
```
```css
button.dangerous {
		/* rules to make our button red here */
}
button.success {
		/* rules to make our button green here */
}
```

---
# CSS Selectors

* The ID selector is similar, but usually only one element with a certain ID should exist in a webpage:
```html
<h1 id='main-title'>Welcome to my homepage</h1>
```
```css
h1#main-title {
		text-align: center;
}
```

---
class: middle, center

# Chrome Developer Tools Demo

---
class: middle, center

# What CSS sometimes feels like

![css](https://media.giphy.com/media/xTiTntxRyKDjRFMVqw/giphy.gif)

---
class: middle, center

# Please go through chapters 1 and 2 of today's worksheet

---

class: middle, center

# Version Control and Git
![Version Control](http://www.datamation.com/imagesvr_ce/3829/version-control.jpg)

---

# Why do we need version control?

Imagine working on a website with a group of people. As your code base grows bigger, you will have problems:

- How do you work on the same files, at the same time?
- How do you make sure that your changes do not affect what everybody else is working on?
- How do you track what everybody else has been doing, without reading all their code?
- How do you revert to previous versions?

--

Google docs and dropbox (shared folders) do not solve all these problems well enough. **Do not send code over facebook or email**, as this gets very messy very quickly.

**Version control**, in its simplest form, is a program that records changes to a set of files over time.

**Git** is a very popular version control system, mainly used for code and software engineering. Other VCSs are Mercurial, CVS and SVN.
---
class: middle, center

![Torvalds](http://rhoit.com/talks/phpmeetX/img/meme/torvalds.jpg)

---
## Git concepts

- **Repository**: A single project. Contains source files (HTML, CSS, Javascript), images, anything that your project needs. Resides in a remote server.
- **Commit**: A set of changes to some files. Comes with a *commit message*, the short verbal description of the changes (i.e. "Styling the header").
- **Pull/Push**: The operation of downloading/uploading a set of commits from/to a remote server.
- **Branches**: An ordered series of commits, usually related to a specific feature or person. Branches can *branch off* other branches and be **merged** together into a single branch.
- **Github**: A git repository hosting service. Stores your code in their servers, and also lets you publish your website.

![git-branches](images/git-branches.png)

---
# A simple git workflow

1. **Pull** the latest changes.
2. **Make some changes** and test that they are working correctly.
3. **Commit** and give a **descriptive message** of what you did. Remember to **commit often**!
4. **Push** to the remote server. You might have to pull before pushing and perform a **merge**.

![git-commits](http://imgs.xkcd.com/comics/git_commit.png)
---
class: middle, center

# Github demo

---
# Github pages

* Github allows you to host static websites in their platform.
* Create a branch `gh-pages` in any repository containing an `index.html` file.
* Push and you are done!

(More detailed instructions in the worksheet)
---
class: middle, center

# Please go through the rest of week's two worksheet.
