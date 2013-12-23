# Simon

Simon is a tool that allows you to quick get up and running with
a [node-webkit](https://github.com/rogerwang/node-webkit) application.
Currently only supported for OSX (not yet tested on Linux, could work).

It works in such a way that it is actually a container for your
node-webkit application. The idea is that you create your app locally
like so:

	- MyApp
	  - MyApp.app/
	  - app/
	    - index.html
	    - assets/
	    - pages
	  - package.json


All of your source code goes into `app/`. You may modify the structure
of this how you like. Simon automaticly generates the `assets` and `pages`
directories for you but you don't need to use them if you don't want to.

Simon sits in the root of your project along side `app/` and `package.json`.
As of now it is only a good idea to use this for new projects. Code will be
added at a later stage to support existing node-webkit projects although it
doesn't take long for you to manually adapt the directory structure to support
this.

## Getting up and Running

Here is an example of how you can get started with Simon:

	$ mkdir MyApp
	$ cd MyApp
	$ git clone https://github.com/hazbo/simon.git
	$ cd simon
	$ ./install MyApp

This will generate all the relevant files you will need to be up and running.
If you `cd` out of the `simon` directory you will see that it has generated
the `app` directory and a sample `index.html` file inside there for you.

It also generates a `build` script inside the `simon` directory which packages
your app up and runs in within an instance of node-webkit. You can do this like
so:

	$ cd simon # if you're not already in there
	$ ./build

You will see your app (or the sample app) build and run in node-webkit.

## Why?

So why would you use this as appose to just manually running your own instance
of node-webkit?

What Simon does is actually caches your application on your local machine.
Currently what is being worked on is auto-updates. These the the kind of
updates you will be able to distribute to everyone using the app without any
one having to re-download the whole application.

Currently auto-updates are not finished yet and Simon should be used for
testing / development purposes as if you release an app build using Simon
out into the wild it will not work.

## Todo

  - Create a spec for how Simon will check for the latest version of the app
  - Test being able to pull down remote applications and install them locally

## Contributing

  - Fork Simon
  - Create a feature branch (`git checkout -b my-feature`)
  - Commit your changes (`git commit -am 'Add some feature'`)
  - Push to your feature branch (`git push origin my-feature`)
  - Create new Pull Request
