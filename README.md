### The group website repository

This repository hosts the source code for the [(new) group website](https://foroozandehgroup.github.io).
The site is currently built using [Jekyll](https://jekyllrb.com/).

----------

**Viewing the site offline**

1. Install Jekyll on your own system ([instructions](https://jekyllrb.com/docs/installation/)).
2. Clone this repository and `cd` into it.
3. Type at the command line `bundle exec jekyll serve`. This should launch a local HTTP server on port 4000, which can be accessed by navigating to http://127.0.0.1:4000 on a browser of choice.
4. If you edit any of the source code (_apart from_ `_config.yml`), the server will automatically detect the changes and refresh.


-----------

**Adding a new post**

See https://jekyllrb.com/docs/posts/. (_This_ markdown file, `README.md`, does not contain "front matter" and is therefore not parsed by Jekyll; it only serves as a readme on the GitHub repo itself.)

-----------

**Publishing changes online**

Commit the files and push to the master branch of this repository. GitHub will automatically build the website and deploy at https://foroozandehgroup.github.io.
