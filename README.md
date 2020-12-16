# Behold: Module Federation

This is a demo application demoing very basic module federation principles. Currently all imports happen against localhost modules. Eventually this demo will include loading resources from files outside of the file structure.

## Setup

To run this demo, clone this repo then `cd` into the `host` and `client` apps in different terminal tabs.

In each terminal app, run `yarn` to install dependencies. Yarn is important because we are using it's `resolutions` key in the `package.json` file to update the webpack dependency used by nextjs from 4.x to 5.x (which is the version with module federation). NPM does not have this ability by default, but there is a [library](https://www.npmjs.com/package/npm-force-resolutions) that adds this capability.

After installing dependencies, run `yarn dev` to start the apps.

With both apps running, open [localhost](https://localhost:3000) and see the beauty of the incredibly basic web app. The navbar (non-functional) was imported from the `client` app, while everything else on the page is part of `host`! how rad is that!

## Information

There were a few key things that needed to happen in order to set up this module federation system. I followed [this tutorial](https://dev.to/hamatoyogi/let-s-build-micro-frontends-with-nextjs-and-module-federation-41en), and it works excellently!
