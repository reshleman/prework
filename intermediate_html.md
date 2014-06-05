# Intermediate HTML

Previously in our HTML we used a couple of tags: `<p>`, `<b>`, and `<i>`. You
may have noticed that when you use `<p>` tags the content is split up:

    <p>Paragraph 1</p>
    <p>Paragraph 2</p>

![Paragraphs demo][paragraphs_demo]

But when we use tags like `<b>` and `<i>` the content remained on the same line.

    <p><b>Bolded</b> and <i>Italicized</i></p>

![Bolded and Italicized demo][bolded_and_italicized_demo]

The reason this happens is because these tags are of different types - inline
and block.

Block elements are designed to take up as much width as they can. This causes
content that would occur before or after a block level element to be on a
separate line from it.

Inline elements are designed to only take up as much space as they need. This
causes the content to appear “inline” with the elements and content around it.

Before moving on, determine if the following tags are block or inline:

    <h1>
    <h2>
    <div>
    <span>

Let’s add a few of these elements to our page by replacing everything in
between the body tags with:

    <h1>A photo gallery application</h1>
    <div>
    <h2>Galleries</h2>
      <p>There are no galleries here yet.</p>
    </div>

Your page should now look like:

![Gallery Demo][gallery_demo]

## Hyperlinks

Links are the main thing that makes ‘the web’ the web. They are defined with the
inline element `<a>` (an ‘anchor’ tag) and a href attribute, which references the
destination of the link. The content you want linked goes between the opening
`<a>` and closing `</a>` tags and can be anything from a word to an entire segment
of HTML that includes images and text. The href attribute can reference an
absolute path (i.e. from another server) or a path relative to the HTML
document.

    <!-- relative path -->
    <a href=’about.html’>Learn about me!</a>

    <!-- absolute path -->
    <img src=’http://www.example.com/images.html’>

You can also link to email addresses, which will force the browser to open the
link with the specified email address in the computer's default email client. To do
so the href value should start with ‘mailto:’ and be followed by the receiving
email address.

    <a href=’mailto:jsteiner@thoughtbot.com’>Email me</a>

Now that we know how to create a link, let’s add one to the page we created in
[Part 1][part_1]. Before we create a link, let’s be sure we have something to link to.
Since we are creating a photo gallery application, let’s link to a gallery of
cat pictures. In the same directory that you created the file index.html, create
a new file called `cats.html`. Be sure to create the file with the necessary
`<html>`, `<head>`, and `<body>` tags, and a descriptive `<h1>` tag.

Now create a link from `index.html` to `cats.html`. If you click on the link, you
should see the cat page. Your pages should look like:

![Gallery With Link Demo][gallery_with_link_demo]

and

![Cats Demo][cats_demo]

You’ll notice after visiting the cats page the link on the index page will
have turned purple. This is because your browser keeps track of which links you
have visited and makes them purple by default to represent they have been
visited:

![Visited Link Demo][visited_link_demo]

Commit your work and push to GitHub:

    git add index.html cats.html
    git commit -m "Link to cat gallery"
    git push origin master

## Adding Images

In addition to text, HTML allows you to add images to your webpage with the
tag `<img>`. For the `<img>` tag to work, you must specify a `src` attribute
(referred to as the “source”), which tells the browser where it can find your
image. The `src` attribute’s value must be a path. Much like an anchor tag, the
path can be relative to the HTML document or absolute.

    <!-- relative path -->
    <img src=’grumpy-cat.png’>

    <!-- absolute path -->
    <img src=’http://example.com/grumpy-cat.png’>

Be sure that you are using the same file extension as your image. Common image
file types are:

`jpg`: for detailed pictures with lots of colors
`png`: for images with transparent backgrounds
`gif`: for quick loading images with few colors

In addition to the `src` attribute, you should always add `alt` attributes to your
`img` tags. `alt`, which stands for ‘alternative text’, is useful for the following
purposes:

* The image is not available
* Search engines know what the image is
* Browsers for the blind

Let’s add an image to our existing cats gallery page. Download the following
image into the directory you saved index.html to by right clicking it and
selecting `Save as...`. You should be able to use what you’ve learned to get the
image to display on the HTML page. If the image does not display, be sure you
saved the image to the correct folder.

![Grumpy Cat][grumpy_cat]

Your page should now look like:

![Gallery With Grumpy Cat Demo][gallery_with_grumpy_cat_demo]

Commit your work and push to GitHub:

    git add cats.html grumpy-cat.png
    git commit -m "Add image to cat gallery"
    git push origin master

## Viewing Source HTML

It is often useful to inspect your own source code as well as the HTML structure
of other websites. If you are using Chrome, you can right click on any webpage
and click `View Page Source` or find the same menu under `View > Developer >
View Page Source`. Other browsers have similar features that you can find
yourself. Now you can look at the HTML of any webpage on the internet!

## Lists

We now have two pages; an index page and a gallery for cats. Unfortunately, this
leaves our website unbalanced in regards to domestic pets. Let’s make a gallery
for dog images to make everything right. Go ahead and make a dog gallery page
similar to the one for cats for the following image.

![Shibe][shibe]

Now, let’s create a link to this page from `index.html`. At this point, we seem to
be creating a list of image galleries. Lucky for us, HTML has built in support
for creating multiple kinds of lists.

### Unordered lists

Unordered lists are collections of related items, where their order does not
matter. These are typically formatted with bullet points, but you may see them
with squares, circles, or nothing to the left of each item. You can create an
unordered list with the `<ul>` tag, and `<li>` tags for each item.

    <ul>
      <li>Cats</li>
      <li>Dogs</li>
      <li>Turtles</li>
    </ul>

### Ordered lists

Ordered lists are just like unordered lists, but, as implied, order does matter.
List items in an ordered list can be prefixed with integers, letters, or roman
numerals. The tag for an ordered list is `<ol>`:

    <ol>
      <li>Ruby</li>
      <li>Python</li>
      <li>PHP</li>
    </ol>

On the index page, organize your links to the dog and cat galleries into an
unordered list. Your page should look like this:

![Gallery With Linked List Demo][gallery_with_linked_list_demo]

Stage all of your changed files with `git add`, commit them, and push to GitHub.
To see all of the files that you have changed, use `git status`.

[paragraphs_demo]: images/paragraphs_demo.png
[bolded_and_italicized_demo]: images/bolded_and_italicized_demo.png
[gallery_demo]: images/gallery_demo.png
[part_1]: part_1.md
[gallery_with_link_demo]: images/gallery_with_link_demo.png
[cats_demo]: images/cats_demo.png
[visited_link_demo]: images/visited_link_demo.png
[grumpy_cat]: images/grumpy_cat.png
[gallery_with_grumpy_cat_demo]: images/gallery_with_grumpy_cat_demo.png
[shibe]: images/shibe.png
[gallery_with_linked_list_demo]: images/gallery_with_linked_list_demo.png
