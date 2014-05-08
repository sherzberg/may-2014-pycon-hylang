Pyowa May 2014 Talk/Workshop
============================

This repo contains the info needed for the Pyowa users
group May 2014 talk. 

The speaker was Spencer Herzberg:

* [https://github.com/sherzberg](https://github.com/sherzberg)
* [@linuxconvert](https://twitter.com/linuxconvert)


PyCon2014 Recap
---------------

[Slides](https://docs.google.com/presentation/d/1yo1qLVrTidHiKZDcA_GZRwHxZjM8dgftj7lOCO390gM/edit?usp=sharing) to my recap of PyCon 2014


Hylang/AST manipulation workshop
--------------------------------

Hylang setup on python 2.7:

```bash
$ pip install https://github.com/hylang/hy/archive/master.zip
$ hy -c '(import hy) (print hy.__version__)'
0.10.0
$ 
```

If you get _0.10.0_ printed, you have everything installed correctly.
We install _0.10.0_  because it has _hy2py_ which is not released yet.

Goals
-----

* Learn about PyCon2014 and why you should go
* Get an abbreviated overview of Hy
* Learn how to look at and possibly use Python AST
* Learn how Hy uses the Python AST

Workshop overview
------------------------

* [Hylang basics](hylang_basics.md)
* [Hylang advanced](hylang_advanced.md)
* [Running scripts](running_scripts.md)
* [Whats AST?](whats_ast.md)

Thanks
------

This repo and workshop could not have been possible without:

* [Source Allies, Inc](http://www.sourceallies.com/) for sending me to PyCon
* [Pyowa Users Group](http://www.pyowa.org/) for raffling a free registration ticket
* [Paul Tagliamonte](https://twitter.com/paultag) and the [HySociety](https://github.com/hylang/hy/graphs/contributors) for hylang and his awesome talk at PyCon
 * [Video](http://www.pyvideo.org/video/2616/getting-hy-on-python-how-to-implement-a-lisp-fro)

Where to go from here?
----------------------

* [macropy](https://github.com/lihaoyi/macropy)
