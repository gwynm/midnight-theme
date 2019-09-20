# Midnight Theme - forked by gwynm

A darker dark.

## Build instructions

npm install
bundle install
grunt watch

## Dev workflow

cd dist
ruby -run -ehttpd . -p8000
Now go to Extensions -> Import Extension -> http://localhost:8000/ext.json . Note that you need to press enter; clicking Import Extension again will fail.  

Make changes to src/main.scss. Grunt watch will pick them up and update dist/dist.css .

You'll need to remove the extension from Standard Notes and re-add it (and activate it) to see changes. 

Note that you need to do this on the Desktop app, or a web app running locally; CORS will prevent you from loading a local extension on the hosted webapp.

There's some really aggressive caching going on. To see changes, you'll need to change the name of the css file referenced in ext.json. (no need to change the name of ext.json itself, or the version number). 