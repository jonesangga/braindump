# mdBook

01-04-25

My last experience with [Jekyll](https://jekyllrb.com/) and [Hugo](https://gohugo.io/) are bad.
For Jekyll, I have trouble with related ruby gems.
For Hugo, it is often fail to live reload the served page.

Then there was time I made my own static site generator using Make and Bash.
It doesn't scale because that time I don't know about parsing hence I cannot
implement a slightly complex markup template.

Then there was time I manually write html and css. It was a trouble to change
a common code like menu items or footnote.

Then I accidently found mdBook from [this](https://xmonader.github.io/letsbuildacompiler-pretty/)
compiler tutorial. It uses Rust. I already have Rust. I build mdBook. It succeed.

Now by just doing

```
mdbook init my-first-book
cd my-first-book
mdbook serve --open
```

I have a page open in browser that automatically refresh with a nice default theme.

But I check Codeberg cannot build these from source like Github.
I don't want to put the built html pages. So I think this time I will place the repo in Github.

I won't change anything, just use the default.
