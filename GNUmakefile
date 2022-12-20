-:docs
.PHONY: docs
docs:-
	@mkdir -p docs
	pushd icons && ./make-sizes.sh && popd
	./make-icns.sh
	@install -v README.md docs/index.md
	@sed 's/images/.\/images/' README.md > docs/index.md
	@cp -R ./icons ./docs/
