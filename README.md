# ABOUT


HTML Muncher is a Python utility that rewrites CSS, HTML, and JavaScript files in order to save precious bytes and obfuscate your code.

### If your stylesheet starts looking out like this:

```
.file2 #special {
    font-size: 1.5em;
    color: #F737FF;
}

.file2 #special2 {
    letter-spacing: 0;
}

.box {
    border: 2px solid #aaa;
    -webkit-border-radius: 5px;
    background: #eee;
    padding: 5px;
}

it will be rewritten as

.a #a {
    font-size: 1.5em;
    color: #F737FF;
}

.a #b {
    letter-spacing: 0;
}

.b {
    border: 2px solid #aaa;
    -webkit-border-radius: 5px;
    background: #eee;
    padding: 5px;
}
```
## INSTALLATION

Easy install [Htmlmuncher.egg](http://htmlmuncher.com/htmlmuncher.egg)

**OR**

Download the source from [Github](http://github.com/ccampbell/html-muncher "Htmlmuncher")
```
$ cd html-muncher
$ python setup.py install
```

## USAGE

Read [Usage](http://htmlmuncher.com/#usage)

**OR**

```
munch --help
```

## EXAMPLES

- To update a bunch of stylesheets and views

```
munch --css demo/css --html demo/views
```

- To update a single file with inline styles/javascript

```
munch --html demo/single-file/view-with-inline-styles.html
```

- You can also select specific files

```
munch --css file1.css,file2.css --html view1.html,view2.html
```

- Or you can mix and match files and directories

```
munch --css /my/css/directory,global.css --html /view/directory1,/view/directory2,/view/directory3,template.html
```
