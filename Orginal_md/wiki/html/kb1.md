[<--Home](README.md)
# Chapter 01: The Basics

The Page you are viewing right now is an HTML document. HTML documents look a lot like word-processing documents...

You can have bold and italicized, Larger and Smaller, or it could look type-written.

Of course, the HTML code for this can look confusing...

You can have <b>bold</b> and <i>italicized</i>, <font size=+2>Larger</font> and <font size=-2>Smaller</font>, or it could look <tt>type-written</tt>. 

So what are all these "<" and ">" things doing here? When you place a certain thing within these you are making something known as a tag. For example the `<b>` tag is saying to start bold text, and the `</b>` tag is saying to stop bold text. The tag with the slash (/) is known as the closing tag. Many opening tags require a following closing tag, but not all do. Tags make up the entire structure of an HTML document.

`‌<b>This Text is Bold</b>
^^^--Opening Tag    ^^^^--Closing Tag`

Here are two pieces of HTML code, the second of the two has an error in it, what is it?

#1 - Bob jumped OVER the fence.
#1 - Bob jumped <b>OVER</b> the fence.
#2 - Bob jumped UNDER the fence.
#2 - Bob jumped <b>UNDER<b> the fence.

You should have noticed that the second code is missing a slash (/) in the tag after the word UNDER, which causes the web browser to interpret the code as leaving the bold face on! This is a common error, so be careful of it!

**Note: Tags in HTML are NOT case sensitive. For example... <title> and <TitLE> both mean the same thing and are interpreted as being the same.**

**Document Structure...**

HTML files are just normal text files... they usually have the extension of .htm, .html, or .shtml. HTML documents have two (2) parts, the head and the body. The body is the larger part of the document, as the body of a letter you would write to a friend would be. The head of the document contains the document's title and similar information, and the body contains most everything else.

Example of basic HTML document Structure...

`<html>
<head><title>Title goes here</title></head>
<body>Body goes here</body>
</html>
`
You may find it easier to read if you add extra blank lines such as follows...

`<html>

<head>
<title>Title goes here</title>
</head>
<body>
Body goes here
</body>
</html>
`
Note: Extra spaces and line breaks (blank lines) will be ignored when the HTML is interpreted... so add them if you wish to do so.

Whatever falls between the TITLE tags will be the title of the document, when the page is viewed it is usually found in the title bar at the top of the screen. [Note: You may NOT use other tags within the TITLE tags (Example: You cannot have the code read: <title><b>title goes here</b></title>.]

Example of how titles are viewed...

In Netscape Navigator...
Netscape - [Title goes here] OR Title goes here - Netscape [depending on version]

In Microsoft Internet Explorer...
Title goes here - Microsoft Internet Explorer

Whatever you place between the BODY tags will fall into the major area of the document window, and therefore it is the largest part of your HTML document.


Your own HTML page...

To begin writing your own HTML page, type the following into a new text file:
<html>
<head><title>My Home Page</title></head>
<body>
</body>
</html>

Save the text file as "Home.htm".

[Chapter 02](kb2.md)





