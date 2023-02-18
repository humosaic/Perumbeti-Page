# Home

## academicpages is a ready-to-fork GitHub Pages template for academic personal websites

This is the front page of a website that is powered by the [academicpages template](https://github.com/academicpages/academicpages.github.io) and hosted on [GitHub pages](https://pages.github.com/). GitHub pages is a free service in which websites are built and hosted from code and data stored in a GitHub repository, automatically updating when a new commit is made to the respository. This template was modified to [fit the mkdocs-material theme](https://squidfunk.github.io/mkdocs-material/getting-started/) from the [Jekyll academicpages](https://academicpages.github.io/) ([git repo](https://github.com/academicpages/academicpages.github.io)), which has been extended to support the kinds of content that academics have: publications, talks, teaching, a portfolio, blog posts, and a dynamically-generated CV. You can fork [this repository](https://github.com/CosiMichele/academicpages-mkdocs) right now, modify the configuration and markdown files, add your own PDFs and other content, and have your own site for free, with no ads!

## A data-driven personal website
The content & metadata of your website are in structured markdown files, while various other files constitute the theme, specifying how to transform that content & metadata into HTML pages. You keep these various markdown (.md), YAML (.yml), HTML, and CSS files in a public GitHub repository. Each time you commit and push an update to the repository, the GitHub pages service creates static HTML pages based on these files, which are hosted on GitHub’s servers free of charge.

Many of the features of dynamic content management systems (like Wordpress) can be achieved in this fashion, using a fraction of the computational resources and with far less vulnerability to hacking and DDoSing. You can also modify the theme to your heart’s content without touching the content of your site. If you get to a point where you’ve broken something in Jekyll/HTML/CSS beyond repair, your markdown files describing your talks, publications, etc. are safe. You can rollback the changes or even delete the repository and start over – just be sure to save the markdown files! Finally, you can also write scripts that process the structured data on the site, such as this one that analyzes metadata in pages about talks to display a map of every location you’ve given a talk.

## Getting started
1. Register a GitHub account if you don’t have one and confirm your e-mail (required!)
2. Fork this repository by clicking the “fork” button in the top right.
3. Go to the repository’s settings (rightmost item in the tabs that start with “Code”, should be below “Unwatch”). Rename the repository “[your GitHub username].github.io”, which will also be your website’s URL.
4. Set site-wide configuration and create content & metadata (see below – also see this set of diffs showing what files were changed to set up an example site for a user with the username “getorg-testacct”)
5. Upload any files (like PDFs, .zip files, etc.) to the files/ directory. They will appear at https://[your GitHub username].github.io/files/example.pdf.
6. Check status by going to the repository settings, in the “GitHub pages” section

## Site-wide configuration
The main configuration file for the site is in the base directory in mkdocs.yml, which defines the content in the sidebars and other site-wide features. You will need to replace the default variables with ones about yourself and your site’s github repository. For example, if you don’t have a portfolio or blog posts, you can remove those items from that mkdocs.yml file to remove them from the header.

## Create content & metadata
For site content, there is one markdown file for each type of content, which are stored in directories like _publications, _talks, _posts, _teaching, or _pages. For example, each talk is a markdown file in the _talks directory. At the top of each markdown file is structured data in YAML about the talk, which the theme will parse to do lots of cool stuff. The same structured data about a talk is used to generate the list of talks on the Talks page, each individual page for specific talks, the talks section for the CV page, and the map of places you’ve given a talk (if you run this python file or Jupyter notebook, which creates the HTML for the map based on the contents of the _talks directory).