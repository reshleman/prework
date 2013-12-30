# Part 5

## The Box Model

When using CSS it’s important to understand the Box Model. The Box Model is how
we refer to an HTML element and the spacing inside and around that element.
There are a few different CSS properties that when combined make up the box
model:

`width`: For inline elements this will be however much space it takes for the
content of the element. For block elements this will either be the maximum width
the block can take up or it will be the width you’ve specified via CSS.

`height`: For both block and inline elements their height is the height required
to fill the content vertically. Additionally you can specify the height for
block elements.

`padding`: Padding is white space that surrounds the content. It will make the
size of your HTML element larger. Padding can be applied in any of the four
directions: top, bottom, left, and right. Padding can be different measurements
for any of the directions, as well.

`border`: A border is typically a colored line around the outside of the element -
essentially around the size of the content plus any padding. The border will add
to the size of the element. Similar to padding, a border can have different
measurements for any of the directions.

`margin`: Margin is white space the surrounds the outside of the element. It is
not considered part of the element itself but is useful for “pushing” the
element away from other elements. As with paddings and borders, margins can have
different measurements for any direction.

Here is a graphical representation of the box model:

![Box Model][box_model]

As you can see, each margin, border, and padding will have values for
the top, right, and bottom. They’ll each extend from the width and height of the
content starting with padding, border, and then margin. In our image the “total
width” of the element is:

    total width = width + padding left + padding right + border left + border right

The “total height” is:

    total height = height + padding top + padding bottom + border top + border bottom

Also remember that the margin is going to push the element away from surrounding
elements in the directions you specify. Typically for a left margin the element
itself will move to the right. For a right margin the element that occurs after
the one with the margin will be moved to the right. With a top margin the
element itself will move down and with a bottom margin it will push elements
beneath it downwards.

If you want an element to entirely take up a specific width you will need to
subtract any padding and border you want to add in order for the element to be
the correct size.

Let’s try out border and margin. First add another the following image to
`cats.html`.

![Colonel Meow][colonel_meow]

Now edit your css and add the following:

    img {
        border: 1px solid black;
        margin: 10px;
    }

Your cats page should now look like:

![Two Cat Gallery][two_cat_gallery]

## Floating Content

It would be nice if our cat page had the image side by side at the top rather
than the bottom. This is happening because both `img` tags are inline elements
and have made the size of the line rather large. We can make them line up
correctly by floating them. Floating an element is typically used on block-level
elements to make them `float` next to each other. In addition to affecting
block-level elements, it will make inline elements not affect the line height.
Let’s float our images by adding:

    float: left

to our `img` selector on the `cats.html` page. We should see the following result:

![Floated Two Cat Gallery][floated_two_cat_gallery]

Notice that our margins are still obeyed when floating content. Floating can be
tricky and have odd consequences, for instance if we add inline content after
our image it will appear next to them, you can make content `clear` the left
float by using:

    clear: left;

Additionally you could use `right` or `both` instead of `left`.

## External CSS

We have a problem now that we have to maintain the CSS across all of our files.
We can solve this by making our css an external resource. External resources are
any pieces of content that the browser has to load separately from your html
page. While you can leave all of your CSS in your main document there are a
couple of reasons you’d want to make it an external resource:

* It’s easier to share across multiple pages
* If a browser is caching a page, it doesn’t have to request the entire page if
the CSS changes
* Similarly if the page changes but the style does not it won’t have to make an
additional request
* It makes it easier to organize your website

To load our CSS externally we’ll want to cut all of the content between our
`style` tag and paste that into a new file called `application.css`. Afterwards
you can delete your empty `style` tag. Next we’ll want to tell our page to use
the file we’ve extracted. We can do this by using the `link` tag. The `link`
tag’s sole purpose is to load external CSS files. The `link` tag belongs in your
`head`. Before we add our link tag let’s refresh the page. It should look bland
again because we’ve removed the CSS. Now let’s change our html file’s `head` tag
to have:

    <link rel=”stylesheet” href=”application.css”>

`rel` is used to describe the relationship between the current document and the
linked resource.
`href` is used much the same way here as with `a` tags and specifies the
location of our external resource.

When you refresh your page, your browser will make a request for this file and
style the page once again. Go ahead and replace the styles on the rest of your
HTML places with the link to `application.css`. Now, when you edit the external
stylesheet, you won’t have to make the same changes to each individual HTML
file.

## Validate your website

W3C, or the World Wide Web Consortium, is the organization that creates the open
standards for the web. Their website contains tools that validate your HTML and
CSS documents against the standard. Upload your documents to the appropriate
[HTML][html_validator] and [CSS][css_validator] validators to ensure correctness.

## Moving on

If you feel comfortable with everything you learned in Part 5, please move on to
[the project][the_project].

[box_model]: images/box_model.png
[colonel_meow]: images/colonel_meow.jpg
[two_cat_gallery]: images/two_cat_gallery.png
[floated_two_cat_gallery]: images/floated_two_cat_gallery.png
[html_validator]: http://validator.w3.org/#validate_by_upload
[css_validator]: http://jigsaw.w3.org/css-validator/#validate_by_upload
[the_project]: README.md#project
