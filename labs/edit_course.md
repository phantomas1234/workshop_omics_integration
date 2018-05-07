---
layout: default
title: Edit course content
---

# Edit course content

## File hierarchy

You can basically invent your own structure for the course but a good template
is the following:


    _config.yml
    index.md
    labs/
        lab1.md
    lectures/
        lecture1.md
        lecture2.pdf
    img/
        plot1.png


## Course menubar

The contents of the menubar at the top is defined in the `_config.yml` file.
Towards the end of that file you should find an entry called `menu` followed
by a number of sub defined menu entries. It should be fairly self
exlpanatory. The number of whitespace characters before tings in the file is
_very_ important so be sure to follow the format.

The most important thing to focus on here is if you want direct links to each
lab and/or lecture which should probably be in submenus, as in this guide and
the base template.


## Pages

Pages are automatically generated by jekyll from the `.md` files in the
repository. A file called `schedule.md` will generate the page
`course-name/schedule` (you can also use the URL `course-name/schedule.html`,
the `.html` ending is optional). Subdirectories in the repository will end up
as subdirectories on the site, just remember to not start your directory names
with `_` (underscore) since those are special and reserved for jekyll.


## Images

It might be a good idea to put the images in the `img/` subdirectory and
reference them from there to reduce clutter.


## Page formatting

Jekyll uses fairly standard markdown format. Below is a quick refrence for most
of the features. **N.B** when adding code blocks, it's better to use the
<code>{% raw %}{% highlight language %}{% endraw %}</code> construct than backticks <code>```</code>.


    Paragraphs are separated by one empty row.

    Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor
    incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis
    nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.

    Indenting a paragraph a level gives a black box, like this:

        Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore
        eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt
        in culpa qui officia deserunt mollit anim id est laborum.

    It's possible to have **bold**, _italic_ and `code` text. Dividers can be
    done by three or more hyphens or underscores:

    ---

    ___


    Lists:

    * Bulleted list
    * with asterisks
    - or hyphens

    1. Numbered list
    2. More numbers
    5. The numbers don't matter
    3. You can have paragraphs in lists too

       As long as you indent properly.

    1. Again, it just needs to _be_ a number, markdown figures it out _what_
       number it should be for you.

    {% raw %}
    {% highlight R %}
    library(lib2)

    p <- read.csv("file.csv")

    plot(p[1,2])
    {% endhighlight %}
    {% endraw %}

    {% raw %}{% {% endraw %} raw %}
    {% raw %}Inside of `raw`/`endraw` it's possible to use {{, }}, {% and %} without problems.{% endraw %}
    {% raw %}{% {% endraw %} endraw %}


Paragraphs are separated by one empty row.

Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor
incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis
nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.

Indenting a paragraph a level gives a black box, like this:

    Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore
    eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt
    in culpa qui officia deserunt mollit anim id est laborum.

It's possible to have **bold**, _italic_ and `code` text. Dividers can be
done by three or more hyphens or underscores:

---

___


Lists:

* Bulleted list
* with asterisks
- or hyphens

1. Numbered list
2. More numbers
5. The numbers don't matter
3. You can have paragraphs in lists too

   As long as you indent properly.

1. Again, it just needs to _be_ a number, markdown figures it out _what_
   number it should be for you.

{% highlight R %}
library(lib2)

p <- read.csv("file.csv")

plot(p[1,2])
{% endhighlight %}

{% raw %}Inside of `raw`/`endraw` it's possible to use {{, }}, {% and %} without problems.{% endraw %}