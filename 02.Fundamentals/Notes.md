# **HTML (HYPERTEXT MARKUP LANGUAGE)**

1. HTML in a markup language that defines the structures of a web page. It is interpreted by your web browser
   (Safari,Google,Chrome,Firefox,etc.) in order to display content on your screen.

2. Let's get started by writing a simple HTML file!.

```
<!DOCTYPE html>'
<html lang="en">
        <head>
            <title>Hello!</title>
        </head>
        <body>
            Hello, world!!
        </body>
</html>
```

3. When we open up this file in our browser, we get:

```
Hello, world!!
```

4. Now, let's take some time to talk about the file we just wrote, which seems to be pretty complicated for such a simple page.

   In the first line, we are declaring (to the web browser) that we are writing the document in the latest version of HTML:HTML5.

   After that, the page consists of nested HTML elements (such as html and body), each with an opening and closing tag marked with either **<element>** for an opening and **</element>** for a closing.

   Notice how each of the inner elements is indented just a bit further than the last. While this is not necessarily required by the browser, it will be very helpful to keep this up in your own code.

   HTML elements can inlude **attributes**, which give the browser extra information about the element. For example, when we include **lang="en"** in our initial tag, we are telling the browser that we are using English as our primary language.

   Inside the HTML element, we tipically want to include both a **head** and a **body** tag. The head element will include information about your page that is not necessarily displayed, and the body element will contain what is actually visible to users who visit the site.

   Within the head, we have included a **title** for our webpage, which you'll notice is displayed in the tab at the top of our web browser.

   Finally, we've included the text "**Hello,World!**" in the body, which is the visible part of our page.

# **DOCUMENT OBJECT MODEL (DOM)**

1. The DOM is a convenient way of visualizing the way HTML elements relate to each other using a tree-like structure.

## **More HTML Elements**

1. The are many HTML elements you may want to use to customize your page, including heandings, lists, and bolded sections. In this next example, we'll see a few of of these in action.

2. One more thing to note: <!----> gives us a comment in HTML, so we'll use that below to explain some of the elements.

# **CSS (CASCADING STYLE SHEETS)**

1. CSS is used to customize the appearance of a website.
2. While we're just getting, started, we can add a style attribute to any HTML element in order to apply some CSS to it.
3. We change style by altering the CSS properties of an element, writing something like **color:blue** or **text-align:center** .
4. In this example below, we make a slight change to our very first file to give it a colorful heading:

**CSS INLINE**

```
<!DOCTYPE html>
<html lang="en">
    <head>
        <title>Hello!</title>
    </head>
    <body>
        <h1 style="color:blue; text-align:center;"> A colorful Heading!</h1>
        Hello, world!
    </body>
</html>


```

5. If we style an outer element, all of the inner elements automatically take on that style. We can see this if we move the styling we just applied from the header tag to the body tag:

```
<!DOCTYPE html>
<html>
    <head>
       <title>Hello!</title>
    </head>
    <body style="color:blue; text-align:center;">
        <h1> A colorful Heading!!</h1>
        Hello, world!!
    </body>
</html>

```

6. While we can style our web page as we've done above, to achieve better design, we should be able to move our styling away from the individual lines.

One way of doing this is to add your styling between <style> tags in the head. Inside these tags, we write types of elements we want to be style, and the styling we wish to apply to them, For example:

**CSS INSIDE THE STYLE TAG AND THE HEAD TAG**

```
<!DOCTYPE html>
<head>
<html>
    <title>Hello!</title>
    <style>
        h1{
            color:blue;
            text-align:center;
        }
    </style>
    </head>
    <body>
        <h1> A colorful Heading!! </h1>
        Hello world!
    </body>
</html>
```

7. Another way is to include in a <link> element in your head with a link to a styles.css file that contains some styling. This means the HTML file would look like:

**CSS IMPORT WITH LINK TAG**

```
<html lang="en">
  <!DOCTYPE html>
  <head>
      <title>Hello!</title>
      <link rel="stylesheet" href="styles.css">
  </head>
  <body>
      <h1 >A Colorful Heading!</h1>
      Hello, world!
  </body>
  </html>
```

And our file called styles.css would look like:

h1{
color:blue;
text-align:center;
}

And our file called **styles.css** would look like:

```
    h1{
        color:blue;
        text-align: center;
    }

```

# **CSS SELECTORS**

This is good introduction into what are known as CSS selectors. There are many ways to determine which HTML elements you are styling, some of which we'll mention here:

1. **Element type:** This is what we've been doing so far: styling all elements of the sample type.
2. **Id:** Another option is to give our HTML elements an id like to so: `<h1 id="first-header">Hello</h1>` and then applying styling using `#first-header{...}` using the hastag to show that we're searching by id. Importantly, no two elements can have the same id, and no element can have more than one id.
3. **class:** This is similar to id, but a class can be shared by more than one element, and a single element can have more than one class. We add classes to an HTML element like this: `<h1 class="page-text muted">Hello!</h1>` (note that we just added two classes to the element: page-text and muted). We then style based on class using a period instead of a hastag `.muted{...}`.

