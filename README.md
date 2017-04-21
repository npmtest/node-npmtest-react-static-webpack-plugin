# npmtest-react-static-webpack-plugin

#### basic test coverage for  react-static-webpack-plugin (v2.1.0)  [![npm package](https://img.shields.io/npm/v/npmtest-react-static-webpack-plugin.svg?style=flat-square)](https://www.npmjs.org/package/npmtest-react-static-webpack-plugin) [![travis-ci.org build-status](https://api.travis-ci.org/npmtest/node-npmtest-react-static-webpack-plugin.svg)](https://travis-ci.org/npmtest/node-npmtest-react-static-webpack-plugin)

#### Build full static sites using React, React Router and Webpack

[![NPM](https://nodei.co/npm/react-static-webpack-plugin.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/react-static-webpack-plugin)

| git-branch : | [alpha](https://github.com/npmtest/node-npmtest-react-static-webpack-plugin/tree/alpha)|
|--:|:--|
| coverage : | [![istanbul-coverage](https://npmtest.github.io/node-npmtest-react-static-webpack-plugin/build/coverage.badge.svg)](https://npmtest.github.io/node-npmtest-react-static-webpack-plugin/build/coverage.html/index.html)|
| test-report : | [![test-report](https://npmtest.github.io/node-npmtest-react-static-webpack-plugin/build/test-report.badge.svg)](https://npmtest.github.io/node-npmtest-react-static-webpack-plugin/build/test-report.html)|
| build-artifacts : | [![build-artifacts](https://npmtest.github.io/node-npmtest-react-static-webpack-plugin/glyphicons_144_folder_open.png)](https://github.com/npmtest/node-npmtest-react-static-webpack-plugin/tree/gh-pages/build)|

- [https://npmtest.github.io/node-npmtest-react-static-webpack-plugin/build/coverage.html/index.html](https://npmtest.github.io/node-npmtest-react-static-webpack-plugin/build/coverage.html/index.html)

[![istanbul-coverage](https://npmtest.github.io/node-npmtest-react-static-webpack-plugin/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fcoverage.lib.html.png)](https://npmtest.github.io/node-npmtest-react-static-webpack-plugin/build/coverage.html/index.html)

- [https://npmtest.github.io/node-npmtest-react-static-webpack-plugin/build/test-report.html](https://npmtest.github.io/node-npmtest-react-static-webpack-plugin/build/test-report.html)

[![test-report](https://npmtest.github.io/node-npmtest-react-static-webpack-plugin/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Ftest-report.html.png)](https://npmtest.github.io/node-npmtest-react-static-webpack-plugin/build/test-report.html)

- [https://npmdoc.github.io/node-npmdoc-react-static-webpack-plugin/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-react-static-webpack-plugin/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-react-static-webpack-plugin/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-react-static-webpack-plugin/build/apidoc.html)

![npmPackageListing](https://npmtest.github.io/node-npmtest-react-static-webpack-plugin/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmtest.github.io/node-npmtest-react-static-webpack-plugin/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "name": "react-static-webpack-plugin",
    "version": "2.1.0",
    "description": "Build full static sites using React, React Router and Webpack",
    "license": "MIT",
    "repository": "iansinnott/react-static-webpack-plugin",
    "main": "dist/index.js",
    "author": {
        "name": "Ian Sinnott",
        "url": "iansinnott.com"
    },
    "scripts": {
        "lint": "eslint src",
        "lint:example": "eslint example/**/src",
        "test": "npm run lint && npm run flowcheck && npm run build && npm run test:unit",
        "test:unit": "cross-env NODE_ENV=production ava --verbose test.js example/**/test.js",
        "flowcheck": "flow check",
        "watch": "babel -w -d dist src",
        "start": "npm run watch",
        "clean": "rimraf dist",
        "build": "mkdir -p dist && npm run clean && npm run build:compile",
        "build:compile": "babel -d dist src",
        "bump:patch": "npm version patch -m \"v%s\"",
        "bump:minor": "npm version minor -m \"v%s\"",
        "bump:major": "npm version major -m \"v%s\"",
        "bump": "npm run bump:patch",
        "preversion": "npm test",
        "postversion": "git push && git push --tags",
        "prepublish": "npm run build"
    },
    "ava": {
        "require": [
            "babel-register"
        ],
        "babel": "inherit"
    },
    "keywords": [
        "react",
        "react-router",
        "webpack",
        "static",
        "generator"
    ],
    "dependencies": {
        "bluebird": "^3.4.1",
        "debug": "^2.2.0",
        "jsdom": "^9.9.1",
        "lodash": "^4.11.1"
    },
    "devDependencies": {
        "ava": "^0.17.0",
        "babel": "^6.3.26",
        "babel-cli": "^6.3.17",
        "babel-core": "^6.18.2",
        "babel-eslint": "^7.1.1",
        "babel-preset-es2015": "^6.3.13",
        "babel-preset-react": "^6.3.13",
        "babel-preset-stage-1": "^6.5.0",
        "babel-register": "^6.8.0",
        "cross-env": "^3.1.3",
        "eslint": "^3.10.2",
        "eslint-config-zen": "^2.0.0",
        "eslint-plugin-flowtype": "^2.25.0",
        "eslint-plugin-react": "^6.7.1",
        "extract-text-webpack-plugin": "^1.0.1",
        "flow-bin": "^0.37.4",
        "history": "^4.4.0",
        "react": "^15.2.1",
        "react-dom": "^15.2.1",
        "react-redux": "^5.0.0",
        "react-router": "^3.0.0",
        "redux": "^3.5.2",
        "rimraf": "^2.5.0",
        "webpack": "^1.13.1"
    },
    "peerDependencies": {
        "extract-text-webpack-plugin": ">= 1.0.1 < 3",
        "history": ">= 4 < 5",
        "react": ">= 0.14.0",
        "react-dom": ">= 0.14.0",
        "react-router": ">= 2.4.0 < 4",
        "webpack": ">= 1.13.1 < 3"
    }
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
