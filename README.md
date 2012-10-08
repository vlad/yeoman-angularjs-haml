
## Introduction

Build, test, and deploy web apps with HAML, AngularJS, and Yeoman!
Thanks to LiveReload in yeoman, HAML files are converted to HTML and reloaded in the browser window after every save.

## Installation

To use, first install grunt-haml locally:

$ npm install grunt-haml

Secondly, whether you use this as a starter project or copy-paste the files into an existing one, be sure to rename every mention of "example" in index.haml, main.js, and example.js (including the file name!) to whatever app name you want.

## Credits

Original idea by @nicolai86 from https://github.com/yeoman/yeoman/issues/399

I (@vlad) mainly converted the templates to HAML, and published this for my own projects.  I hope this helps!

## Issues

### Haml.js is not quite the real HAML

You should know that haml.js, the JavaScript implementation of haml used by grunt-haml, has many differences from ruby HAML.  For example,
- it seems to remove blank attributes, which is why you see the ng-view attribute assigned "see-readme" in index.haml
- it doesn't support the :plain filter; on the other hand, HTML comments don't appear to need a filter.
- it mangles the following comment from HTML5 Boilerplate:
  <!--[if gt IE 8]><!--> <html class="no-js"> <!--<![endif]-->
  which is why <!-- see readme --> appears in its place.

These are minor annoyances for now.  Ping me if you find that another HAML JavaScript library, like https://github.com/uglyog/clientside-haml-js, is better.

### Other annoyances

- each individual haml file must be listed in the Gruntfile.js (again, due to grunt-haml).

## Links

http://yeoman.io
http://angularjs.org
https://github.com/andrewrjones/grunt-haml
https://github.com/creationix/haml-js