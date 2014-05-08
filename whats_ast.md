What's AST?
===========

Python AST is the Abstract Syntax Tree, or the internal
representation of python code, in python.

![AST Image](http://www.codeproject.com/KB/codegen/astdlrtest/astdlrtest2.png)

At a high level, this image shows what an AST represents.

[AST Docs](https://docs.python.org/2/library/ast.html)

Lets use the ast:

```bash
$ python
>>> import ast
>>> module = ast.parse("print('hello')")
>>> exec compile(module, 'string', 'exec')
hello
>>> import astor
>>> astor.dump(module)
"Module(body=[Print(dest=None, values=[Str(s='hello')], nl=True)])"
>>> astor.dump(ast.parse("def hi(): print('hi')"))
"Module(\n    body=[\n        FunctionDef(name='hi',\n            args=arguments(args=[], vararg=None, kwarg=None, defaults=[]),\n            body=[Print(dest=None, values=[Str(s='hi')], nl=True)],\n            decorator_list=[])])"
>>> module.body
[<_ast.Print at 0x21224d0>]
>>> astor.codegen.to_source(module.body[0])
"print 'hello'"
```

Typing strings into _ast.parse_ is no fun, so:

```bash
>>> def x(): print 'hi'
>>> inspected = inspect.getsource(x)
>>> module = ast.parse(inspected)
>>> module.body
[<_ast.FunctionDef at 0x244c110>]
```

Cool. Now lets see how hylang works. If you still have your _myfile.hy_ from before:

```bash
$ hy2py --with-ast myfile.hy
```

Nice. What about doing this from the REPL?

```hy
=> (disassemble `(print "Hello"))   
Module(body=[Expr(value=Call(func=Name(id='print'), args=[Str(s=u'Hello')], keywords=[], starargs=None, kwargs=None))])
```

You can also get the python equivalent:

```hy
=> (disassemble `(print "Hello") true)
print('Hello')
```

Exercises:

* Check out what python code is generated for _if_, _even?_, _for_, and any other expressions and macros you want.
* Whats the ast look like for more complex functions?
