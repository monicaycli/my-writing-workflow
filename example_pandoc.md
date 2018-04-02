---
title: "Example for Converting Markdown into Word Doc and PDF with Pandoc"

author:
- Monica Li^a^
- Imaginary Author Two^b^
- ^a^_University of Connecticut_
- ^b^_Institute of Somewhere Over the Rainbow_
---

# Instructions
1. Install [`Pandoc`](https://pandoc.org/installing.html)

2. To convert this file into a Word Document, run the following command:
```
pandoc example_pandoc.md -o example_pandoc.docx \
--bibliography example.bib \
--csl APA_ML.csl \
--reference-doc APA_template_ML.docx \
--filter pandoc-citeproc
```

3. To convert this file into a PDF file, run the following command:
```
pandoc example_pandoc.md -o example_pandoc.pdf \
--bibliography example.bib \
--csl APA_ML.csl \
--filter pandoc-citeproc
```

# In-Text Citation Examples
Citations are referred to by their citation key (which you can specify in your reference manager, like _Mendeley_) in square brackets [@Magnuson2011], and multiple citations are separated by semicolon like so [@Magnuson2011; @Magnuson2015].

You can add a prefix or suffix to a citation, for example, when you cite pages from a book [@Marr1982, pp.24-27].

Although you can technically put the citation outside of square brackets like @Magnuson2018, you might encounter formatting issues like unwanted ampersands.
In cases like this, you might want to suppress the author name(s) in the parenthesis by adding `-` before the citation key, like this: Magnuson, Mirman, Luthra, Strauss, and Harris [-@Magnuson2018].

Also, the _(in press)_ part of the previous reference is enabled by my workaround `APA_ML.csl` to work with _Mendeley_.
Check out `example.bib` for `@Magnuson2018` to see how it's set up.

For theses, dissertations, unpublished, and almost published manuscripts, like [@Li2014; @Li2016; @Li2017; @Noordenbos2013a], some care needs to be done when entering the information in your reference manager.
Check out `example.bib` for these references to see the setup.

All cited references will be automatically generated at the end of the converted document or under `# References`/`# Bibliography`.

# References
