NAME=pm

FILES= \
pm.tex

all: pdf

clean:
	rm $(NAME).aux $(NAME).log $(NAME).toc $(NAME).out $(NAME).bbl $(NAME).blg 2> /dev/null

pdf: $(FILES)
	pdflatex $(NAME).tex

run: pdf
	evince $(NAME).pdf

