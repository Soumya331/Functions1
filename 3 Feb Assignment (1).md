Ans 1) def() is used to create a function.


```python
##function that returns list of odd numbers in the range of 1 to 25. 
def test1():
    for i in range(1,25,2):
        print (i)
test1()
```

    1
    3
    5
    7
    9
    11
    13
    15
    17
    19
    21
    23


Ans 2) *args and **kwargs are used when we are unsure about the number of arguments to pass in the functions.



```python
## *args
def myFun(*argv):
	for arg in argv:
		print(arg)


myFun('Hello', 'Welcome', 'to', 'PWSkills')

```

    Hello
    Welcome
    to
    PWSkills



```python
## **kwargs
def sentence(**words):
    sentence = ''

    for words in words.values():
        sentence+=words
    return sentence
    
print("Sentence",sentence(a='Hello',b='Everyone'))


```

    Sentence HelloEveryone


Ans 3) Iterator in Python is an object that is used to iterate over iterable objects like lists, tuples, dicts, and sets. 
The method used to initialise the iterator object and the method used for iteration are iter() and next() respectively.


```python
list = [2, 4, 6, 8, 10, 12, 14, 16, 18, 20]
iter1 = iter(list)
print(next(iter1))
print(iter1.__next__())
print(next(iter1))
print(next(iter1))
print(next(iter1))

```

    2
    4
    6
    8
    10


Ans 4)A generator is a function that returns an iterator that produces a sequence of values when iterated over.
Generators are useful when we want to produce a large sequence of values, but we don't want to store all of them in memory at once.

Yield keyword is used to create a generator function. A type of function that is memory efficient and can be used like an iterator object.


Ans5)
```python
def my_generator(n):

    value = 0
    while value < n:        
        yield value
        value += 1
for value in my_generator(3):
    print(value)
```

    0
    1
    2



```python
def get_primes(): 
    primes = []
    for number in range(2, 1000): 
        is_prime = True
        for prime in primes:
            if number % prime == 0: 
                is_prime = False 
                break  
        if is_prime: 
            primes.append(number) 
            yield number 

```


```python
prime_generator = get_primes()
for _ in range(20): 
    print(next(prime_generator)) 

```

    2
    3
    5
    7
    11
    13
    17
    19
    23
    29
    31
    37
    41
    43
    47
    53
    59
    61
    67
    71



```python

```

