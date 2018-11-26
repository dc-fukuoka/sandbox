LATEX  = latex
DVIPDF = dvipdf
SRC    = note.tex
DVI    = $(SRC:%.tex=%.dvi)
OUT    = $(SRC:%.tex=%.pdf)

.SUFFIXES: .tex .dvi

.tex.dvi:
	$(LATEX) $<
	$(LATEX) $< # workaround for a warning of a reference of an equation

$(OUT): $(DVI)
	$(DVIPDF) $^

ALL: $(OUT)

clean:
	rm -f *.log *.dvi *.ps *.pdf *.aux *~
