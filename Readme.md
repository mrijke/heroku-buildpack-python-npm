Heroku buildpack: Python + NPM
========================

This is a [Heroku buildpack](http://devcenter.heroku.com/articles/buildpacks) for Python apps, powered by [pip](http://www.pip-installer.org/). It will also install the NPM packages that are defined in the `npm_requirements.txt` file in the root of the project.


Usage
-----

This is pretty hacky. At the moment it reinstalls all the defined npm packages on every deploy. It will also only work if your slug builder already has NPM installed. For dokku, add `npm` to the packages.txt of the `buildstep` step.
Probably a better solution would be to use the Heroku multi buildpack. 
