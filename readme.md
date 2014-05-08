Pyowa May 2014 Talk/Workshop
============================

This repo contains the info needed for the Pyowa users
group May 2014 talk. 

The speaker was Spencer Herzberg:

* [https://github.com/sherzberg](https://github.com/sherzberg)
* [https://twitter.com/linuxconvert](@linuxconvert)


PyCon2014 Recap
---------------

_link_

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
* [Running scripts](running_scripts.md)
* Examining hylang to python AST
* Moar AST please
