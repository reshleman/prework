# Basic CSS

Now that we have a few pages of content, the site is starting to look a little
bland. Our pages are all black and white, with the default fonts and link
colors, and our images are squashed up against the text. We would like to style
it to make it look a little nice, however HTML is not the right tool for the
job. Remember that HTML is used for markup. It gives semantic meaning to
elements on the page, telling the browser and programmer what elements are
headers, paragraphs, etc. For defining how our page looks we will use CSS
(Cascading Style Sheets).

CSS allows us to style elements on the page without coupling our styles to the
HTML. This means that we can define a style once, for example that all
paragraph’s have blue text, and we don’t have to copy that style definition from
paragraph to paragraph. Let’s take a look at a chunk of CSS that will do just
that:

    p {
      color: blue;
    }

## Selectors

The selector, in this case the `p` element before the opening bracket,
determines what elements on the page are affected by the styles within the
brackets. Selectors can be very generic, targeting all paragraph tags on the
page, or can hone in on specific elements. We will discuss some of this
flexibility soon.

## Declarations

Declarations are the property and value pairs within the brackets. Each selector
may have multiple declarations within the brackets.

## Properties

The property, in this case the `color` attribute before the colon, determines
what style will be applied to all selected elements. There are numerous
properties available that can change an element’s color, size, position on the
page, visibility, and more.

Now that we know how to define styles, let’s change the color and size of the
header tag at the top of our page. Because our style definitions are a directive
for the browser and are not rendered on the page, we will define them in the
`head` section of the document. Inside of `<head>` add the following:

    <style>
      h1 {
        color: magenta;
      }
    </style>

If you open the page in a browser, you should see something like this:

![Magenta Header][magenta_header]

If you visit the other pages of your site, you will see that they are still
unstyled. To style them in the same way, copy the `<style>` tag and its contents
from the index page into the other documents.

## Ids and Classes

When we described CSS selectors, we mentioned that it was possible to target
items in a more specific way than by their tag. If we have multiple `p` tags on
a page, it is often useful to be able to target one p separately than the
others. This is where `id`s and `class`es come in.

`id`s are used when only a single element on the page will have that id; for
example, the logo in the top left hand corner of a page. Once you give an
element an `id`, no other element can have that same `id`.

`class`es can be used on multiple elements on the page, even elements that are not
of the same type. For example, you may have multiple `div`s or `p`s that have the
same border around them.

You can add one or more `id`s and `class`es to any HTML tag like the following:

    <p class=’orange’>This paragraph has a class of ‘orange’.</p>
    <p class=’orange left’>This paragraph has a class of ‘orange’ and a class of ‘left’.</p>
    <h1 id=’logo’>This header has an id of ‘logo’</h1>
    <div class=’orange’ id=’left-column’>This div has a class of ‘orange’ and an id of ‘left-column’</div>

In CSS, you can target any element with a `class` by using a period followed by
the class name. Target elements with the `class` of `orange` like so:

    .orange { … }

Similarly, do the same for `id`s with a hashtag:

    #logo { … }

## divs and spans

We have mentioned `div` and `span`s a couple times already. These tags are
frequently used for styling as they have few default styles applied to them and
have no semantic meaning (whereas a `p` should only be used for paragraphs). Since
`div`s are block elements, they are often used for layouts and positioning.
`span`s, on the other hand, are inline elements often used to add a style within a
part of another tag. For example:

    <h1>The <span class=’green’>Green</span> Mile</h1>

    .green {
      color: green;
    }

The above will give the word ‘Green’ a green color, but the rest of the `h1` will
have the default styles.

## Chaining selectors

You don’t have to limit yourself to targeting elements by either an `id`,
`class`, or `tag`. You can also chain these together and target elements based on
how they are nested.

Select all paragraphs that have the class `orange`:

    p.orange { .. }

Select `div`s with the `class` `left` and `id` `hero`:

    div.left#hero { … }

Select image tags that are inside a `div`:

    div img { … }

Select `div`s and `img`s:

    div, img { … }

These are the types of selectors we feel you will use most often. For more, see
the [W3Schools reference on CSS Selectors][w3schools_css_selectors].

Note that, while all the above are possible, and sometimes necessary, it is
preferable to use the most minimal selector possible. Much of time that will be
only a single element or class.

Let’s pull of of this together. Modify your `index.html` file so it has the
following below the `h1`

    <div id=”introduction”>Below are a list of galleries that contain images of
    animals.</div>

Let’s modify the other `div` to have an `id` of “galleries”. Then add the following
to your `<style>` tag:

    #introduction {
      color: gray;
    }
    #galleries li a {
      color: green;
    }

Your page should now look like:

![Green Gallery Links][green_gallery_links]

## Measurements

CSS properties that take measurements can be in any of the following units:

`px`: number of pixels on the screen.
`em`: Usually used for fonts, `1em` is equal to the current font size, `2em` is two
times the current font size, etc. ems are useful, as you can size things
relative to one another.
`%`: When applied to fonts, it is relative to the current font size, much like em.
When applied as widths and heights of elements, it is relative to the width or
height of the containing block.

Let’s set the body text to `20px`:

    body {
      font-size: 20px;
    }

Now all text within the body will be based on that size, and you should see your
paragraph text is `20px` tall. You should also see the size of your `h1` increase,
but it is much larger than `20px`. This is because the default `font-size` for an
`h1` is `2em`, so it scales relative to the current font size.

When you are done; add, commit, and push all of your changes to GitHub.

[magenta_header]: images/magenta_header.png
[w3schools_css_selectors]: http://www.w3schools.com/cssref/css_selectors.asp
[green_gallery_links]: images/green_gallery_links.png
