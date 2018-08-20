# Change Log

## Unreleased
* Add support for class based elements and inlined templates
  * `class MyElement extends Polymer.Element {}` + `<dom-module id="my-element">`
  * ```Polymer({is: 'legacy-inline-element', _template: Polymer.html``})```;
  * ```class MyInlineElement extends Polymer.Element {static get template(){ return Polymer.html``}}```

## [0.3.0] - 2018-08-10
* Upgrade to using @webcomponents/shadydom for Polymer v2 support
* Use polymer-analyzer instead of hydrolysis
* Remove vulcanize step of Polymer v1
* Add `--polymer-version` flag to specify v1 or v2
  * `--polymer-version=2` is default
* Also mark `<template>` in `<dom-module>` with `css-build` attribute
* Rewrite tests to test Polymer v1 and Polymer v2
* **NOTE**: Only `Polymer({})` elements are supported for now!

## [0.2.2] - 2017-10-17
### Fixed
* Don't distribute development git submodule

## [0.2.1] - 2017-10-17
### Fixed
* Removed broken package-lock.json that was breaking tests

## [0.2.0] - 2017-10-17
### Fixed
* Fix selectors of the form `html:not([foo]) *`
* Support the `:dir()` selector

## [0.1.1] - 2017-05-23
### Fixed
* Fix `--no-inline-includes` to collect includes when collating styles

## [0.1.0] - 2017-03-07
### Fixed
* Also support `name="..."` and `is="..."` when identifying `<dom-module>`s
* Handle Polymer 1.7+ Hybrid elements using `::slotted()` syntax

## [0.0.9] - 2017-02-23
### Fixed
* Respin node module

## [0.0.8] - 2017-02-23
### Added
* Added `--no-inline-includes` to optionally not inline `<style include>` elements

### Fixed
* Fixed ordering of when `<custom-style>` is processed

## [0.0.7] - 2016-11-01

### Added
* Don't process CSS in templates with a `preserve-content` attribute.

### Fixed
* Fix support for node v4. (Don't use Array.includes)
* Improve shimming of incorrect `var()` calls, where the fallback value is a custom property that doesn't itself use `var()`
* Improve support for node v6 by updating to the `command-line-args` v3 branch.

