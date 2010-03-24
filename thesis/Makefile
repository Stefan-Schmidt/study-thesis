FILE = thesis
PDFLATEX = pdflatex
PDFLATEX_OPTS =
LATEX = latex
LATEX_OPTS =
DVIPS = dvips
DVIPS_OPTS =
BIBTEX = bibtex

all: paper

dvi:
	${LATEX} ${LATEX_OPTS} ${FILE}.tex

ps: dvi
	${DVIPS} ${DVIPS_OPTS} ${FILE}.dvi

paper:
	${PDFLATEX} ${PDFLATEX_OPTS} ${FILE}.tex
	${BIBTEX} ${FILE}
	${PDFLATEX} ${PDFLATEX_OPTS} ${FILE}.tex
	${PDFLATEX} ${PDFLATEX_OPTS} ${FILE}.tex

clean:
	rm -f ${FILE}.{log,lof,lot,toc,aux,pdf,dvi,ps,out,nav,snm,bbl,blg}
