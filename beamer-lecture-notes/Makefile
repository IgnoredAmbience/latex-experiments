LATEXMK = latexmk
LATEXMKFLAGS = -norc -interaction=nonstopmode -halt-on-error -file-line-error

# Fetch all output forms of the lecture notes (example.*.tex)
LECTEX := $(wildcard example.*.tex)
LECPDF := $(patsubst %.tex,%.pdf,$(LECTEX))

all: $(DIRS) $(LECPDF)

%.pdf: %.tex
	$(LATEXMK) $(LATEXMKFLAGS) -pdf $<

$(LECPDF): example.tex beamer-inline.sty  # Add other dependencies of example.tex here
example.article.pdf: example.slides.pdf   # Slides inserted into article version are extracted from the pdf

clean: $(CLEANDIRS)
	$(LATEXMK) $(LATEXMKFLAGS) -C $(LECTEX)
	$(RM) *.snm
	$(RM) *.nav

.PHONY: all
.PHONY: clean
