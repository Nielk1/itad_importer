## Collection Import Script for IsThereAnyDeal.com

This userscript adds "Export to ITAD" buttons to the following online game
vendors who do not provide a way for sites like IsThereAnyDeal.com to query
user game lists remotely.

It is currently in **beta** and any bugs should be reported in the issue
tracker.

Currently supported vendors are:

* [DotEmu](http://www.dotemu.com)
* [GOG.com](http://www.gog.com)
* [Humble Store](http://www.humblebundle.com) (anything in your Humble Library)
* [IndieGameStand](http://www.indiegamestand.com)
* [ShinyLoot](http://www.shinyloot.com)

Pending a proper website, [screenshots](http://imgur.com/a/6FG6B) are available
on imgur.

### Installation

1. Install [Greasemonkey](https://addons.mozilla.org/en-US/firefox/addon/greasemonkey/)
   in [Firefox](http://getfirefox.com/) (Tampermonkey in Chrome should also work
   but hasn't yet been tested)
2. Click the Javascript file here and then click the "Raw" button
3. You should be presented with a dialog offering to install the script.

(This script will be uploaded to userscript repositories like
[Greasy Fork](https://greasyfork.org/) once it is reasonable apparent that
rapid patching is no longer a concern.)

### Development

The authoritative copy of this script is the CoffeeScript source file. Patches
against the generated JavaScript may or may not be accepted at the developers'
discretion.

(We have to rewrite them in CoffeeScript, so they'll have to be worthwhile.)

The official method for developing this script is as follows:

1. Install the release version of the script in your browser
2. Install Node.js
3. Run `npm install -g coffee-script coffeelint docco`
4. Run `./develop.sh`
5. Saving changes to the CoffeeScript source will now regenerate the installed
   copy of the script.
6. When you're finished, hit Ctrl+C
7. `develop.sh` will regenerate the in-repository JavaScript and code
   documentation.
8. Commit the updated built files

However, if you do not have a Unixy machine handy, this quick and dirty method
can also be used:


 1. Open http://coffeescript.org/
 2. Open the "Try CoffeeScript" tab.
 3. Use the browser's Developer Tools to add a `contentEditable`
  attribute to the `<pre>` tag for the right pane so you can use
  <kbd>Ctrl+A</kbd> <kbd>Ctrl+C</kbd> to quickly copy everything.
 4. Install the stable version of this userscript and use Greasemonkey's
  edit button to open up the version it's using so you can test changes
  simply by copying JS from "Try CoffeeScript" to the editor, clicking
  save, and reloading the page in the browser.
 5. Use the "Try CoffeeScript" button to switch back and forth between
  code and reference materials.

