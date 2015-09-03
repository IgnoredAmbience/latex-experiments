LATEXMK = latexmk
LATEXMKFLAGS = -norc -interaction=nonstopmode -halt-on-error -file-line-error

# Fetch all output forms of the lecture notes (example.*.tex)
TEX := $(wildcard *.tex)
PDF := $(patsubst %.tex,%.pdf,$(TEX))

all: $(PDF)

report.pdf: publications.pdf

%.pdf: %.tex
	$(LATEXMK) $(LATEXMKFLAGS) -pdf $<

clean:
	$(LATEXMK) $(LATEXMKFLAGS) -C $(TEX)

.PHONY: all
.PHONY: clean
