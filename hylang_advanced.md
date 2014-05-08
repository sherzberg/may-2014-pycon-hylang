Hylang Advanced
===============

* [Builtins](http://docs.hylang.org/en/latest/language/api.html#builtins)
* [Core](http://docs.hylang.org/en/latest/language/core.html)

Helper Macros:

```hy
=> (empty? [])
True
=> (empty? "")
True
=> (empty? (, 1 2))
False
=> (dec 3)
2
=> (dec 11.4)
10.4
=> (iterable? "abc")
True
=> (iterable? 1)
False
=> (some? even? [1 2 3])
True
=> (some? odd? [2 4 6])
False
```

Classes in hy?

```hy
(defclass Test [object]
  [[--init--
    (fn [self]
      (print "INIT")
      None)]])

(setv test (Test))
```

Hate nested expressions? Threading macro to the rescue:

```hy
=> (print (+ 1 (+ 2 3)))
6
=> (print (-> (+ 2 3) (+ 1)))
6
```

Exercises:

* Define a function to find the smallest item in a list of integers.
* Define a class called Point with (x, y) as attributes. Use it in a loop.
* Define a map function (like python map) that takes a list and a filter lambda.
