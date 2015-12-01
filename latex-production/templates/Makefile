# VARS
RM=rm -f
ECHO=@echo
LATEX_BUILDER=pdflatex
BUILD_FLAGS=-interaction nonstopmode

# COMMON RULES
all: cleanAll build show

cleanAll: clean
	$(RM) *.pdf

clean:
	$(RM) *.toc *.log *.aux *.tdo

build: buildMain

show: main.pdf
	if test "${DESKTOP_SESSION}" = "plasma"; then \
		okular $< &> /dev/null & \
	else \
		evince $< &> /dev/null & \
	fi

# SPECIFIC RULES
buildMain: main.tex
	$(LATEX_BUILDER) $(BUILD_FLAGS) $< #> /dev/null
	$(LATEX_BUILDER) $(BUILD_FLAGS) $< #> /dev/null
