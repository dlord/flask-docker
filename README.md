# Flask - a Python Microframework


## About this image

This image contains my personal stack for building Flask applications.
This image comes with the following:

1. Flask
2. Flask-Assets
3. Coffeescript compiler
4. SCSS compiler
5. Bower


## How to use this image

Create a `Dockerfile`, `requirements.txt`, and `bower.json` at the root
of your project. Have your `Dockerfile` extend this image, and it will
copy all the files in your current directory.

This Docker image contains `ONBUILD` triggers that will copy
`requirements.txt` and `bower.json` to `/usr/src/app`. Once copied, it
will run `pip install -r requirements.txt` and `bower install`.

The working directory for the image is set to `/usr/src/app`
