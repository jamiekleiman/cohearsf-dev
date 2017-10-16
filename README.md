# cohearsf.com

## Jekyll

This website is implemented using [Jekyll](https://jekyllrb.com/), which is a static site generator. 

## How to run the site locally

From a console: 

Install Jekyll: 

```
$ gem install jekyll 
```

Clone the repository:

```
$ git clone https://github.com/jdmaturen/cohearsf.com
```

And then run jekyll in that directory: 

```
$ cd cohearsf.com
$ jekyll serve
```

And then open a browser to http://127.0.0.1:4000/ and you should see the site! 

## Site Architecture

The primary template is in [`_layouts/default.html`](./_layouts/default.html). 

All 6 pages are in the top directory: [`index.html`](index.html), [`process.html`](process.html), [`mission.html`](mission.html), [`about.html`](about.html), and [`blog.html`](blog.html). The top of each contains a fragment of markdown that specifies which layout (default) the page gets rendered with, as well as that page's title content. 

Styling is managed through SASS in [`css/main.scss`](css/main.scss) and the [`_sass/`](_sass/) directory. There is some common styling and then each page has a default as well as mobile styling SASS file. This is a pretty brute force approach and not at all the most elegant. 

## Images

Images were squashed using [imageOptim](https://imageoptim.com/mac) before being added to the repo. The [`<picture>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/picture) html element is used to manage responsive images. Images are by default served at 2x dpi. One or two images which are quite large have conditional logic for serving at high res. 
