Converting markdown file to `mobi` format.  

Steps:  

1. Convert `.md` into `.epub`
2. Convert `.epub` into `.mobi`

`md` -> `epub` -> `mobi` 

# From Markdown to EPUB

Install `pandoc`:  

    sudo apt-get update 
    sudo apt-get install pandoc

`pandoc` command for conversion:  

    pandoc -o sample.epub -f markdown_github -t epub sample.md

For multiple markdown files:  

    pandoc -o output.epub title.txt \
         chapters/chapter1.md \
         chapters/chapter2.md

# From EPUB to MOBI

Install Calibre:  

    sudo apt-get install calibre

Convert with the `ebook-convert` command:  

    ebook-convert "book.epub" "book.mobi"
