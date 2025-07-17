##
# Presentación 2025-2S
#
# @file
# @version 0.2

# Makefile for compiling a LaTeX Beamer presentation with LuaLaTeX and Biber

# Name of your main .tex file (without extension)
MAIN = sample

# LaTeX compiler
LATEX = lualatex

# Flags
LATEX_FLAGS = -interaction=nonstopmode -shell-escape

# Default target
all: $(MAIN).pdf

# Compile with Biber
$(MAIN).pdf: $(MAIN).tex $(MAIN).bib
	$(LATEX) $(LATEX_FLAGS) $(MAIN).tex
	biber $(MAIN)
	$(LATEX) $(LATEX_FLAGS) $(MAIN).tex
	$(LATEX) $(LATEX_FLAGS) $(MAIN).tex

# Clean auxiliary files
clean:
	rm -f *.aux *.log *.bbl *.blg *.bcf *.run.xml *.nav *.out *.snm *.toc *.vrb *.lof *.lot *.fls *.fdb_latexmk *.synctex.gz

# Full clean (including PDF)
distclean: clean
	rm -f $(MAIN).pdf

# end
