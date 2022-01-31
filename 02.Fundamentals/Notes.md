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
