@def title = "More goodies"
@def hascode = true
@def rss = "A short description of the page which would serve as **blurb** in a `RSS` feed; you can use basic markdown here but the whole description string must be a single line (not a multiline string). Like this one for instance. Keep in mind that styling is minimal in RSS so for instance don't expect maths or fancy styling to work; images should be ok though: ![](https://upload.wikimedia.org/wikipedia/en/b/b0/Rick_and_Morty_characters.jpg)"
@def rss_title = "More goodies"
@def rss_pubdate = Date(2019, 5, 1)

@@docs

~~~
        <div class="row flex-xl-nowrap">
            <div class="col-12 col-md-3 col-xl-3 docs-sidebar">
                <form class="docs-search d-flex align-items-center">
                    <button class="btn docs-toggle d-md-none p-0 mr-3" type=button data-toggle=collapse data-target=#docs-nav aria-controls=docs-nav aria-expanded=false aria-label="Toggle section navigation">
                        <span><i class="fas fa-bars"></i></span></button>
                    <input name=q type=search class=form-control placeholder=Search... autocomplete=off>
                </form>
                <nav class="collapse docs-links" id=docs-nav>
                    <div class="docs-toc-item active"><a class=docs-toc-link href=/courses/example/>Franklin</a>
                    </div>
                    <div class=docs-toc-item><a class=docs-toc-link >Features</a>
                        <ul class="nav docs-sidenav">
                            <li><a href=/courses/example/code-blocks/>Code Blocks</a>
                            </li>
                            <li><a href=/courses/example/more-goodies/>More Goodies</a>
                            </li>
                        </ul>
                    </div>
                </nav>
            </div>
            <div class="d-none d-xl-block col-xl-2 docs-toc">
                <ul class="nav toc-top">
                    <li><a href=# id=back_to_top class=docs-toc-title>Contents</a></li>
                </ul>
                <nav id=TableOfContents>
                ~~~
                \toc
                ~~~
            </nav>
            </div>
            <main class="col-12 col-md-9 col-xl-7 py-md-3 pl-md-5 docs-content" role=main>
                <article class=article>
                    <div class=docs-article-container>
                        <h1>More Goodies</h1>

~~~

@@article-style

## More markdown support

The Julia Markdown parser in Julia's stdlib is not exactly complete and Franklin strives to bring useful extensions that are either defined in standard specs such as Common Mark or that just seem like useful extensions.

* indirect references for instance [like so]

[like so]: http://existentialcomics.com/

or also for images

![][some image]

some people find that useful as it allows referring multiple times to the same link for instance.

[some image]: https://upload.wikimedia.org/wikipedia/commons/9/90/Krul.svg

* un-qualified code blocks and indented code blocks are allowed and are julia by default

    a = 1
    b = a+1

or

```
a = 1
b = a+1
```

you can specify the default language with `@def lang = "julia"`.
If you actually want a "plain" code block, qualify it as `plaintext` like

```plaintext
so this is plain-text stuff.
```

## A bit more highlighting

Extension of highlighting for `pkg` an `shell` mode in Julia:

```julia-repl
(v1.4) pkg> add Franklin
shell> blah
julia> 1+1
(Sandbox) pkg> resolve
```

you can tune the colouring in the CSS etc via the following classes:

* `.hljs-meta` (for `julia>`)
* `.hljs-metas` (for `shell>`)
* `.hljs-metap` (for `...pkg>`)
@@

@@
