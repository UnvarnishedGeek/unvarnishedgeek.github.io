---
layout: post
title: "Plain-Text Writing Lesson: Detangling Your Footnotes"
date: 2021-08-17
categories: writing plaintext pandoc markdown howto footnotes
theme: midnight
---

## Plain-Text Writing Lesson: Detangling Your Footnotes

>*Note: This is the fifth installment in a series of brief lessons on writing with plain text tools, such as basic text editors, Markdown syntax, and Pandoc. The lessons are designed with the non-techy in mind, and are meant to take about 5-10 minutes apiece to digest. If you're unfamiliar with plain-text tools, I recommend that you begin with [this introduction](https://unvarnishedgeek.github.io/2020/11/25/plain-text-one.html).*

### Footnote Foofaraw

Now that we've got the basics of plain-text writing, using markdown syntax, and invoking pandoc for formatting, let's tackle one of the more complex bugbears of writing, especially for academic writers: footnotes.

If you're accustomed to using a traditional word processor such as Word or LibreOffice Writer, you're aware that the initial steps for including footnotes are pretty easy: select "footnote" from an "insert" menu or hit a keyboard shortcut, an auto-numbered note shows up at the bottom of the page, and you type happily away (or insert a note or placeholder code from a citation manager like Zotero or Endnote). Easy peasy.

As you've likely experienced if you've done a lot of heavily-footnoted writing, however, the problem isn't about adding the notes initially; it's about maintaining their continuity and formatting down the line. This isn't such a big deal for shorter-form writing (like blog posts), but it can be a very big deal indeed for longer, more in-depth work, such as articles and book chapters. The problem is that those longer pieces tend to travel a great deal before reaching their final (published) destinations: they go back and forth between writers, peers, peer-reviewers, editors, publishers, etc. As with all of the complex coding that underlies a word processor document, irregularities have a way of creeping in as the document is continually emailed, opened under different platforms or tools, edited and modified, etc. This process can turn those easily-added footnotes into a nightmare: if you've ever had the problem of suddenly finding that your notes are out of sequence, or that the formatting has suddenly changed and no change in settings seems to bring them back into order, you know what I'm talking about.

### Markdown and Pandoc to the Rescue, Again

What's handy about Markdown here is basically the same principle outlined in [this article](https://unvarnishedgeek.github.io/2021/02/14/plain-text-two.html): You keep your original document in a kind of "raw" format in which everything is consistent, and then use Pandoc to turn that universal format into any other format an editor, publisher, or friend might require. In this way, your preferred formatting, and the position and style of your footnotes, is essentially always preserved in a consistent state in your original markdown document. Changes can be made easily in that Markdown document without any possibility of unintentionally adding code that will affect your formatting down the line. In other words, using Markdown and Pandoc together can mean that you'll never again need to tear your hair out when your notes go haywire.

### The How-To Bit

There are two different ways to create footnotes using Markdown. The first is entirely native to Markdown, and is ideal for shorter-form writing for the web (i.e. blog posts). The second requires Pandoc, but is ideal for longer-form writing where maintaining the consistency of many footnotes is important.

**The Markdown Way**

To create a basic Markdown footnote, place your cursor where you want the footnote to appear in your text and start with an open bracket, followed by a caret, a footnote name or number, and a close bracket, like this:

```
[^1]
``` 

Then, at the bottom of your main text, place the same sequence of characters again, followed by a colon, a space, and then the text of your note:

```
[^1]: Here is the text of the footnote.
```

In the final document, markdown will create a footnote at the bottom of your text that includes a link back to the in-text footnote marker, like this.[^1]

This sort of footnote is excellent for web-oriented writing, since it assumes a contiguous text (i.e. no page breaks) and provides an easy way for readers to click back and forth between the superscript note indicators in the text and the notes themselves at the bottom.

However, it's not difficult to see how these footnotes can become unwieldy with longer, more print-oriented documents with many footnotes. For one thing, creating them would mean constantly scrolling up and down your ever-expanding main text. For another, adding footnotes would mean manually re-numbering every note that comes after the newly added one. Talk about a pain!

**Inline Footnotes in Pandoc**

Luckily, we're not stuck with native Markdown footnotes if we have Pandoc, which was introduced in [this article](https://unvarnishedgeek.github.io/writing/plaintext/pandoc/markdown/howto/2021/02/06/pandoc-magic.html) 

Pandoc allows us to create inline footnotes, which are much more convenient for print-oriented writing that utilizes numerous notes and citations. To create an inline footnote, one simply places a caret at the point one wishes the superscript footnote indicator to appear, follow by the content of the note in brackets, thus:

```
##Using In-Line Footnotes with Pandoc

Here is my main text, rolling along and expressing its usual brilliance, followed by an inline footnote.^[Footnotes are cool.] As I continue to write, I can place additional footnotes using the same format.^[Cool like bow ties and fezzes]
```

When I run this through Pandoc, using the procedure outlined in the article linked above, and open the resulting formatted text in a word processor (LibreOffice in this case), I get this result:

![First note sample!](/assets/test1.png)


Note that Pandoc has automatically formatted and numbered the inline notes. It gets better. Let's say I need to add a sentence to the above text that requires an additional note between the two initial ones, like this:

```
##Using In-line Footnotes with Pandoc

Here is my main text, rolling along and expressing its usual brilliance, followed by an inline footnote.^[Footnotes are cool.] I might even need to add a sentence that needs its own note later on.^[No, I'm not a *Doctor Who* fan. Why do you ask?] As I continue to write, I can place additional footnotes using the same format.^[Cool like bow ties and fezzes.]
```
Here's the new output from Pandoc:

![Second note sample!](/assets/test2.png)

Notice that Pandoc has inserted the new note and automatically renumbered the other notes to accomodate my addition.

The value of creating notes this way for longer, more heavily-annotated documents should be apparent: instead of dealing with an "insert note" function at all, one simply creates all one's footnotes right in line with the text, keeping the flow of thought contiguous and avoiding unecessary keyboard commands. No matter how much the plain-text document is edited, and no matter how many notes are added or deleted in that process, running the plain-text document through Pandoc again will always renumber footnotes automatically, meaning that the output from Pandoc will always be a "fresh" word processor document, with all the formatting and numbering of notes perfectly consistent. No more fiddling around with footnotes that seem to have a mind of their own.

There can be even more flexibility when inline notes are used with a citation manager, which we'll tackle in a future lesson.

For now, your five-minute assignment is to create a sample document with both native markdown and Pandoc inline footnotes (if you don't remember how to use Pandoc, [refer back to my article on Pandoc](https://unvarnishedgeek.github.io/writing/plaintext/pandoc/markdown/howto/2021/02/06/pandoc-magic.html). Or, better yet, try out the note functionality in some of your normal writing.

[^1]: Click on the arrow at the end of this note to return to the note's position in the main text. 

