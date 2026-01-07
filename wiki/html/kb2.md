---
layout: default
---

# Chapter 03: More Common Tags

You will often use paragraphs in HTML, just as you do when you write stories. The opening tag for a paragraph is <p>, and the closing tag is </p>. The closing tag for a paragraph is not always needed, but I recommend using it anyway.

Example of a paragraph...

Bob starts to chase the chicken around. Bob trips over a string and goes flying into the pig's mud pit! eww! What a pity!
<p>Bob starts to chase the chicken around. Bob trips over a string and goes flying into the pig's mud pit! eww! What a pity!</p>

Text Formatting Properties...

If you had an entire web page without formatted text, it would look rather dull and boring. This is why we use text formatting tags. Some common text formatting tags are:
<b> and </b> for bold,
<i> and </i> for italics,
<u> and </u> for underlined, and
<tt> and </tt> for typewriter.

Text Formatting Properties...Font Tags

The <font size=n> and </font> tags come in handy.
n is the number of font points by which to change the size of the current font. 
n can be positive or negative: a positive number will increase the font size, and a negative number will decrease it.
n can also be an absolute number, indicating an absolute size for the font (not a relative size).

Example of font tags...

Bob is a Cool Guy isn't he?

<font size=+1>Bob</font> <font size=+2>is</font> <font size=+3>a</font> <font size+2>Cool</font> <font size=+1>Guy</font> isn't <font size=-1>he?</font>

ALIGN attributes...

Many tags support ALIGN attributes... if you want something to be aligned from the left margin, from the center, or from the right margin. The ALIGN attribute is placed in the opening tag before the >.
Left Align
<h1 align=left>Left Align</h1>
Center Align
<h1 align=center>Center Align</h1>
Right Align
<h1 align=right>Right Align</h1>
The Line Break...

When your HTML document is viewed, normally the text will do a word-wrap at the end of a line. If you want to have the text BREAK (go to another line) you will use the <br> tag. This tag has no closing tag.

Example WITHOUT line Break...

Sentence One. Sentence Two. Sentence Three.

Sentence One.
Sentence Two.
Sentence Three.

Example WITH line Break...

Sentence One.
Sentence Two.
Sentence Three.

Sentence One.<br>
Sentence Two.<br>
Sentence Three.<br>
Preformatted Text...

If you wish to have text line up properly (a.k.a. fixed width text) that will include line breaks without the use of the <br> you may find the <pre> and </pre> tags helpful.

Example of text WITHOUT preformatting...

The cat ran after the dog. ^ ^-verb ^noun ^-noun 
 The cat ran after the dog.
    ^   ^-verb        ^noun
    ^-noun

HTML ignores the extra line breaks, so the text does not line up properly.
Example of text WITH preformatting...

The cat ran after the dog.
    ^   ^-verb        ^noun
    ^-noun

 <pre>
The cat ran after the dog.
    ^   ^-verb        ^noun
    ^-noun
</pre>