---
layout: content
title: "RendrJS"
---

<a href="http://github.com/rendrjs/rendr">
  <img class="top-img" src="http://cl.ly/image/272q3f1u313b/Rendr-logotype.png" width="395" height="100">
</a>

[![travis-ci status](https://secure.travis-ci.org/rendrjs/rendr.png)](http://travis-ci.org/#!/rendrjs/rendr/builds)
[![Dependency Status](https://david-dm.org/rendrjs/rendr.png)](https://david-dm.org/rendrjs/rendr)
[![Coverage Status](https://coveralls.io/repos/rendrjs/rendr/badge.png)](https://coveralls.io/r/rendrjs/rendr)


Rendr is a small library that allows you to run your [Backbone.js](http://backbonejs.org/) apps seamlessly on both the client and the server. Allow your web server to serve fully-formed HTML pages to any deep link of your app, while preserving the snappy feel of a traditional Backbone.js client-side MVC app.

<h2 id="getting-started">Getting Started</h2>

To see how to use Rendr to build a simple web app, check out the [examples](https://github.com/rendrjs/rendr-examples) repository for a number of different ways to set up a Rendr app.

Check out the [blog post](http://nerds.airbnb.com/weve-launched-our-first-nodejs-app-to-product) for a more thorough introduction to Rendr.

<h2 id="premise">The Premise</h2>

We believe there has to be a better way to build rich web apps today. In the last few years, we've seen more of the application moved to the client-side, with JavaScript representations of views, templates, and models. This enables us to build interactive, native-style single-page apps, but splitting your app into two distinct codebases (often using different languages for client and server) also creates challenges for performance, maintainability, and SEO.


<h2 id="goals">The Goals</h2>

Rendr is intended to be a building block along the way to this envisioned future of web apps that can be run on either side of the wire according to the needs of your application.

Some specific design goals:

* Write application logic agnostic to environment
* Minimize `if (server) {...} else {...}`
* Talk to RESTful API
* Library, not a framework
* Hide complexity in library
* No server-side DOM
* Simple Express middleware

<h2 id="not-included">What's Not Included</h2>

### Express app

Rather than owning your entire Express app, Rendr simply provides some useful middleware that you can mount into your existing Express app.

### Asset Bundling

Asset bundling and serving are outside of Rendr's scope. However, it does have some specific requirements for JavaScript packaging to support modules that are accessible in the CommonJS style on both the client and server. The example app uses Stitch for this, though you could also do this with other tools, such as Browserify.

## Notes

Rendr uses the native ECMAScript 5 methods `Array.prototype.map`, `Function.prototype.bind`, `Object.create`, etc. If you plan to support older browsers, such as IE<=8, you should include the lovely [es5-shim](https://github.com/kriskowal/es5-shim) (and es5-sham) libraries as client-side dependencies.

<h2 id="contributing">Contributing</h2>

We'd love to see what the community can come up with! There are no doubt a number of developers who are tackling this same problem, and we can learn from each other. If you have a bug fix or feature proposal, submit a pull request with a clear description of the change, plus tests.

Rendr was originally developed by [@braitz](https://github.com/braitz) and [@spikebrehm](https://github.com/spikebrehm), and now has a healthy list of [contributors](https://github.com/rendrjs/rendr/graphs/contributors).

## Reporting problems and getting help

Please use the [issue tracker][issues] to report bugs. For support with using
rendr, try asking in the [Google group][ggroup] or join #rendr on
irc.freenode.org.

[ggroup]: https://groups.google.com/forum/#!forum/rendrjs
[issues]: https://github.com/rendrjs/rendr/issues

## License

MIT

[![Bitdeli Badge](https://d2weczhvl823v0.cloudfront.net/rendrjs/rendr/trend.png)](https://bitdeli.com/free "Bitdeli Badge")

