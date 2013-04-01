# cmus-remote web app

This is a web app to control a server instance of [`cmus`](http://cmus.sf.net),
a powerful music player, remotely. So far it only supports basic player and
volume controls, not adding items to the playlist. 

![Screenshot of cmus_app running in Firefox](cmus-app-screenshot.png)

## Dependencies

- Python (tested with 2.7)
- [`bottle`](http://bottlepy.org)
- [`sh`](http://amoffat.github.com/sh/)

The web app also makes use of [Zepto](http://zeptojs.com/),
[Kube](http://imperavi.com/kube), and [Font
Awesome](http://fortawesome.github.com/Font-Awesome/). These are all included.
Thanks to the creators for making them available under permissive licenses. 

## Instructions

- Install `bottle` and `sh` on the host that will be running the web app. (The
  web app can run on the same host as `cmus` or a different one, but both will
  have to have `cmus` installed.)

        $ pip install bottle sh

- Edit the configuration file.
- Run an instance of `cmus` using the `--listen` option.

        $ cmus --listen <host>

- Set a password in `cmus` using `:set passwd=<passwd>`.
- Run the app:

        $ cd cmus_app
        $ python app.py [config-file]

- Open your browser and navigate to `http://<host>:<port>`.

Enjoy!
