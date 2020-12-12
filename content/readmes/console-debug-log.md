---
title: console-debug-log
date: 2020-12-12T08:27:16+0000
draft: false
---
<p align="center">
<a href="https://dscvit.com">
	<img src="https://user-images.githubusercontent.com/30529572/72455010-fb38d400-37e7-11ea-9c1e-8cdeb5f5906e.png" />
</a>
	<h2 align="center"> Debug logger </h2>
	<h4 align="center"> Node.js tooling to log only in debugging environments <h4>
</p>

--- 

# Functionalities
- [x] Log entries only when DEBUG environment variable is set.
- [ ] Customizable environment variable name for debugging.

# Instructions to run

* Pre-requisites:
	- Node.js
    - NPM

* Directions to install: 
    - Navigate to your project directory. 
	- Run `npm i -s console-debug-log`


# Usage instructions
Usage is very straightforward after installation.

## Require in the package
```js
const log = require('console-debug-log');
```

## Log wherever needed
```js
log.debug('Sample Text');
// will print out "Sample Text" to stdout if the DEBUG environment variable is set
```

# Contributors

* [ Pragati ](https://github.com/Pragati1610)
* [ Amogh ](https://github.com/ATechnoHazard)

## License

[![License](http://img.shields.io/:license-mit-blue.svg?style=flat-square)](http://badges.mit-license.org)

<p align="center">
	Made with :heart: by <a href="https://dscvit.com">DSC VIT</a>
</p>
