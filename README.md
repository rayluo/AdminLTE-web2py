# AdminLTE-web2py: A web2py layout using the AdminLTE template


## How to use it

* Create a new web2py app. Let's call it `lte` for this example.
* Open a terminal window and go to the web2py/applications directory. It should look something like this:

````
__init__.pyc    adminltest    welcome
__init__.py    admin        examples    lte
````

* Change to the `static` directory for the new application (in this case named `lte`)

````
$ cd lte/static
````

### Download AdminLTE straight from Github

* Download the [AdminLTE Dashboard & Control Panel Template](http://almsaeedstudio.com/preview). Assuming
you are still in the `web2py/applications/lte/static` directory, get it from Github like this:

If you don't have Curl, get it free from http://curl.haxx.se/download.html

````
# Copy as a zip file from Github.
# -C means resume transfer if interrupted
# -L means follow any redirects
# -O saves file to the current directory
# -k relaxes security. Hey, it's Github.
$ curl -C - -LOk https://github.com/almasaeed2010/AdminLTE/archive/master.zip
````

#### Warning
AdminLTE carries a ton of demo code. It's a 6MB download. 

* Confirm the file has been copied down to your directory:

````
$ ls
403.html	500.html	images		master.zip
404.html	css		js
````

* Now extract the .zip archive. 


````
$ unzip master
````

This will create a directory called AdminLTE-master:

````
$ ls
403.html	500.html	css		js
404.html	AdminLTE-master	images		master.zip
```

* You can delete `master.zip` if you wish.

````
$ rm master.zip
````

* Rename the unzipped directory `adminlte`. 
To keep with convention and save typing, I simplified the directory name in 
the 'layout_adminlte.html' file:

````
$ mv AdminLTE-master adminlte
````

### Look at the demo project and documentation pages

* Try viewing some of the files. Here's how to do it from the command line. Again, 
still assuming you're in the `web2py/applications/lte/static` directory.

````
# The two best demos:
$ sudo open adminlte/index.html
$ sudo open adminlte/index2.html

# Show a minimal page--this is a good starting
# point for your own AdminLTE templates.
$ sudo open adminlte/starter.html

# The documentation is pretty damn good
# for an open source freebie.
$ sudo open adminlte/documentation/index.html
````

Or if you have web2py's default Rocket server installed (replace the directory name lte with the name of your application):

http://127.0.0.1:8000/adminlte/static/adminlte/index.html

http://127.0.0.1:8000/adminlte/static/adminlte/index2.html

http://127.0.0.1:8000/adminlte/static/adminlte/starter.html

http://127.0.0.1:8000/adminlte/documentation/index.html

## Get layout_adminlte.html from Github

Go to the ../views directory, then download the new layout file:

````
$ cd ../views
curl -C - -LOk  https://raw.githubusercontent.com/tomcam/AdminLTE-web2py/master/layout_adminlte.html
````

## Use the new layout in a web2py project

* Fire up web2py and edit the view default/index.html. Find this line (it's usually the first):

````
{{extend 'layout.html'}}
````

* Replace `layout.html' with `layout_adminlte.html` so it now looks like this:

````
{{extend 'layout_adminlte.html'}}
````

OK. Run your app and you'll see a stunningly new look.



