BIN = ./node_modules/.bin

SRC_JS = $(shell find src -name "*.js")
DIST_JS = $(patsubst src/%.js, dist/%.js, $(SRC_JS))

js: $(DIST_JS)

$(DIST_JS): dist/%.js: src/%.js
	mkdir -p $(dir $@)
	cp package.json $(dir $@)
	cp ../readme.md $(dir $@)
	"$(BIN)/babel" $< -o $@
