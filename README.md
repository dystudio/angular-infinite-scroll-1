# angular-infinite-scroll

[![Build Status](https://travis-ci.org/srph/angular-infinite-scroll.svg?branch=master)](https://travis-ci.org/srph/angular-infinite-scroll)
[![Bower version](https://badge.fury.io/bo/angular-srph-infinite-scroll.svg)](http://badge.fury.io/bo/angular-srph-infinite-scroll)
[![Author | Shields.io](http://img.shields.io/badge/author-%40srph-blue.svg?style=flat-square)](http://twitter.com/_srph)
[![MIT license](http://img.shields.io/badge/license-MIT-brightgreen.svg)](http://opensource.org/licenses/MIT)

Another infinite scroll shit solution for AngularJS.

## Important Notes

Latest versions are still alpha and should not be used for production.

### Why another Infinite Scroll solution?

- [sroze/ngInfiniteScroll](https://github.com/sroze/ngInfiniteScroll) is an okay solution, however it seems to not support infinite scrolling for containers, and has oudated documentation.
- The author of the mentioned library is difficult to contact (no twitter, mail seems down, and busy according to his Github activity).
- Some part of the internal code just doesn't make sense to me.
- It Just Works™.
- Why not?
- I don't know at all.

One thing is that it's not better.

### Status

Current version is ```v0.1.0```. All tests are failing because I suck. Please send a PR, thanks.

**Todo**

- [/] Tests
- [x] Automation
- [/] Documentation
- [ ] Removal of jQuery as dependency
- [ ] Support for responsive apps (threshold, lel)

*Legend*: ```/```: almost -- ```x``` done

## Getting Started

Getting started is very easy!

**Requirements**

- AngularJS ```>=v1.2.0``` (Should work with)
- jQuery (at least) ```>=v.1.7``` (Planned in the future to be removed)

### Installation

```angular-infinite-scroll``` is available on **Bower**:

```
$ bower install angular-srph-infinite-scroll --save
```

***** *The purpose of the ```--save``` argument is to add it your bower file's dependencies.*

```angular-infinite-scroll``` is also available on CDN(s):

- **Raw GIT**
```html
<script src="https://cdn.rawgit.com/srph/angular-infinite-scroll/master/dist/angular-srph-infinite-scroll.js"></script>
<!-- min -->
<script src="https://cdn.rawgit.com/srph/angular-infinite-scroll/master/dist/angular-srph-infinite-scroll.min.js"></script>
```

**Include the script to your HTML file after jQuery and AngularJS** (must be in proper order).**

```html
<!-- other scripts -->
<script src="/path/to/jquery.js"></script>
<script src="/path/to/angular.js"></script>
<script src="/path/to/angular-srph-infinite-scroll.js"></script>
```

**Add the library module to one of your app module's dependencies.**

```js
angular.module('myApp', [/** other dependencies */, 'srph.infinite-scroll']);
```

### Usage

And then, use the directive on a container.

```html
<div srph-infinite-scroll="callback()"
  disabled="true"
  container="true"
  throttle="0"
  threshold="200">
</div>
```

You may check the API Reference (still being written).

## Contribution

All contributions are appreciated. Please simply file an issue first for any inquiry, proposal, or question to avoid closed pull-requests; useless work. Thanks.

```
=========      ================
| issue |  ->  | pull-request |
=========      ================
```

### Building

If you plan to contribute (put some fixes, add a feature, put some tests), then this is for you. Otherwise, I wouldn't recommend building the library from source (and probably won't make sense).

**Requirements**

1. ```nodejs```
2. ```npm```
3. ```bower```

If you are using a Debian-based Linux distro, you may install ```nodejs``` and ```npm``` by:

```bash
# nodejs-legacy since it properly registers to PATH
$ apt-get install nodejs-legacy npm
```

If you have restriction / access issues, simply add ```sudo``` (```sudo apt-get install ...```).

And then install ```bower``` and ```karma-cli``` which depends on nodejs and is registered through ```npm```.

```
$ npm install bower karma-cli  -g
```

Now, we'll start building the project itself.

Start by cloning this repository. Then run these commands to install the project's dependencies:

```bash
$ cd </path/to/project-root> # replace with the root dir of the project
$ npm install & bower install
```

Uglification / Testing:

```
$ npm run test # Run the tests
$ npm run build # Build / annotate (ng-annotate)
$ npm run uglify # Uglify
$ npm run start # (build and annotate)
```

If you would like to watch the files for the tests, install ```karma-cli``` (allows you to use ```karma``` on the cli).

```bash
$ npm install karma-cli 

# on root dir
$ karma start
```

### Coding Style

This was copy-pasted from [```ReactJS```'s contribution style guide](https://github.com/facebook/react/blob/master/CONTRIBUTING.md)

1. Use semicolons;
2. Commas last,
3. 2 spaces for indentation (no tabs)
4. Prefer ```'``` over ```"```
5. ```"use strict";```
6. 80 character line length
8. "Attractive"
9. Keep it simple, stupid

Do not forget to add tests!

## Acknowledgement

Primarily motivated and almost based on [sroze/ngInfiniteScroll](https://github.com/sroze/ngInfiniteScroll).

**angular-infinite-scroll** © 2014+, Kier Borromeo (srph). Released under the [MIT](http://mit-license.org/) License.<br>

> [srph.github.io](http://srph.github.io) &nbsp;&middot;&nbsp;
> GitHub [@srph](https://github.com/srph) &nbsp;&middot;&nbsp;
> Twitter [@_srph](https://twitter.com/_srph)
