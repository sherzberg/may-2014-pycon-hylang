Running Scripts
===============

Create a file called _myfile.hy_ with a _main_ function and run:

```bash
$ hy myfile.hy
```

Run it from python?

```bash
$ hyc myfile.hy
$ ls -la | grep myfile
...
$ python myfile.pyc
```

Cool huh!?

How about viewing what python code would be generated?

```bash
$ hy2py myfile.hy
```

Woah?!

One last trick. Create a file called _python.py_ with contents:

```python
import hy.importer

from myfile import main

main()
```

MAGIC...

Exercises:

* View some more of your code snippets with _hy2py_.
