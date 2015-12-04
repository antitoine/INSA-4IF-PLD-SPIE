# Construit le PDF du rapport LaTex

LATEX_BUILDER=pdflatex
BUILD_FLAGS=-interaction nonstopmode
ECHO=@echo
RM=rm -f

all: build

build: cleanAll buildTitle

show:
	$(ECHO) "Nothing to show"

clean:
	$(RM) *.toc *.log *.aux *.tdo *.lof *.lot

cleanAll: clean
	$(RM) *.pdf

buildTitle: title.tex
	$(LATEX_BUILDER) $(BUILD_FLAGS) $< #> /dev/null
	$(LATEX_BUILDER) $(BUILD_FLAGS) $< #> /dev/null

.PHONY: clean show
