# These variables can be set from the command line
# SPHINXOPTS and SPHINXBUILD can be set from the environment
SPHINXOPTS    ?=
SPHINXBUILD   ?= sphinx-build
SOURCEDIR     = .
BUILDDIR      = _build

# "make" without arguments is like "make help"
.PHONY: help
help:
	@$(SPHINXBUILD) -M help "$(SOURCEDIR)" "$(BUILDDIR)" $(SPHINXOPTS) $(O)

.PHONY: latex-logo
latex-logo:
	rsvg-convert --format=pdf --output=latex-logo.pdf _static/images/boards/arduino-uno.svg

# Catch-all target: route all unknown targets to Sphinx
# $(O) is a shortcut for $(SPHINXOPTS)
.PHONY: Makefile
%: Makefile
	@$(SPHINXBUILD) -M $@ "$(SOURCEDIR)" "$(BUILDDIR)" $(SPHINXOPTS) $(O)
