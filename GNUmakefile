-:docs
.PHONY: docs
docs:
	@mkdir -p docs
	cd icons && ./make-sizes.sh && cd ..
	./make-icns.sh
	@install -v README.md docs/index.md
	@sed 's/images/.\/images/' README.md > docs/index.md
	@cp -Rf ./icons ./docs/
	@cp -RfP ./icons ../ || echo
	@ln -sf icons/512x512.png icon-512x512.png
init:initialize
initialize:
	cd scripts && ./initialize && cd ..
nuke-docker:
	cd scripts && ./nuke-docker && cd ..
