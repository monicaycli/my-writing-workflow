# My Writing Workflow
## markdown, pandoc, and more!
![](./workflow.png)
1. I use [_Mendeley_](https://www.mendeley.com/) to organize PDF files of academic articles.
2. _Mendeley_ can automatically generate `.bib` files that contain citation info of all or part of your _Mendeley_ library.
3.  `.csl` files specify what citation style (e.g., APA) the references will be formatted in. It can be extracted from _Mendeley_ or easily obtained from the internet.
4. [_Scrivener_](https://www.literatureandlatte.com/scrivener/overview) is a writing program I use for organizing my writing projects. It's good for making outline, moving things around, focusing on selective parts of a manuscript, taking notes, gathering research materials, exporting to various file formats etc.
    * Note: _Scrivener_ is a paid software. There is an open-source alternative that I heard of, called [_Manuskript_](http://www.theologeek.ch/manuskript/). I have not personally tried it, but it seems cool.
5. I usually write in _Scrivener_ and export the text as `.md`, so that version control can be done easily with `git` and `github`.
6. `.md` text can be converted to APA-formatted documents via `pandoc` along with appropriate specifications, including a `.bib` file, a `.csl` file (in APA style), and a APA-formatted template (in my case, a `.docx`).
7. Alternatively, to more easily include analyses and results in the manuscript, one can write in `.Rmd` to incorporate `R` code and outputs, and use `papaja` (an `R` package based on `pandoc`; recommended to use in `R Studio`) to convert the `.Rmd` into even more sophisticated version of APA documents then the previously mentioned regular `pandoc` approach.

----

# In this repository
* You will find examples of converting markdown (`.md`) or Rmarkdown (`.Rmd`) files into APA-formatted, publication-ready documents (e.g., `.docx`, `.pdf`, `.tex`), using `pandoc` or `papaja`.

* Specific instructions can be found in `example_pandoc.md` and `example_papaja.Rmd`

* `APA_template.docx` is modified from the template provided by `papaja`

* `APA_ML.csl` is modified from the [`apa.csl` obtained from _Zotero_](https://www.zotero.org/styles/apa), such that **in press** articles can be correctly cited with _Mendeley_.
    * Enter **in press** in the `Short title` field in _Mendeley_, which is equivalent to the `shorttitle` variable in `.bib` files
    * Note: If references are not managed via _Mendeley_, the regular `apa.csl` can be used with the `status` variable specified as **in press** for a given entry in `.bib` files

* See `example.bib` for ways to specify different types of manuscripts, including:
    * published journal articles
    * published books
    * published book chapters
    * in press manuscripts
    * manuscripts submitted for publication
    * unpublished manuscripts
    * master's theses or doctoral dissertations

----

# Useful links
## reference management
* Mendeley: https://www.mendeley.com/
* BibTeX (.bib): http://www.bibtex.org
* Citation Style Library (.csl): http://citationstyles.org/

## text editing
* interface
    * Scrivener: https://www.literatureandlatte.com/scrivener/overview
    * Manuskript: http://www.theologeek.ch/manuskript/
    * vim: https://www.vim.org/
    * vimwiki: https://github.com/vimwiki/vimwiki
    * MacDown: https://macdown.uranusjr.com/
    * R Studio: https://www.rstudio.com/
* filetypes
    * Markdown (.md): https://www.markdownguide.org/
    * Rmarkdown (.Rmd): https://rmarkdown.rstudio.com/

## file conversion / formatting
* pandoc: https://pandoc.org/
* scrivomatic: https://github.com/iandol/scrivomatic
* R Studio
    * papaja: https://github.com/crsh/papaja
    * bookdown: https://bookdown.org/yihui/bookdown/

## version control
* git: https://git-scm.com/
* github: https://github.com/
* hub: https://github.com/github/hub
* tig: https://github.com/jonas/tig
