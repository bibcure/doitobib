# Description
doi2bib is a module of [bibcure](https://github.com/bibcure/bibcure) and [scihub2pdf](https://github.com/bibcure/scihub2pdf)
![](https://raw.githubusercontent.com/bibcure/logo/master/gifs/doi2bib.gif) 

# Install

```
$ sudo python /usr/bin/pip install doi2bib
```
or if you want the full version

```
$ sudo python /usr/bin/pip install bibcure
```
# Features and how to use


Given a DOI number...

```
$ doi2bib 10.1038/s41524-017-0032-0
```

* get bib item given a doi (requires internet connection)

You can easily append
a bib into a bibfile, just do

```
$ doi2bib 10.1038/s41524-017-0032-0 >> file.bib
```

You also can generate a bibtex from a txt file containing a list of DOIs

```
$ doi2bib --input file_with_dois.txt --output refs.bib
```

## bibcure

Given a bib file...

```
$ bibcure -i input.bib -o output.bib
```

* check sure the Arxiv items have been published, then update them (requires
internet connection)

* complete all fields(url, journal, etc) of all bib items using DOI number (requires
internet connection)

* find and create DOI number associated with each bib item which has not
DOI field (requires internet connection)

* abbreviate journals names


## title2bib

Given a title...

```
$ title2bib An useful paper
```

* search papers related and return a bib for the selected paper (requires
internet connection)

You can easily append
a bib into a bibfile, just do

```
$ title2bib An useful paper --first >> file.bib
```

You also can generate a bibtex from a txt file containing a list of "titles"

```
$ title2bib --input file_with_titles.txt --output refs.bib --first
```

## arxivcheck

Given a arxiv id...

```
$ arxivcheck 1601.02785
```

* check if has been published, and then returns the updated bib (requires internet connection)

Given a title...

```
$ arxivcheck --title An useful paper published on arxiv
```

search papers related and return a bib the first item.
You can easily append a bib into a bibfile, just do

```
$ arxivcheck --title An useful paper published on arxiv >> file.bib
```

You also can interact with results, just pass --ask parameter

```
$ arxivcheck --ask --title An useful paper published on arxiv
```

# scihub2pdf

Given a bibtex file

```
$ scihub2pdf -i input.bib
```

Given a DOI number...

```
$ scihub2pdf 10.1038/s41524-017-0032-0
```

Given a title...

```
$ scihub2bib --title An useful paper
```

Location folder as argument

```
$ scihub2pdf -i input.bib -l somefoler/
```

Use libgen instead sci-hub

```
$ scihub2pdf -i input.bib --uselibgen
```
