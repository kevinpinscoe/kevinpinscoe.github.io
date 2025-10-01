PORT   ?= 4040
LRPORT ?= 35740
HOST   ?= 127.0.0.1

.PHONY: serve build clean

serve:
	@echo "Serving at http://$(HOST):$(PORT) (livereload: $(LRPORT))"
	bundle exec jekyll serve \
	  --host $(HOST) --port $(PORT) \
	  --livereload --livereload-port $(LRPORT) \
	  --destination docs --trace --verbose

build:
	bundle exec jekyll build -d docs --trace --verbose

clean:
	rm -rf _site docs .jekyll-cache
