SOURCES=wire-black.svg wire-blue.svg wire-brown.svg wire-color.svg wire-green-yellow.svg wire-green.svg wire-grey.svg wire-orange.svg wire-purple.svg wire-red.svg wire-white.svg wire-yellow.svg
TARGETS=$(SOURCES:.svg=.png)

all: $(TARGETS)

%.png: %.svg
	inkscape \
		--export-type=png \
		--export-filename=$@ \
		--export-width=100 \
    	--export-background-opacity=0 \
		$<

.PHONY: clean