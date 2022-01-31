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
