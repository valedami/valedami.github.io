origs=$(wildcard ../images/*)
thumbs=$(patsubst ../images/%,../thumbs/%,$(origs))

all: $(thumbs)

../thumbs/%: ../images/%
	convert -resize x128 "$<" "$@"

.PHONY: all

# vim:noexpandtab
