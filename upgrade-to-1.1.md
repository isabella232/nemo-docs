# Upgrade to Nemo 1.1

Nemo 1.1 adds [selenium-webdriver ~2.46.1](https://github.com/SeleniumHQ/selenium/blob/master/javascript/node/selenium-webdriver/CHANGES.md) 
support. Since browser support changes so dramatically between selenium-webdriver 2.44 and 2.46.1, it makes sense to release a new minor 
version of nemo to help people make a clean transition when they are ready.

There will be an alpha-testing period while we verify support (see smoke testing section below). While the alpha-testing period 
commences, you can use the alpha versions listed below to test out the new selenium-webdriver. It is not anticipated that there 
will be drastic (or at all breaking) changes to any nemo API during this alpha period.

## Alpha testing versions

* `nemo: ^v1.1.0-alpha.1`
* `nemo-view: ^v1.3.0-alpha.1`
* `nemo-screenshot: ^v1.2.0-alpha.1`
 
## Upgraded version ranges

If you're using the carat identifier, (e.g. `"nemo": "^1.0.0"`) then you will get nemo@1.1.x when it moves out of alpha. The same goes for any 
plugins you're using.

If you want to opt-out of the new webdriver version, then use the tilde identifier (e.g. `"nemo": "~1.0.0"`) to remain on nemo@1.0.x

None of this will be relevant, however, until Nemo 1.1 moves out of alpha and is published at version 1.1.1.

## Plugins and peerDependency

If you find that a plugin complains about a peerDependency on an older version of nemo (such as 1.0.0), then bug 
that plugin's author to specify a range instead, which includes the older and newer versions.

e.g.

```js
   "peerDependencies": {
        "nemo": ">= 1.0.0"
   }
```

## More information on the selenium-webdriver 2.46.1 release

* http://www.joecolantonio.com/2015/06/05/selenium-webdriver-2-46-0-released/

## Browser/OS combos smoke-tested

### Mac OS X

* Firefox 40.0.3
* Chrome 45.0.2454.85 (Official Build) (64-bit)
  * requires chromedriver 2.19 ([More info](https://sites.google.com/a/chromium.org/chromedriver/downloads))
* Safari 8.0.8 (10600.8.9)
  * requires SafariDriver 2.45 ([More info](https://github.com/SeleniumHQ/selenium/wiki/SafariDriver))
  * ran into an unexpected StaleElementReference Error. Didn't investigate any further and will not until I'm told that 
  someone requires Safari support
   
### Windows OS

none yet

### Linux OS

none yet