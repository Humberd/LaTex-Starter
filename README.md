# LaTex-Starter

This is a template for starting a Master Thesis.

#### Features
 * Default styles configuration.
 * Auto generation of Table of Contents
 * Auto generation of Spis rysunkow
 * Auto generation of Kody źródłowe
 * Auto generation of Literatura
 
 
## Prerequistes
  To efficiently develop a Master Thesis you need:
  
  1. [LaTeX](https://www.latex-project.org/get/) - Latex compiler
  2. [Texmaker](http://www.xm1math.net/texmaker/index.html) - Latex IDE
  3. [JabRef](http://www.jabref.org/) - bibliography GUI editor
  
## Basics

The project is split into many small thematic files called _Pages_. For example: 
titlePage, introductionPage or eventsPage. The project has the main file called `main.tex`,
which defines the configuration of the document. It also imports every _Page_, so you have to rember:
**When you create a new Page don't forget to import it in the main file!**

Bibliography source file is `bib/bibliography.bib`. You can open it using _JabRef_ or just edit it by hand.
It's only a text file.

## Problems

In Texmaker by default you can only compile the document when you have the file with document configuration opened.
In our case it's `main.tex`. So when you edit your _Page_ and you want to compile to see how it looks
you would have to close the page and then compile it. 

#### To fix this issue:
 1. Go to Texmaker
 2. Click **Options**
 3. Click **Define current document as 'Master Document'** while having `main.tex` opened.
 
Now you can hit **F1** and the document will compile successfully on whatever the page you are.

------

Texmaker by default doesn't compile bibliography by itself.

#### To fix this issue:
 1. Go to Texmaker
 2. Click **Options**
 3. Click **Configure Texmaker**
 4. Head to **Quick Build** on the left
 5. Check **PdfLaTeX + Bib(la)tex + pdfLaTeX (x2) + View Pdf**
 6. Click OK
 
Now when you hit **F1** Texmaker will also compile your bibliography

------

The pdf view on the right sometimes does not reflect the changes after compilation, for example:
 * when you add a new image and it doesn't appear in the _Spis rysunków_
 * when you add a new translation and it doesn't appear anywhere in the document
 * or anything else
 
#### To fix this issue:
  Compile (F1) the documnet a couple of times. The issue should be gone.
  
If it doesn't work only [God](https://www.google.com/) can help you.

## Tips
 * `\include{texParts/statementPage}` - creates a new page and puts a _Page_ on it
 * `\input{texParts/examplePage}` - doesn't create a new page and puts a _Page_ right after ther previous text finished
 * `\clearpage` - makes a new page
