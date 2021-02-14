---
title: Introducing Markdown: The Plain-Text Writer's Power Tool
layout: post
theme: midnight
tags: plain-text, plain, text, writing, markdown, minimalism, computer. computing
---

##Introducing Markdown, the Plain-Text Writer's Power Tool

Everybody's familiar with the usual way of formatting text in a traditional word processor, but have you stopped to think about how laborious the process normally is?

If you want to make a word italic, your hands come off the keyboard and one hand moves to the mouse. Using the mouse, you click and drag the cursor over a word (or double-click on the word) to highlight it, then move the mouse cursor up to the top of the screen to click on the "italicize" button along the toobar. To create a footnote, your hands again leave the keyboard, you move your mouse cursor up to an "insert" pull-down menu, select "footnote," which brings you down to the bottom of your page. You type the footnote, then scroll back up to where you were originally working in your document. Not a big deal once or twice, but such operations, when repeated over and over, actually consume a lot of time and break the flow of your thinking.

What if there were a way to perform all those operations as you go, simply by typing normal keyboard characters? Your hands would never leave the keyboard, and the mechanics of your software wouldn't interrupt your train of thought.

This is where Markdown Syntax is a godsend.

Markdown syntax is simply a set of textual conventions, using standard keyboard characters, that indicate various kinds of formatting you want in your final output. Here are some of the basic conventions:

>    # Markdown Syntax:
>    ## Hashtags indicate headings
>    ## One for a level-one heading, two for level two, etc.

A string of three or more asterisks, like this:

>    ***

Indicates a horizontal rule.

>    *An asterisk on either side of a word or phrase indicates italics*
>    **Two asterisks on either side of a word or phrase indicates boldface**
>    **Three asterisks indicate both boldface and italics***

You can use hyphens to indicate a bullet list:

>    - Like this
>    - And this
>    - And this
>        - To create another level to your list,
>        - simply indent the hyphen four spaces.

Indicate numbered lists as you'd expect, with numbers:

>    1. Like this
>    2. And this
>    3. And this

If you'd like to create a hyperlink, simply enclose the link text in brackets, followed by the link itself in parenthesis, like so:

> [This is the link to my blog](https://unvarnishedgeek.github.io).

You can indent a quotation by using a "greater than" symbol, like this

>    >Putting a "greater than sign at the front of a paragraph of text will indent the whole thing as a nice block quote.

    There are a couple of ways of doing footnotes. We'll explore two eventually, but the first way is to enclose a caret and a "name" or number for the note inside square brackets, 

Then, at the bottom of the document, you create the note itself like this:

 >   [^1]: Here's our actual footnote.

Here's the magic. When you type a plain-text document using markdown syntax, it looks like this above. Once you're done composing, however, you run your file through another piece of software that interprets your markdown and uses it to format a final document in the form of your choice, be it a word file (.docx), a PDF file (.pdf), a Libre/OpenOffice file (.odt) or a web page (.html).

For example, I can convert the mardown example above into html to incorporate it into this log page, and it looks like this:

***

# Markdown Syntax:

## Hashtags indicate headings

## One for a level-one heading, two for level two, etc.

A string of three or more asterisks, like this:

***

***

Indicates a horizontal rule.

*An asterisk on either side of a word or phrase indicates italics*

**Two asterisks on either side of a word or phrase indicates boldface**

**Three asterisks indicate both boldface and italics***

You can use hyphens to indicate a bullet list:

- Like this
- And this
- And this
    - To create another level to your list,
    - simply indent the hyphen four spaces.

Indicate numbered lists as you'd expect, with numbers:

1. Like this
2. And this
3. And this

If you'd like to create a hyperlink, simply enclose the link text in brackets, followed by the link itself in parenthesis, like so:

[This is the link to my blog](https://unvarnishedgeek.github.io)
You can indent a quotation by using a "greater than" symbol, like this:

>Putting a "greater than sign at the front of a paragraph of text will indent the whole thing as a nice block quote.

There are a couple of ways of doing footnotes. We'll explore two eventually, but the first way is to enclose a caret and a "name" or number for the note inside square brackets, like this.[^1]

Then, at the bottom of the document, you create the note itself like this:

[^1]: Here's our actual footnote.

***

Pretty sweet, huh? The beauty of this system is that all of your basic formatting happens in the plain text format, in a way that makes all your formatting choices perfectly visible and unmistakeable, and right in line with your prose. Including the formatting, then, neither interrupts the flow of your thinking or inserts hidden code that can mess with your formatting later on. When you edit your prose, the formatting naturally moves with it, overtly, as opposed to all that messy underlying code in a regular word processor that seems to bent on destroying both your formatting and your sanity.

So here's a five-minute practice assignment to get you started with using Markdown:

- Fire up the text editor of your choice
- Using the above formatting as a guide, do a little of your normal daily writing (some freewriting or journaling, some notes, an email draft, etc.) using markdown syntax for formatting.
- You can find an even more comprehensive guide to Markdown syntax [here](https://help/github.com/articles/markdown-basics/).

That's it for this installment! Have fun experimenting with the syntax, and note how much word processor fussiness it removes from your writing process. In the next installment, I'll show you how to convert your markdown documents into beautifully formatted Word, LibreOffice, or PDF documents.
