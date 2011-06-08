.SUFFIXES: .svg .pdf
.PHONY: all clean
IMG_DEPS=fuse.pdf drzewo.pdf

NAME=dokumentacja_koncowa

all: $(NAME).pdf

$(NAME).pdf: $(NAME).tex $(NAME).blg ${IMG_DEPS}
	pdflatex $^
	pdflatex $^

$(NAME).blg: $(NAME).aux
	bibtex $^

$(NAME).aux: $(NAME).tex ${IMG_DEPS}
	pdflatex $^

clean:
	rm -f $(NAME).aux $(NAME).bbl $(NAME).blg $(NAME).log $(NAME).out \
		$(NAME).toc *.pdf

.svg.pdf:
	inkscape -A $@ $^
