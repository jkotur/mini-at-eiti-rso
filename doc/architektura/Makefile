.SUFFIXES: .svg .pdf
.PHONY: all clean
IMG_DEPS=fuse.pdf drzewo.pdf

all: architektura.pdf

architektura.pdf: architektura.tex architektura.blg ${IMG_DEPS}
	pdflatex $^
	pdflatex $^

architektura.blg: architektura.aux
	bibtex $^

architektura.aux: architektura.tex ${IMG_DEPS}
	pdflatex $^

clean:
	rm -f architektura.aux architektura.bbl architektura.blg architektura.log \
		architektura.out *.pdf

.svg.pdf:
	inkscape -A $@ $^
