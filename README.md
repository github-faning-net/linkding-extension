# linkding extension

Companion extension for the self-hosted [linkding](https://github.com/sissbruecker/linkding) bookmark service.

*NOTE: Currently only developed and tested for Firefox. Will try to add Chrome support later*

**Screenshot**

![Screenshot](/docs/screenshot.png?raw=true "Screenshot")

## Installation

*TODO: Link to extension stores as soon as extension is published*

## Manual installation

### Firefox

Run the build as described below and then follow the instructions [here](https://developer.mozilla.org/en-US/docs/Mozilla/Add-ons/WebExtensions/Your_first_WebExtension#installing) to load it into Firefox.

### Chrome

*TODO*

## Build

**Requirements**
- Latest LTS Node version
- Latest LTS NPM version
- bash
- web-ext

First ensure that web-ext is installed, which is a tool for building distribution packages of Firefox extensions:
```
npm install --global web-ext
```

Then run the following bash script to generate a build (might need to make the file executable using `chmod +x build.sh`):
```
./build.sh
```

The script does:
- Install all dependencies using NPM
- Runs rollup to transpile and minify source files, with output written to `build`
- Run web-ext to package the extension for uploading to the Mozilla addon store

After the build the root directory contains the complete, unpackaged extension. Use the `manifest.json` file to load it manually into the browser.

The packaged extension can be found in the `web-ext-artifacts` folder.