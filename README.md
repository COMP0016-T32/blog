# COMP0016-T32 Development Blog
Welcome, this is team 32 of MotionInput v3.2.

## How to see the generated website
If there is a `_site` directory, it is the generated website which is also running [here](https://comp0016-t32.github.io/blog/).

## How to run the blog in local
1. Install Ruby and NodeJS

This site is built with [Jekyll](https://jekyllrb.com/), a static site generator. To run the site locally, you need to install Ruby and RubyGems first. Then, install Jekyll and Bundler gems through the command line.

```bash
gem install jekyll bundler
```

Next, in the root directory, run:

```bash
bundle install
```

Finally, run the following command in the root directory of the project to start the server.

```bash
bundle exec jekyll serve
```

or to generate a website run:

```bash
bundle exec jekyll build
```

There will be `_site` directory generated in the root directory.

## How to write a blog post
To add a new post, create a new markdown file in the `_posts` directory. The naming of the file must follow the following convention: `YYYY-MM-DD-title.markdown`. To change a post, find it in the `_posts` directory according to the title.
