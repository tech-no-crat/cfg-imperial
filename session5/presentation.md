class: middle, center

# Session 5: Recap
CodeFirst: Girls

---

# Goals
- HTML
- CSS
- Git
- Bootstrap

---
class: middle, center

# Recap

---
class: middle, center

# HTML

---
# What is HTML?
* The standard markup language to define how webpages look, initially released in 1993.
* A webpage is made up of HTML tags, for example:
  * `<h1>CubeSat</h1>` - Header (title)
  * `<img src='images/tesla.jpg' alt='Tesla Model S' />` - an image
  * `<a href='https://cubesat.ic.ac.uk'>Imperial Cubesat</a>` - a link
  * `<p> <a href='http://google.com/'>Best search engine</a></p>` A link within a paragraph. An HTML tag can contain other HTML tags inside it, said to be its "children".
* Good HTML is **semantic** (reinforces the meaning of the information), but does not describe how the webpage will look.

---
## HTML Example

```html
  <!DOCTYPE html>
  <html>
  <head>
    <title>Example HTML Page</title>
  </head>
  <body>
    <header class='main'>
      <h1>This is an example HTML page</h1>
    </header>
    <section>
      <span class='acronym'>HTML</span> is <em>wonderful</em>.
      Here's a link to <a href='https://google.com'>google</a>
    </section>
  </body>
  </html>
```


---
class: middle, center

# CSS

---

# What is CSS?

* A language used to define how a webpage should look. 
* CSS aims to separate appearance detail from content.
  * Easier to read
  * Easier to share style
  * Permits hierachy of styles

---
```html
<!DOCTYPE html>
    <head>
      <link rel='stylesheet' type='text/css' href='my_stylesheet.css'>
    </head>
    <body>
      <h1> Affected by the css since we're styling h1 there. </h1>
      <p class='spicy'> Text with some zing </p>
      <p id='mission'> a specific thing </p>
      <p id='mission' class='spicy'> what will happen here? </p>
    </body>
  </html>
```
my_stylesheet.css
```css
.spicy {
    color: red;
}

#mission {
    color : blue;
}

h1 {
    font-size: 18px;
    font-syle: italic;
}
```
---
class: middle, center

# Twitter Bootstrap

---

# What is Bootstrap?

* A library of open-source stylesheets 

---
# Why Bootstrap?

* Use someone elses stylesheets to make your life easier
* Makes responsive web-pages easy
* Makes delivery of mobile content easy
* You can add your own stylesheet files to extend bootstrap or override it's default behaviour

---

