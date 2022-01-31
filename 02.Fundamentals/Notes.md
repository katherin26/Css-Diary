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