**SPECIFICITY**

4. Now, we also have to deal with the problem of potentially conflicting CSS. What happens when a header should be red based on its class but blue on its id? CSS has a specificity order that goes:

- In line styling.
- Id.
- Class.
- Element Type.

5. In addition to the comma for multiple selectors, there are several other ways to specify which elements you would like to style. This table from lecture provides a fewm adn we'll go through a few examples below.

```
a, b     === Multiple Element Selector
a b      === Descendant Selector
a > b    === Child Selector
a + b    === Adjacent Sibling Selector
[a-b]    === Attribute Selector
a : b    === Pseudoclass Selector
a :: b   === Pseudoelement Selector
```

**Descendant Selector:** Here, we use the descendant selector to only apply styling to list items found within an unordered list:

```
<!DOCTYPE html>
<html lang="en">
    <head>
        <title>Using Selectors</title>
        <style>
            ul li {
                color: blue;
            }
        </style>
    </head>
    <body>
        <ol>
            <li>foo</li>
            <li> bar
                <ul>
                    <li>hello</li>
                    <li>goodbye</li>
                    <li>hello</li>
                </ul>
            </li>
            <li>baz</li>
        </ol>

    </body>
<html>

```

**Attributes as Selectors**

We can also narrow down our selection based on the attributes we assign to HTML elements using brackets. For example, in the following list of links, we choose to only make the link to Amazon red:

```
<!DOCTYPE html>
<html lang="en">
    <head>
        <title>Using Selectors</title>
        <style>
            a[href="https://www.amazon.com/"] {
                color: red;
            }
        </style>
    </head>
    <body>
        <ol>
            <li><a href="https://www.google.com/">Google</a></li>
            <li><a href="https://www.amazon.com/">Amazon</a> </li>
            <li><a href="https://www.facebook.com/">Facebook</a></li>
        </ol>

    </body>
<html>


```

Not only can we use CSS to change what an element looks like permanently, but also what it looks like under certain conditions. For example, what if we wanted a button to change color when we hover over it? We can acheive whis using a **CSS PSEUDOCLASS**, which provides additional styling during special circumstances. We write this by adding a colon after our selector, and then adding the circumstance after that colon.

**CSS PSEUDOCLASS**

In the case of the button, we would add **:hover** to the button selector to specify the design only when hovering:

```
<!DOCTYPE html>
<html lang="en">
    <head>
        <title>Pseudoclasses</title>
        <style>
            button {
                background-color: red;
                width: 200px;
                height: 50px;
                font-size: 24px;
            }

            button:hover {
                background-color: green;
            }
        </style>
    </head>
    <body>
        <button>Button 1</button>
        <button>Button 2</button>
        <button>Button 3</button>

    </body>
<html>


```

# **RESPONSIVE DESIGN**

**Viewport:** The viewport is part of the screen that is actually visible to the user at any given time. By default, many webpages assume that the viewports is the same on any device, which is what leads to many sites (especially older ones) being difficult to interact with on mobile devices.

One simple way to improve the appearance of a site on a mobile device is to add the following line in the head of our HTML files. This line tells the mobile device to use a viewport that is the same width as that of the device you're using rather than a much larger one.

```
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

**Mediaqueries:** Media queries are ways of changing the style of a page based on how the page is being viewed.

For an example of a media query, let's try to simply change the color of the screen when it shrinks down to a certain size. We signal a media query by typing @media followed by the type of query in parentheses:

```
<style>
            @media (min-width: 600px) {
                body {
                    background-color: red;
                }
            }

            @media (max-width: 599px) {
                body {
                    background-color: blue;
                }
            }
        </style>

```

**FLEXBOX:** This allows us to easily have elements wrap around to the next line if they don't fit horizontally. We do this by putting all of our elements in a div that we'll call our container. We then add some styling to that div specifying that we want to use a flexbox display for the elements inside of it. We've also added some additional styling to the inner divs to better illustrate the wrapping that's ocurring here.

```
<style>
            #container {
                display: flex;
                flex-wrap: wrap;
            }

            #container > div {
                background-color: green;
                font-size: 20px;
                margin: 20px;
                padding: 20px;
                width: 200px;
            }
</style>

```

**Grid:** Another popular way of styling a page is using an HTML grid. In this grid, we can specify style attributes such as column widths and gaps between columns and rows, as demostrated below. Note that when we specify column widths, we say the third one is auto, meaning it should fill the rest of the page.

```
 <style>
            .grid {
                background-color: green;
                display: grid;
                padding: 20px;
                grid-column-gap: 20px;
                grid-row-gap: 10px;
                grid-template-columns: 200px 200px auto;
            }

            .grid-item {
                background-color: white;
                font-size: 20px;
                padding: 20px;
                text-align: center;
            }
</style>

```
