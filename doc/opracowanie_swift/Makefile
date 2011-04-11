NAME=swift

FILES= \
swift.tex

BIB= \
../bibliografia.bib

all: pdf

clean:
	rm $(NAME).aux $(NAME).log $(NAME).toc $(NAME).out $(NAME).bbl $(NAME).blg 2> /dev/null

pdf: bib $(FILES)
	pdflatex $(NAME).tex

bib: $(BIB)
	pdflatex $(NAME).tex
	bibtex $(NAME).aux
	pdflatex $(NAME).tex

run: pdf
	evince $(NAME).pdf

