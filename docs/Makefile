FILES = $(wildcard *.tex)
PDF = $(FILES:.tex=.pdf)

TEX = pdflatex
TFLAGS = -interaction=nonstopmode

all: $(PDF) clean-temp

%.pdf: %.tex
	$(TEX) $(TFLAGS) $<
	$(TEX) $(TFLAGS) $<

clean-temp:
	rm -f *.aux
	rm -f *.log
	rm -f *.lof
	rm -f *.lot
	rm -f *.out
	rm -f *.toc
clean: clean-temp
	rm -f $(PDF)

.PHONY: clean clean-temp
