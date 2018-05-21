# addTranslation
A project to translate english strings to json files using Yandex API Services.  Designed for SPA architecture.

### Usage ###

To start you need to create a yandex.json file in the same directory as your binary.

 	echo -e '{
    	"key":"YourAPIKey",
    	"path":"web/pages",
    	"languages":[
      		"es",
      		"ja"
    	]
  	}' > yandex.json
  	
### Adding a new translation from english string to languageX.###

Linux AMD64

	addTranslation myPage "SomeKey" "SomeValue"
	
Darwin

	addTranslationDarwin myPage "SomeKey" "SomeValue"
	
###  Building the Binaries ###

	bin/build
	
Output files will be located in dist.
	
###  Deploying to your project. ###

Copy the desired binary and yandex.json file to the root directory of your project.
	
### Output ###

Each "myPage" argument will create a sub folder located under the path key.  A file named i18n.json will be created.  This can then be imported using webpack or downloaded using a get request.
	



