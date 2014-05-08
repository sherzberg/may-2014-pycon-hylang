Hylang Basics
=============

Getting into the hy repl is easy:

```bash
$ hy
hy 0.10.0
=>
```

Lets try some things out:

```hy
=> (print "hello world")
hello world
=> (+ 5 6)
11L
=> (+ 1 2 3)
6L
=> (+ 5 (- 5 2))
8L
```

Setting variables?

```hy
=> (setv x (+ 9 1))
=> (print x)
10
```

Functions?

```hy
=> (defn greet [name]
...   (print "hello " name)

=> (greet "john")
hello john
=> (defn greet [name &optional [prefix "hello"]]
...   (print prefix name)

=> (greet "john" "hola")
hola john
=> (apply greet ["john"]
...   {"prefix" "hello"})
hola john
```

Calling methods?

```hy
=> (.strip " fooooo   ")
"fooooo"
```

Conditionals?

```hy
=> (if true 
...   (print "this is true")
...   (print "this is false"))
this is true
```

Loops?

```hy
=> (for [i (range 3)]
...   (print i))
0
1
2
```

List Comprehensions?

```hy
=> (list-comp
...   x
...   (x (range 5))
...   (= (% x 2) 0))
[0, 2, 4]
```

Exercises
---------

* Define a function (with leap year parameter) that calculates the number of minutes in a year.
* Define a function that takes a list of numbers and filters out odd entries.
