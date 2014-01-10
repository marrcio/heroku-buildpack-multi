# heroku-buildpack-multi

Use multiple buildpacks on your app, with support to custom files for each project using overlay.
A fusion of https://github.com/projetoeureka/heroku-overlay and https://github.com/projetoeureka/heroku-overlay

## Usage

    $ heroku config:add BUILDPACK_URL=https://github.com/ddollar/heroku-buildpack-multi-overlay.git --app YOURAPP
    $ heroku config:add OVERLAY="app-extension"

    $ ls *.app-extension
    Procfile.app-extension  requirements.txt.app-extension  .buildpack.app-extension

    $ cat .buildpacks.app-extension
    https://github.com/heroku/heroku-buildpack-nodejs.git#0198c71daa8
    https://github.com/heroku/heroku-buildpack-ruby.git
