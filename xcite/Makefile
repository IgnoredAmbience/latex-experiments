LATEXMK = latexmk
LATEXMKFLAGS = -norc -interaction=nonstopmode -halt-on-error -file-line-error

all: xcite.pdf xcite.sty

%.pdf: %.tex
	$(LATEXMK) $(LATEXMKFLAGS) -pdf $<

%.pdf: %.dtx
	$(LATEXMK) $(LATEXMKFLAGS) -pdf $<

%.sty: %.ins
	latex $<

clean:
	$(LATEXMK) $(LATEXMKFLAGS) -C xcite.dtx
	rm -f xcite.{glo,sty}

.PHONY: all
.PHONY: clean
