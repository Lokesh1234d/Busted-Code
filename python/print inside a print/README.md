# print inside a print
In this test, we will be putting a print function inside a print function.

### Test 1
*(File: src/01.py)*

First, lets put a print inside a print. Simple enough.

Input:
```python
print(print('Hello World!'))
```

Output:
```
Hello World!
None
```

#### Explanation:
The reason this is happening is because it is running 'Hello World!' through print and getting the text, then it is running the base print(), but not returning anything because another print() is inside.

### Test 2
*(File: src/02.py)*

We *have* to test the limits of this occurrence. Lets do it 24 times.

Input:
```python
print(print(print(print(print(print(print(print(print(print(print(print(print(print(print(print(print(print(print(print(print(print(print(print('Hello World!'))))))))))))))))))))))))
```

Output:
```
Hello World!
None
None
None
None
None
None
None
None
None
None
None
None
None
None
None
None
None
None
None
None
None
None
None
```

#### Explanation:
This code is very beautiful. The explanation is the same as above, but longer.

### Test 3
*(File: src/03.py)*

Lets try this once more, but inside itself 1,536 times!

Input:
Honestly, I almost broke Atom just trying to load this, there is not way it is going in here. The good thing is, you can get to all of the code I use in the src folder here.

Output:
```
SyntaxError: too many nested parentheses
```

#### Explanation:
Well, too many parentheses.

## Outcome
Putting a print function inside a print function will return the top input, then `None` for every time it is nested. There is a limit, however, due to a SyntaxError: `too many nested parentheses`

### Credit
This test was written and completed by Zer0 2022.
