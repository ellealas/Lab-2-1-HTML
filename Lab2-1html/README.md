Lab 1 - HTML
The goal of this lab is to help you familiarize with HTML tags, their properties and usages.
Completing the steps would require searching the answers on the Internet, which is the bread and butter of a software developer’s life. 

TIP: try to learn keyboard shortcuts as you progress with this exercise - shortcuts can greatly simplify a web developer’s life.

I. Template and HTTP server
Template contains a skeleton for your website that uses semantic HTML. 
There are two files index.html and form.html because we'll be creating two separate pages and then linking them together using <a> tags.
Assets, like images, audio and video that you'll be using are to be found in the assets directory.
Steps:
    1. Take a look at the template
    2. Start http-server in the current directory by typing
    ```
        npx http-server .
    ```
    3. Visit the address printed in the console in the web browser
        3.1 try localhost:8080
        3.1 try localhost:8080/form

II. HTML elements - metadata
In this section you'll be editing the index.html file
Steps:
1. Add a title in the head section of your page. Use the HTML title tag.
2. Add metatags in the head section of your page. Use HTML meta tags.
  - charset
  - description
  - keywords
  - author
  - viewport


III. HTML elements - div, span, p, pre, ul, li, ol, article
Steps:
1. Add 3 divs next to each other at the beginning of the body section and put some distinctive content into each of the div,  e.g.
```
    <div>avocado</div>
    <div>kiwi</div>
    <div>banana</div>
```
2. Below divs add 3 spans next to each other and put some distinctive content into each span
Observe the difference between block and inline elements.

TIP: In VSCode, you can press ctrl+shift+i to auto-format the code. VSCode won't auto-format if code is invalid - tags are improperly closed or nested.


3. Below, add p and pre tags into your HTML body and copy the contents below into them
```
<p>
p represents paragraph
</p>
<pre>
Text in         a pre element
is displayed in a fixed-width
font, and it preserves
both      spaces and
line breaks
</pre>
```
Observe how <pre> tag preserves the structure of the text inside, while the p tag collapses spaces and newlines.
7. Add an unordered list to your page using ul and li tags
8. Add an ordered list to your page using ol and li tags
9. Wrap all the elements you've created with an article tag
```
<article>
   <!-- Content added in previous points -->
</article>
```
10. Add a page headline - add an h1 tag above article with any content, e.g. "My HTML learning journey"
11. Add article headline - add an h2 tag within an article tag with any content, e.g. "Learning elements - div, span, p, pre, ul, li, ol, article".
Consider the difference between page headline and article headline.

IV. HTML elements - Tables - table, thead, tbody, tr, td, th
1. Start by adding another article below the first one, add h2 tag inside this newly created article.
2. Search the web for HTML table and copy code you can find, e.g. from the Mozilla website:
```
<table>
    <thead>
    <tr>
        <th>First header</th>
        <th>Second header</th>
    </tr>
    </thead>
    <tbody>
        <tr>
            <td>First cell - first row</td>
            <td>Second cell - first row</td>
        </tr>
    </tbody>
</table>
```
4. Create another row by copying tr tag together with its children below the first row.
5. By default tables don't have any styles, add styling by copying code below to the head section of the page
```
<style>
    table, th, td {
        border: 1px solid black;
    }
</style>
```
6. Add a third cell inside one of the rows. Observe how the table lost its shape.
Tables must be m rows by n columns and violating this rule will cause your table to lose shape.
```
    <td>Third cell - first row</td>
```
6. Fix the table by adding missing td tag
7. Now the header is missing for the third column, we'll fix that by adding `colspan="2"` attribute
to the first th tag to make it span two columns.
8. Add third row to the table and add `rowspan="2"` attribute to one of the td tags above and observe what happens 
```
    <tr>
        <td>First cell - third row</td>
        <td>Second cell - third row</td>
    </tr>
```
V. HTML elements - img, video, audio
Steps:
1. Add an image to your website. Here we're using an image provided from the external service, picsum.


<img src="https://picsum.photos/200/300" alt="" />

2. Add video
```
<video controls width="250">
    <source src="/media/cc0-videos/flower.webm"
            type="video/webm">
    <source src="/media/cc0-videos/flower.mp4"
            type="video/mp4">
    Sorry, your browser doesn't support embedded videos.
</video>
```

3. Add audio element
```
<audio
    controls
    src="/media/cc0-audio/t-rex-roar.mp3">
        Your browser does not support the
        <code>audio</code> element.
</audio>
```
4. Try removing the controls attribute and adding autoplay attribute to both audio and video tags


VI. HTML elements - Forms - form, input, label, select, option, button
In this section you'll be editing the form.html file
You can access this file at http://localhost:8080/form - you usually skip .html extension in URLs.
Steps:
1. Open form.html file
2. Add a form using <form> tag like this
```
    <form method="POST" action="http://localhost:3000/profile">
    </form>
```
3. Inside the form, add 2 inputs - one for inputting first name and the second one for inputting last name.
    Remember about adding labels for each input. 
    Wrap inputs together with labels using divs to layer inputs one below another.
4. Add radio button using <input type="radio" ...>, remember to label the inputs and add name and value attributes
5. Add checkboxes using <input type="checkbox" ...>, remember to label the inputs and add name and value attributes
6. Add select element to your form using <select> and <option> tags, remember to label the select and add name to your select.
You should also add value for each of the available options.
7. Add submit button at the end of the form
```
    <button type="submit">Submit form</button>
```

VII. Adding a link from a Home to a Form page
In this section you'll extend a navigation bar so users can navigate from Home to Form page
by clicking a link in the navigation bar.
1. Add another <a> element inside of the <nav> tag in both index.html and form.html. 
2. Notice the difference between adding
```
    <a href="./form">Form</a>
```
and
```
    <a href="/form">Form</a>
```

VIII. Inspecting the HTML
In this section you'll inspect the HTML that you've written on the page.

1. Use inspection tool - open developer console and select inspection tool from the top left corner.
2. Select various elements on your website using inspection tool
3. Take a look at the CSS in the "Styles" subtab ("Elements" tab - opens automatically after selecting an element using inspection tool)
    3.1. Try editing CSS styles in the developer console. For example you may try adding following values:
```
    margin: 20px;
    color: blue;
    font-size: 24px;
```
Take a look at the screenshot and use element.style {} to add new styles to selected HTML elements.

