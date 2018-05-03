# Cross Platform PhaserJS Project

Writing programs is fun, but when you want or need to share your game with others, they may not be using the same Browser, or even same operating system.

You will need to consider the myriad of different screen resolution and aspect ratios.

Making your game cross platform means your app/game will work and scale to multiple devices screens.

## Table of Contents

<!-- toc -->

- [Make your project scale](#make-your-project-scale)
- [Device Input](#device-input)
- [Hosting your app](#hosting-your-app)
  * [Deploy to Github Pages](#deploy-to-github-pages)
  * [Hybrid App with Apache Cordova](#hybrid-app-with-apache-cordova)
- [Credits](#credits)

<!-- tocstop -->

## Make your project scale

- Set and Viewport in your main html document

```html
<meta name="viewport" content="width=device-width, initial-scale=1, maximum-scale=1, minimum-scale=1, user-scalable=no" />
```

Additional information on the viewport meta tag can be found on `Mozilla Developer Networks website`

## Device Input

In order to truely have a good cross-platform experience you need to consider how people will interact with your app.  You develop on a computer, you likely have a keyboard, don't just asume everyone has a keyboard or controller.

## Hosting your app

There are tons of ways to accomplish hosting your application, but you will want to think about the who is going to be using your app or game and what types of devices make sense.

### Deploy to Github Pages

Github offers an extremly easy way to host application demos as well as project documentation.

Check out [Github Pages](https://pages.github.com/) for more information and look at this [blog post which describes how publishing is as easy as 1, 2, 3](https://blog.github.com/2016-12-09-publishing-with-github-pages-now-as-easy-as-1-2-3/)

### Hybrid App with Apache Cordova

Cordova is a Native (IOS or Android) wrapper around your web application.
Latest setup details can be found on the [Cordova Project site](https://cordova.apache.org/docs/en/latest/guide/cli/)

```bash
# Make sure you have nodeJS installed (CodeAnywhere has it installed by default)
# Use nvm to install a newer version of NodeJS
nvm install v9.11.1
nvm alias default v9.11.1

# Install Cordova CLI
# This will make the `cordova` command available on your server
# [CLI Reference](https://cordova.apache.org/docs/en/latest/reference/cordova-cli/)
npm install -g cordova

# Create Cordova app
cordova create demo com.example.cross-platform-demo CrossPlatformDemo

# Navigate to the project directory that cordova create just made
cd demo

# Add platforms to the project
cordova platform add android
cordova platform add ios

# Install cordova project dependencies
cordova requirements

# Build the app
cordova build # Will build for all platforms

# Or you can build a platform individually
cordova build ios
cordova build android

```

## Credits

Original [source code](https://github.com/fariazz/phaser-craterconf2016) and [presentation](https://www.youtube.com/watch?v=7qe2XOkubL0&t)