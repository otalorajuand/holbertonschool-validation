space=$(subst ,, )
var=$(subst $(space),-,$(POST_TITLE))

build:
	hugo new site dist
	curl -o ananke https://github.com/theNewDynamic/gohugo-theme-ananke/archive/master.zip
	@mv ananke dist/themes/
	echo "theme = 'ananke'" >> config.toml
	echo "publishDir = './dist'" >> config.toml

post:
	hugo new posts/$(var)/$(POST_NAME).md -f
	@mv posts/$(var)/$(POST_NAME).md content/posts/
	@rm content/posts/$(var)

clean:
	rm -r dist/


