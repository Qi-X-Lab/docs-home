---
title: &title Troubleshooting PUBLISH
description: &description This page helps you troubleshoot issues with PUBLISH.
head:
  - ['meta', {property: 'og:title', content: *title}]
  - ['meta', {property: 'og:image', content: 'https://qixlab.com/img/og/webcontainer-troubleshooting.png'}]
  - ['meta', {name: 'twitter:title', content: *title}]
  - ['meta', {name: 'twitter:description', content: *description}]
---

# {{ $frontmatter.title }}

This page helps you troubleshoot issues with PUBLISH.

## Cannot load native addon

Currently, PUBLISH can only execute languages that are natively supported on the Web, including JavaScript and WebAssembly. It is not possible to run [native addons](https://nodejs.org/api/addons.html) which are usually implemented using native languages such as C++, unless they can be compiled to WebAssembly. Therefore, loading native addons is disabled by default via [`--no-addons`](https://nodejs.org/api/cli.html#--no-addons) in PUBLISH. As a result, you may encounter an error that says: `Cannot load native addon because loading addons is disabled`.

The solution to this is to use an alternative to the native addon which is either fully implemented in JavaScript or can be compiled to WebAssembly.
