conference.scipy.org
====================

This repository contains the landing page and blog for the
conference.scipy.org.  Each specific SciPy Conference manages it's own
website and this site is only meant to capture the commonalities
between them.

## Contributing

Currently the website is a set of static pages generated by
[Pelican](http://getpelican.org).  The generated content is uploaded
to our server sponsored by [Enthought](http://enthought.com). Contact
[scipy-organizers@scipy.org](mailto://scipy-organizers@scipy.org) to
get things updated.

Please feel free to contribute in what ever capacity you feel best.
For now, the site contains details for conferences past and news items
from conferences. 

Here are a few ways you can contribute:

### Add news item

* [Fork the repository](https://help.github.com/articles/fork-a-repo) on
  [github](https://github.com/scipy-conference/conference.scipy.org)

* [Clone the fork](https://help.github.com/articles/fork-a-repo#step-2-clone-your-fork)

```
$ git clone git@github.com:aterrel/conference.scipy.org.git
Cloning into 'conference.scipy.org'...
remote: Counting objects: 74, done.
remote: Compressing objects: 100% (68/68), done.
remote: Total 74 (delta 3), reused 73 (delta 2)
Receiving objects: 100% (74/74), 248.52 KiB | 0 bytes/s, done.
Resolving deltas: 100% (3/3), done.
Checking connectivity... done
$ cd conference.scipy.org
```

* [Create a new branch](https://help.github.com/articles/fork-a-repo#create-branches) with the name of your news item.

* Add your news item in content/news, see
  [Pelican docs](http://docs.getpelican.com/en/3.3.0/getting_started.html#writing-content-using-pelican)
  for details can be rst or markdown. An exmple below:

```
$ cd content/news
$ cat << EOF > 2013-10-25-test.md
> Title: Test
> Date: 2013-10-25
> Comments: true
> Categories: 
> Author: Andy R. Terrel <andy.terrel@gmail.com>
> Summary: Testing
> 
> Testing how this works!
> 
> EOF
```

* [Push to your fork on github](https://help.github.com/articles/fork-a-repo#push-commits)
 
* [Create a pull request](https://help.github.com/articles/using-pull-requests)

* Email [scipy-organizers@scipy.org](mailto://scipy-organizers@scipy.org) to get the content deployed.

### Add or edit a page

* To edit the website one needs to first install the pelican blog system, see http://docs.getpelican.com/en/3.3.0/getting_started.html  
  * be sure to have [Markdown](http://pythonhosted.org/Markdown/index.html) installed as well

* Next checkout the source code:
```
$ git clone git@github.com:scipy-conference/conference.scipy.org.git
$ cd conference.scipy.org.git
```


* Editting pages:

  * The content of the page can be found in the content directory
```
$ cd content; ls
 images news pages pdf
```
    * images and pdf: static content to be copied,
    * news: the markdown blog like pages,
    * pages: the set of pages to be displayed

  * To add a new post, add a file to the news, see pelican docs for the page issues:

* Generating and viewing changes
  * Now go to the top dir and regenerate site:
```
$ cd ../../
$ make html
```

  * To view it locally:
```
$ make serve
< open browser to http://127.0.0.1:8000 >
( you should see your test page in the News and archives )
< Ctrl-C to exit server on terminal >
```

  * To modify a page edit inside the pages content
```
$ cd content/pages
$ vi 2013_detail.md
```

  * Once again go to top and make it and view
```
$ cd ../.. && make html && make serve
```

  * To edit the layout see thing inside the theme
```
$ ls theme
tuxlite_zfs
```

  * Be sure to check in your changes and push
```
$ git add <files changed>
$ git commit -m “<Describe changes>”
$ git push origin <branch-name>
```

## Contact

The site is collaboratively edited by the SciPy Organizers.  Please
email scipy-organizers@scipy.org for details.
