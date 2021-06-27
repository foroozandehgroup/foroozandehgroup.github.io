# The group website repository

This repository hosts the source code for the [(new) group website](https://foroozandehgroup.github.io).
The site is currently built using [Jekyll](https://jekyllrb.com/) and [GitHub Pages](https://docs.github.com/en/github/working-with-github-pages/getting-started-with-github-pages).
You can enter text using a combination of [(GitHub flavoured) Markdown](https://github.github.com/gfm/) and [Liquid](https://shopify.github.io/liquid/), which is automatically converted to HTML and published every time the master branch is pushed to.
Mathematical and chemical equations can be typed using [MathJax](https://www.mathjax.org/).

----------

## What do these mean?

The links above have more detailed descriptions.

 - **GitHub Pages**: A mechanism by which you can host a website at `https://<username>.github.io`, free of charge. The easiest way to do so is to create a repository named `<username>.github.io`, as has been done here.

 - **Jekyll**: A software written in Ruby which converts Markdown files into HTML which can then be viewed with a web browser. It also provides CSS styles / themes for the website. It has "special" support on GitHub Pages, meaning that if you don't otherwise specify, GH Pages will automatically build the website using Jekyll (i.e. convert the Markdown files you commit into HTML).

 - **Markdown**: A simple markup language which is widely used on the Internet, including Stack Overflow and the Stack Exchange network, as well as GitHub itself. It is far easier to type in Markdown than in pure HTML, but web browsers cannot natively read Markdown files, hence the need for a conversion tool like Jekyll.

 - **Liquid**: A template language which can generate HTML in a programmatic fashion. Thus, for example, one can conditionally insert HTML code depending on whether the post satisfies a certain set of criteria.

 - **MathJax**: A set of JavaScript tools which render LaTeX-type maths equations as images (which actually look pretty good). Essentially, it allows you to use `$...$` and `$$...$$` (or `\(...\)` and `\[...\]`) in the Markdown code itself.

----------

## How do I do X?

**Viewing the site offline**

1. Install Ruby, Bundler, and Jekyll on your own system (follow [these instructions](https://jekyllrb.com/docs/installation/)).
2. Clone this repository and `cd` into it.
3. Run `bundle exec jekyll serve`. This should launch a local HTTP server on port 4000, which can be accessed by navigating to 127.0.0.1:4000 or localhost:4000 on a browser of choice.
4. If you edit any of the source code (_apart from_ `_config.yml`), the server will automatically detect the changes and refresh. If you edit `_config.yml`, you will have to terminate the `bundle` process and rerun it.

-----------

**Changing the front page**

Edit the `index.md` file. Note that many of the things are automatically filled in for you by the theme.

The current theme is called `hamilton`; there are quite a few others which are available.
The theme can be changed or customised in the `_config.yml` file: in there you can also change information such as the email address, etc. in the footer.

-----------

**Adding a new post**

1. Create a new file in the `_posts` directory called `YYYY-MM-DD-title.md`. (The title can be anything you like, but it will be turned into the URL of the website so probably a good idea to choose something sensible.)

2. Include some *front matter* at the top of the post: this includes information such as the title of the post, which Jekyll will use to create a heading. You can see how this works in any of the existing posts in that directory.

3. After the front matter, you can include any Markdown / Liquid code that you want. See https://jekyllrb.com/docs/posts/ for more information.

(_This_ markdown file, `README.md`, does not contain any front matter and is therefore not parsed by Jekyll; it only serves as a readme on the GitHub repo itself.)

-----------

**Adding an image to a post**

1. Put your image in the `assets/images` directory. If you plan to have a series of images it's probably a good idea to make a subdirectory for yourself.

2. In the Markdown file, you can use either Markdown syntax:

   `![Alt text](/assets/images/my_image.png)`

   or raw HTML, which gives you more control over width, height, and other properties:

   `<img src="/assets/images/my_image.png">` 

   Note that in both cases, the very first forward slash ensures that the path is resolved from the top-level directory. This is important! Or else you might have some difficulty finding the correct relative path.

-----------

**Publishing changes online**

Commit the files and push to the `master` branch of this repository. GitHub will automatically build the website and deploy at https://foroozandehgroup.github.io.
