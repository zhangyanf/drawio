# Building
draw.io consists of two parts, currently. The main part is the client-side JavaScript code. You can create the minified JavaScript using the default "all" task of the Ant build.xml file which you can execute by running ant in the etc/build folder of the repo.

Note, if you use just the client-side code, you'll be missing the Gliffy and .vsdx importers, the embed support, icon search and publishing to Imgur.

If you want to build the full war with the Java server-side code and the client-side JavaScript, invoke the "war" task in the Ant build.xml file. Deploy the resulting .war file to a servlet engine.

# Running locally in the browser

If you want to run draw.io locally, e.g. for development, you can use a local server (e.g. pythons python -m SimpleHTTPServer 8000) in the /war directory. Since draw.io enforces https by default, use a certificate or open draw.io’s index.html with the parameter https=0, (e.g. http://localhost:8000/index.html?offline=1&https=0).

# Running locally in electron

You can also run draw.io in electron for development purposes. Clone the mxgraph repo into a folder called "mxgraph2". The mxgraph2 folder needs to be a sibling folder of the draw.io repo. folder. Go the the war folder of your checkout of draw.io’s repo. Run npm install (which will download electron) and npm run, which will start draw.io in electron.