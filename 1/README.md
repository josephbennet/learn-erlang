# 1.1 use erlang shell

```bash
erl
```

## 1.1.1 inputs erlang command

The Erlang shell incorporates a line editor build on a subset of Emacs'features

## 1.1.2 exit erlang shell

```bash
1> q().
````
Or press control+g inputs h

# 1.2 erlang basic

## 1.2.1 numeric type

```bash
1> 2+15.
17
2> 49*100.
4900
3> 1892-1472.
420
4> 5/2.
2.5
```

**Erlang does not care whether the input is a floating point number or an integer**
If you want the result to be an integer, you must use div or rem

```bash
5> 5 div 2.
2
6> 5 rem 2.
1
```

## 1.2.2 Invariant variables

```bash
1> One.
* 1:1: variable 'One' is unbound
2> One = 1.
1
3> Un = Uno = One = 1.
1
4> Two = One + One.
2
5> Two = 2.
2
6> Two = Two + 1.
** exception error: no match of right hand side value 3
```

Compare the left and right values to see if they are equal, pattern matching

```bash
7> 47 = 45 + 2.
47
8> 47 = 45 + 3.
** exception error: no match of right hand side value 48
```
If the variable on the left does not have a bound value, the assignment will be implemented
The first letter of the variable must be capitalized or use '_'

## 1.2.3 atom

The atom represents itself

```bash
1> atom
atom
2> atom = 'atom'.
atom
```

## 1.2.4 bool

```bash
1> true and false.
false
2> false or true.
true
3> true xor false.
true
5> not (true and true).
false
```
Note: the boolean operators and and or will always evaluate arguments on both sides of the operator. If you want to have the short-circuit operators (which will only evaluate the right-side argument if it needs to), use andalso and orelse.

```bash
6> 5 =:= 5.
true
7> 1 =:= 0.
false
8> 1 =/= 0.
true
9> 5 =:= 5.0. 
false
10> 5 == 5.0.
true
11> 5 /= 5.0.
false
```
## tuples
