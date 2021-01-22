# Ruth's Awesome LaTeX MakeFile

DOC = main

all : $(DOC).tex
	pdflatex $(DOC).tex
#	makeindex $(DOC)
	pdflatex $(DOC).tex
	bibtex $(DOC)
	bibtex $(DOC)
	pdflatex $(DOC).tex
#	makeindex $(DOC)
	pdflatex $(DOC).tex

open : $(DOC).tex
	pdflatex $(DOC).tex
	pdflatex $(DOC).tex
	bibtex $(DOC)
	bibtex $(DOC)
	pdflatex $(DOC).tex
	pdflatex $(DOC).tex
	open $(DOC).pdf

# if there is a pdf already in the folder make clean first, just so we can actually make
#$(DOC).pdf : $(DOC).tex
#	pdflatex $(DOC).tex
#	pdflatex $(DOC).tex
#	bibtex $(DOC)
#	bibtex $(DOC)
#	pdflatex $(DOC).tex
#	pdflatex $(DOC).tex
#	open $(DOC).pdf

# quick compile if we only have changed a little text, saves time.
text : $(DOC).tex
	pdflatex $(DOC).tex
	pdflatex $(DOC).tex
#	open $(DOC).pdf

# the mv command is a hack to make sure that we can actually run if changes are not in main.tex
clean :
	rm -f *.toc *.aux *.log *.out
	mv $(DOC).pdf tmp.pdf

# won't do the annoying move of our pdf. :)
finish :
	rm -f *.toc *.aux *.log *.out
