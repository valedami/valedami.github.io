images=$(wildcard ../images/*.jpg)
stills=$(wildcard ../_stills/*.jpg)
thumbs=$(patsubst ../images/%,../thumbs/%,$(images)) \
       $(patsubst ../_stills/%,../thumbs/%,$(stills))

all: $(thumbs)

../thumbs/%: ../images/% Makefile
	convert -resize x100 "$<" "$@"

../thumbs/%: ../_stills/% ../_stills/overlay.png Makefile
	convert -resize x100 "$<" "$@"
	composite -gravity center ../_stills/overlay.png "$@" "$@"

.PHONY: all

# vim:noexpandtab
