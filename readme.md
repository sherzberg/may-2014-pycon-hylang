Pyowa May 2014 Talk/Workshop
============================

This repo contains the info needed for the Pyowa users
group May 2014 talk. 

The speaker was Spencer Herzberg:

* [https://github.com/sherzberg](https://github.com/sherzberg)
* [https://twitter.com/linuxconvert](@linuxconvert)


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

Workshop overview
------------------------

* [Hylang basics](hylang_basics.md)
* [Hylang advanced](hylang_advanced.md)
* [Running scripts](running_scripts.md)
* [Whats AST?](whats_ast.md)
