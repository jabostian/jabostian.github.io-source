# jabostian.github.io-source
Source for my github page.  

This is how I built the **Adventures in Computing** blog.  These sources were really helpful it getting
things up and running
- [http://docs.getpelican.com/en/stable/index.html](http://docs.getpelican.com/en/stable/index.html)
- [https://github.com/jakevdp/jakevdp.github.io-source](https://github.com/jakevdp/jakevdp.github.io-source)
- [https://gist.github.com/JosefJezek/6053301](https://gist.github.com/JosefJezek/6053301)

I used [Jake Vanderplas' blog](http://jakevdp.github.io/) as a model and example.

#### One-time setup to create the build environment
```
conda create -n jab-blog jupyter notebook
source activate jab-blog
pip install pelican Markdown ghp-import
```

#### Pelican Quickstart
```
cd <git-repo-for-blog-source>
pelican-quickstart
cd content
mkdir articles
mkdir images
mkdir -p downloads/notebooks
cd articles
vi 2017-01-01-hello-world.md
```
Add the necessary content for the article.  Mine looks like this:
```
Title: Hello World
Date: 2017-01-01
Category: Blog

Hello, World
```
Make sure not to put anything in the ```Title``` that can break Pelican - like the ```,``` that is often
included in Hello, World applications.

Now build the static content
```
cd <git-repo-for-blog-source>
make html
make serve
```
Now preview your article.  Use your browser to navigate to http://localhost:8000
