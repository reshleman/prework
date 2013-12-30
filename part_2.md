# Part 2

Your first step into learning web development is to learn HTML. HTML stands for
HyperText Markup Language and while this sounds like a complicated term it’s a
very simple way for you to create web pages. The term HyperText means that you
have a collection of documents with “hyperlinks” between the documents. When
talking about web pages, these “hyperlinks” are the links you click on a page to
get to a different page. A markup language is a way to annotate a document to
provide it with formatting like bold or italic text. So altogether we have pages
or “documents” that we can markup and link together. Here is a very simple HTML
example.

    <p>A paragraph with <b>bold</b> and <i>italic text</i></p>

The first thing to notice in the HTML above are the tags. A tag in HTML starts
with `<` and ends with `>`. At the beginning of our HTML we have `<p>` which is
known as a paragraph tag. We know this because it has a `p` between the `<` and
`>`. A tag’s type is always determined by the text at the start of the tag - for
instance we also have a `<b>` or “bold” tag and a `<i>` or “italic” tag.

Aside from the tags we’ve mentioned, you’ll note that there are tags that
include a `/` at the beginning of the tag. These are known as closing tags and
they tell the browser to stop formatting the text according to that tag. This
allows us to stop bolding the text after the word “bold”. Similarly we do the
same thing with the italic tag and paragraph tag.

You will find that while most HTML tags contain both an open and close tag, some
tags will not:

    <p>This paragraph has a newline or “break”<br>Inside of it</p>

Tags that only have an open tag typically are used for creating one-off elements
on the page, like the `<br>` tag which will break up lines of text.

Let’s create a simple page using what we’ve learned so far. Within the
`metis_prework` directory you created in [Part 1][part_1], create a file called
`index.html` and add the following text to it:

    <p>A <b>photo</b> gallery application</p>

When you open this in the browser, either by double-clicking on the `index.html`
file or dragging it on top of your browser, you should see a paragraph with the
text “photo” bolded. Now that you’ve written an HTML page see if you can
recreate the following pages within the `metis_prework` directory:

    filename: paragraphs.html
    requirements: Do not use a break tag.

![paragraphs.html][paragraphs_html]

    filename: breaks.html
    requirements: Only use one paragraph tag

![breaks.html][breaks_html]

Congratulations on making your first HTML pages! Take a look in a browser to
make sure everything came out as expected. If everything looks good, ensure you
are in the correct directory, and commit these to GitHub:

    git add index.html paragraphs.html breaks.html
    git commit -m ”My first pages.”
    git push origin master

## Structuring an HTML document

While the browser has rendered our pages correctly, our HTML pages are actually
incomplete. The browser will typically try to “fix” our pages for us which is
why we’re able to see the content. If we want to make valid pages, we need to
add a bit more information about our document. Looking back at our first
example, a valid HTML page might look something like this:

    <!DOCTYPE html>
    <!-- A gallery page -->
    <html>
      <head>
        <meta charset="UTF-8">
        <title>My Web Gallery</title>
      </head>
      <body>
        <p>A <b>photo</b> gallery application</p>
      </body>
    </html>

Let’s review this line by line:

`<!DOCTYPE html>`: This is a special tag. The `!` at the beginning of the tag tells
our browser that it is not part of the document, but is instead a special
instruction to the browser. The instruction we’re providing is the `DOCTYPE`. The
`DOCTYPE` tells the browser which version of HTML we are using. We’re only
concerned with HTML5 which is the latest version of HTML and in order to use
HTML5 we just add the word “html” after the `DOCTYPE`.

`<!-- A gallery page ->`: This is another special tag. Again this is a special
instruction, but this time the `--` means we’re writing a comment. A comment has
no effect on the page but can provide you with additional information about its
surroundings.

`<html>`: This tag starts our document. Aside from the `DOCTYPE` tag or any other
comments, every tag goes inside of this.

`<head>`: This tag contains information related to our page. The browser will not
render anything inside of the head tag on the page so you should make sure not
to put tags like `<p>` or `<b>` inside of it.

`<meta charset="UTF-8">`: The meta tag provides data about the document to the
browser or other programs that may read your code, such as a search engine. The
charset metadata will tell the program what character encoding you are using. In
this case, we are using UTF-8, or Unicode, a character set that allows you to
use letters from languages around the world and other various symbols.

`<title>`: This tag describes the title of the page. The browser will typically
show you the title at the top of the browser or on the page’s tab.

`</head>`: Closing the head tag.

`<body>`: This tag contains the content of our page. The browser is supposed to
render everything that is inside of the `<body>` tag. Here is where we want to put
our `<p>` and `<b>` tags

`<p>A <b>photo</b> gallery application</p>`: Our content from before.

`</body>`: Closing the body tag.

`</html>`: Closing the html tag.

Change your `index.html` file to look like the above HTML. Also make these changes
to the `breaks.html` and `paragraphs.html` files, but make sure not to lose the
content that was already in those files. After you’ve changed all of the files
commit them to GitHub.

    git add index.html breaks.html paragraphs.html
    git commit -m ”Using proper HTML”
    git push origin master

You’ll notice that when using Git, you will use this workflow a lot: make a
small change, add the files, commit them, and then push them to a remote
repository. For additional Git practice, you can try http://try.github.io/.

## Moving on

If you feel comfortable with everything you learned in Part 2, please move on to
[Part 3][part_3].

[part_1]: part_1.md
[paragraphs_html]: images/paragraphs_html.png
[breaks_html]: images/breaks_html.png
[part_3]: part_3.md
