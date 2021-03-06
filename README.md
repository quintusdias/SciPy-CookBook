Scipy cookbook conversion
=========================

This is a conversion-in-progress of [Scipy
cookbook](http://wiki.scipy.org/Cookbook/) to Ipython notebooks. It's based on
Matti Pastell's work: https://github.com/mpastell/SciPy-CookBook

Give a hand
-----------

Your help is both needed and appreciated. The quick way to get started is to
fork this repo, and then do

    git clone git@github.com:YOURUSERNAME/SciPy-CookBook.git
    git remote add upstream https://github.com/pv/SciPy-CookBook.git
    cd SciPy-CookBook/ipython

and then switch to a new branch

    git checkout -b edit-xxx
    git fetch upstream
    git reset --hard upstream/master

after which

    ipython notebook
    # edit notebook XXX in ipython web notebook and save
    git commit -m "Fix up notebook XXX" -a
    git push origin edit-xxx

and then browse to your github repo page and send the fixed version as a pull
request.

If you however cannot be arsed to use git, just upload the file somewhere (e.g.
gist.github.com) and file [a new
issue](https://github.com/pv/SciPy-CookBook/issues) and tell which file you
changed and include a link to the uploaded file. Thanks!

Before starting, check out the list of pull requests and issues here to avoid
doing duplicate work.

What to fix
-----------

The Ipython notebook conversion is not fully flawless, and cannot be fully
automated. What needs to be done is:

- Ensure the code examples are runnable.

- Ensure the image links are correct (look for malformatted \[...\]\(...\) in
  the markdown text blocks --- the conversion didn't always treat these
  correctly).

  Local files and images should be linked to via standard Markdown syntax
  `[link text](files/attachments/NotebookName/filename)` and
  `![](files/attachments/NotebookName/image.png)`

- Ensure each notebook begins with a top-level heading with a title for the
  snippet.  Avoid using other top-level headings in the rest of the notebooks.
  (This should be the case currently.)

- Replace image attachments with the images generated by the plotting commands
  in the examples themselves, where appropriate.

- Remove unnecessary file attachments, where appropriate (remember that the
  ipython notebooks can be converted to scripts easily, and the purpose is more
  to distribute code snippets rather than full modules).

- Remove obviously useless (e.g. empty) files.

- Obviously outdated content should get a short notice on top, with a date
  of the last update on http://wiki.scipy.org/

- If some entry is too incomplete to fix (e.g. math formulas), look at the
  source version at http://wiki.scipy.org/Cookbook/

- And other things. Note, however, that the point is more to fix surface issues
  than to try to rewrite things in a better way.

