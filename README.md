# Simon

Just started developing this to allow auto updates for a node-webkit app.
Currently only supported for OSX.

Disclaimer: It's a mess as of now. It's just an experiment and is far from
being finished.

### What Does It Do?
Once cloned into the root of your new node-webkit app, you can run the
`build` shell script and let Simon take what you have done and cache it
on your local machine.

Once your app is cached, Simon can then dynamicly load in your app and
restart itself. This way once auto-updates have been implemented, it
will be able to pull down your latest version of the app and load it
in straight away without having to download an instance of node-webkit
or any other dependencies.

Do not try to use this yet as it's not finished.
