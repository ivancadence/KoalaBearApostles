# KoalaBearApostles
crappy scripts used to export KBA into PDF

**Required Add-ons**
* Firefox Add-on: cmdlnprint
* booty.sh: 

# Usage

**get_articles**
this script crawls through the sections page in Zendesk, the script identify all article pages attached to this section and then pulls it down as a local html via wget.

```
$ get_articles https://employmenthero.zendesk.com/hc/en-us/sections/200612395-Notifications
```

output: all articles attached to this section will be downloaded into this path: $PWD/employmenthero.zendesk.com/hc/en-us/articles/..

**convert_article_pdf**
to use this script move into the dir housing the downloaded html content (../../hc/en-us/articles/.)
simply call by

```
$ convert_article_pdf
```

Script will pull down every .pdf file in current dir and clean it to be presentable in PDF format. Script will then load html into firefox and proceed to print into a PDF.

default output of pdf printed this way is $HOME/mozilla.pdf.

The script will attempt to mv output into a more meaningful name-scheme and store it in $HOME/zendesk/kba

