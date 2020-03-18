@def title = "Post | Jupyter"
@def hascode = true
@def hasmath = true
@def date = Date(2019, 3, 22)

~~~
    <article class=article>
        <div class="article-container pt-3">
            <h1>Display Jupyter Notebooks with Academic</h1>
            <p class=page-subtitle>Learn how to blog in Academic using Jupyter notebooks</p>
            <div class=article-metadata>
                <div><span><a href=/authors/admin/>Nelson Bighetti</a></span></div><span class=article-date>Last updated on
Sep 5, 2019</span>
                <span class=middot-divider></span><span class=article-reading-time>2 min read</span></div>
        </div>
        <div class="article-header article-container featured-image-wrapper mt-4 mb-4" style=max-width:720px;max-height:313px>
            <div style=position:relative><img src=/assets/post/jupyter/featured.png alt class=featured-image></div>
        </div>
        <div class=article-container>
            <div class=article-style>
~~~

```python
from IPython.core.display import Image
Image('https://www.python.org/static/community_logos/python-logo-master-v3-TM-flattened.png')
```

![png](/assets/post/jupyter/index_1_0.png)

```python
print("Welcome to Academic!")
```

Welcome to Academic!

## Install Python and JupyterLab

[Install Anaconda](https://www.anaconda.com/distribution/#download-section) which includes Python 3 and JupyterLab.

Alternatively, install JupyterLab with `pip3 install jupyterlab`.

## Create or upload a Jupyter notebook

Run the following commands in your Terminal, substituting `<MY-WEBSITE-FOLDER>` and `<SHORT-POST-TITLE>` with the file path to your Academic website folder and a short title for your blog post (use hyphens instead of spaces), respectively:

```bash
mkdir -p <MY-WEBSITE-FOLDER>/content/post/<SHORT-POST-TITLE>/
cd <MY-WEBSITE-FOLDER>/content/post/<SHORT-POST-TITLE>/
jupyter lab index.ipynb
```

The `jupyter` command above will launch the JupyterLab editor, allowing us to add Academic metadata and write the content.

## Edit your post metadata

The first cell of your Jupter notebook will contain your post metadata ([front matter](https://sourcethemes.com/academic/docs/front-matter/)).

In Jupter, choose _Markdown_ as the type of the first cell and wrap your Academic metadata in three dashes, indicating that it is YAML front matter: 

```
---
title: My post's title
date: 2019-09-01

# Put any other Academic metadata here...
---
```

Edit the metadata of your post, using the [documentation](https://sourcethemes.com/academic/docs/managing-content) as a guide to the available options.

To set a [featured image](https://sourcethemes.com/academic/docs/managing-content/#featured-image), place an image named `featured` into your post's folder.

For other tips, such as using math, see the guide on [writing content with Academic](https://sourcethemes.com/academic/docs/writing-markdown-latex/). 

## Convert notebook to Markdown

```bash
jupyter nbconvert index.ipynb --to markdown --NbConvertApp.output_files_dir=.
```

## Example

This post was created with Jupyter. The orginal files can be found at https://github.com/gcushen/hugo-academic/tree/master/exampleSite/content/post/jupyter

~~~
            </div>
        </div>
    </article>
~~~

