---
layout: post
title:  "Pinitto.me gets a security upgrade"
date:   2013-06-07 12:00:00
tags: security ssl beast https 
categories: security
---

As of this moment the pinitto.me proxy code now protects users from the TLS BEAST attack.

What does this mean? Well as an every day user you won’t notice any difference but a BEAST attack is a way that a third party can decypt the secure connection between pinitto.me’s servers and your browser.

We use a wrapper around nodejitsu’s [node-http-proxy](http-proxy) module in order to serve requests to the actual pinitto.me node.js application, with the code being available on github: [pinitto.me proxy code](pinittome-proxy).

If you are interested in finding more out about the updated code and the fix please see lead developer [Lloyd Watkin](lloydwatkin)'s post on the fix: [Protect nodejs from TLS BEAST attack](beast-attack).

[http-proxy]: "https://github.com/nodejitsu/node-http-proxy"
[beast-attack]: "http://www.evilprofessor.co.uk/634-protecting-node-js-from-beast-tls-attack/"
[lloydwatkin]: "https://twitter.com/lloydwatkin"
[pinittome-proxy]: "https://github.com/pinittome/proxy
