# Minimal makefile for Sphinx documentation
#

# You can set these variables from the command line, and also
# from the environment for the first two.
SPHINXOPTS    ?=
SPHINXBUILD   ?= sphinx-build
SOURCEDIR     = .
BUILDDIR      = _build
INSTALLDIR    = .

# Internal variables.
PAPEROPT_a4     = -D latex_paper_size=a4
PAPEROPT_letter = -D latex_paper_size=letter
ALLSPHINXOPTS   = -d $(BUILDDIR)/doctrees $(PAPEROPT_letter) $(SPHINXOPTS) .


.PHONY: help html pdf all help clean dirhtml latex sphinxhelp

html:
	$(SPHINXBUILD) -b html $(ALLSPHINXOPTS) $(BUILDDIR)/html
	@echo
	@echo "Build finished. The HTML pages are in $(BUILDDIR)/html."


all: html pdf
	$(SPHINXBUILD) -b html $(ALLSPHINXOPTS) _build/html
	cd $(BUILDDIR)/latex && make all-pdf
	@echo
	@echo "Build finished. The HTML pages are in _build/html."

pdf: latex
	cd $(BUILDDIR)/latex && make all-pdf
	cp -pr $(BUILDDIR)/latex/see_facilities.pdf $(BUILDDIR)/html/see_facilities.pdf

help:
	@echo "Please use \`make <target>' where <target> is one of"
	@echo "  html      to make standalone HTML files"
	@echo "  pdf       pdf from latex version"
	@echo "  all       html, pdf, and doc.zip"
	@echo "  clean     to remove all output"
	@echo "  sphinxhelp  for full sphinx help"

sphinxhelp:
	@$(SPHINXBUILD) -M help "$(SOURCEDIR)" "$(BUILDDIR)" $(SPHINXOPTS) $(O)

latex:
	$(SPHINXBUILD) -b latex $(ALLSPHINXOPTS) _build/latex
	@echo
	@echo "Build finished; the LaTeX files are in _build/latex."
	@echo "Run \`make all-pdf' or \`make all-ps' in that directory to" \
	      "run these through (pdf)latex."

latexpdf:
	$(SPHINXBUILD) -b latex $(ALLSPHINXOPTS) _build/latex
	@echo "Running LaTeX files through pdflatex..."
	make -C _build/latex all-pdf
	@echo "pdflatex finished; the PDF files are in _build/latex."

clean:
	-rm -rf _build/*
