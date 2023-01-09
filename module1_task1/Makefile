space=$(subst ,, )
var=$(subst $(space),-,$(POST_TITLE))

build:
	hugo --destination ./dist

post:
	hugo new posts/$(var)/$(POST_NAME).md -f
	@mv posts/$(var)/$(POST_NAME).md content/posts/
	@rm content/posts/$(var)

clean:
	rm -r dist/


