# api documentation for  [brunch (v2.10.9)](http://brunch.io/)  [![npm package](https://img.shields.io/npm/v/npmdoc-brunch.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-brunch) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-brunch.svg)](https://travis-ci.org/npmdoc/node-npmdoc-brunch)
#### Fast front-end web app build tool with simple declarative config, seamless incremental compilation for rapid development, an opinionated pipeline and workflow, and core support for source maps

[![NPM](https://nodei.co/npm/brunch.png?downloads=true)](https://www.npmjs.com/package/brunch)

[![apidoc](https://npmdoc.github.io/node-npmdoc-brunch/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-brunch_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-brunch/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-brunch/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-brunch/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Brunch team",
        "url": "http://brunch.io"
    },
    "bin": {
        "brunch": "./bin/brunch"
    },
    "bugs": {
        "url": "https://github.com/brunch/brunch/issues"
    },
    "dependencies": {
        "anymatch": "~1.3",
        "anysort": "~1.0",
        "check-dependencies": "~1.0.1",
        "chokidar": "^1.6",
        "coffee-script": "~1.11",
        "commander": "~2.9",
        "commonjs-require-definition": "~0.6.2",
        "debug": "~2.2",
        "deppack": "~0.7",
        "deps-install": "~0.1",
        "fcache": "~0.3",
        "init-skeleton": "~1.0",
        "loggy": "~1.0.2",
        "micro-es7-shim": "^0.1",
        "micro-promisify": "~0.1",
        "mkdirp": "~0.5",
        "promise.prototype.finally": "^2",
        "read-components": "~0.7",
        "serve-brunch": "~0.2",
        "since-app-start": "~0.3",
        "skemata": "~0.1",
        "source-map": "~0.5",
        "universal-path": "^0.1"
    },
    "description": "Fast front-end web app build tool with simple declarative config, seamless incremental compilation for rapid development, an opinionated pipeline and workflow, and core support for source maps",
    "devDependencies": {
        "ava": "~0.16",
        "eslint": "^3",
        "eslint-config-brunch": "^1",
        "fixturify": "^0.2",
        "fs-extra": "^0.30",
        "nyc": "^6.4.2",
        "rewire": "^2.5",
        "test-console": "^1"
    },
    "directories": {},
    "dist": {
        "shasum": "a74bb5aef87fa87ce0dd4ca4f996610204358d30",
        "tarball": "https://registry.npmjs.org/brunch/-/brunch-2.10.9.tgz"
    },
    "engines": {
        "node": ">= 4.0",
        "npm": ">= 3.0"
    },
    "eslintConfig": {
        "extends": "brunch"
    },
    "files": [
        "bin",
        "lib"
    ],
    "gitHead": "9184f2d6c6487a99c9819bc3b4e5ce1051c76038",
    "homepage": "http://brunch.io/",
    "keywords": [
        "assembler",
        "builder",
        "stack",
        "pipeline",
        "build tool",
        "workflow",
        "source map",
        "incremental",
        "config",
        "react",
        "webpack",
        "browserify",
        "grunt",
        "gulp",
        "broccoli",
        "backbone",
        "ember",
        "angular",
        "chaplin",
        "html5"
    ],
    "license": "MIT",
    "main": "./lib/index",
    "maintainers": [
        {
            "name": "tosh",
            "email": "tosh@blossom.io"
        },
        {
            "name": "nikgraf",
            "email": "nik@deck.cc"
        },
        {
            "name": "paulmillr",
            "email": "paul@paulmillr.com"
        },
        {
            "name": "es128",
            "email": "elan.shanker+npm@gmail.com"
        }
    ],
    "name": "brunch",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/brunch/brunch.git"
    },
    "scripts": {
        "lint": "eslint bin/brunch lib test",
        "lint:fix": "eslint --fix bin/brunch lib test",
        "test": "npm run lint && LOGGY_STACKS=1 ava -s --verbose --fail-fast",
        "test:coverage": "nyc ava -s && nyc report --reporter=html"
    },
    "version": "2.10.9"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module brunch](#apidoc.module.brunch)
1.  [function <span class="apidocSignatureSpan">brunch.</span>build ()](#apidoc.element.brunch.build)
1.  [function <span class="apidocSignatureSpan">brunch.</span>new (rootPath, options)](#apidoc.element.brunch.new)
1.  [function <span class="apidocSignatureSpan">brunch.</span>watch ()](#apidoc.element.brunch.watch)



# <a name="apidoc.module.brunch"></a>[module brunch](#apidoc.module.brunch)

#### <a name="apidoc.element.brunch.build"></a>[function <span class="apidocSignatureSpan">brunch.</span>build ()](#apidoc.element.brunch.build)
- description and source-code
```javascript
build = function () { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.brunch.new"></a>[function <span class="apidocSignatureSpan">brunch.</span>new (rootPath, options)](#apidoc.element.brunch.new)
- description and source-code
```javascript
(rootPath, options) => {
  checkLegacyNewSyntax(options);

  const initSkeleton = require('init-skeleton').init;
  const skeleton = options.skeleton ||
    process.env.BRUNCH_INIT_SKELETON ||
    defaultSkeleton;

  return initSkeleton(skeleton, {
    logger,
    rootPath,
    commandName: 'brunch new',
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.brunch.watch"></a>[function <span class="apidocSignatureSpan">brunch.</span>watch ()](#apidoc.element.brunch.watch)
- description and source-code
```javascript
watch = function () { [native code] }
```
- example usage
```shell
...
  initWatcher(watchedPaths) {
const isDebug = !!process.env.DEBUG;
const config = this.config._normalized;
const paths = config.paths;
const isConfig = path => paths.allConfigFiles.includes(path);

speed.profile('Loaded watcher');
this.watcher = chokidar.watch(watchedPaths, Object.assign({
  ignored,
  persistent: config.persistent,
}, config.watcher))
  .on('error', error => {
    // TODO: Watch error.
    logger.error(error);
  })
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
