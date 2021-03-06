ENIDownloader
=============

Download a full PDF from Editions ENI.
It's fork project from [Nainterceptor PoC](https://github.com/Nainterceptor/ENIDownloader).

What is "Editions ENI" ?
------------------------

Editions ENI is a great company which sell some great books in french about technical subjects.

Why ?
-----

I want to read an ebook on my tablet/e-reader but I can't, because ENI want to "prevent" or "limit" piracy.
I have an account on ENI. So I have access to books and I can download a PDF. One by one for each chapter.
I can also read my book online through the website himself.
 
Now, I can download the book thanks to this PoC and read my book where I don't have Internet (like subways) without the manual download of ~120 files.

About the law...
----------------

In France, the copyright (called "Droit d'auteur") law [L122-5](https://www.legifrance.gouv.fr/affichCodeArticle.do?cidTexte=LEGITEXT000006069414&idArticle=LEGIARTI000006278917) has an exception called "private copy" ("Copie privée") :
> When the work has been divulged, the author may not prohibit [...] Copies or reproductions made from a lawful source and strictly reserved for the private use of the copier and not intended for collective use, [...].

So, you are not able to use this script to publish a book on a hidden network :)

Requirements
------------

[NodeJs](https://nodejs.org/), and run `~/[...]/ENIDownloader-master $ npm install`.

You should have [cpdf](http://community.coherentpdf.com/). Please download the according executable **cpdf** file to your OS [cpdf-binaries](https://github.com/coherentgraphics/cpdf-binaries) at root.

Usage
-----

Sorry, this script is under development, but functional, I provide no interface at this time, and it will be simplified.

Steps :
1. Login to your eni-training, choose your book, copy and past some values in **./app.js**
- your **URL** in "url" var, **line 7**
- your cookie value __\__rsaxc__: **line 29**
- your cookie value __\__hnwky__: **line 30**
- your cookie value __ENI\_Editions_Portail__: **line 31**
2. Execute `~/[...]/ENIDownloader-master $ npm run crawl`
- Check pdf in **./docs/** directory. If a file is < than 3ko, crawl failed. Check the number in the file name, uncomment lines 43/47, change the number, and back to step 1 : URL can change for the same book.
3. Execute `~/[...]/ENIDownloader-master $ npm run merge` to merge all pdf files in a single file and add a right "Page x of x" :)

Contribution
------------

Being a padawan, all contributions will be welcome :)
