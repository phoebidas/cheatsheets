# Python cheat sheet

### To mark python code in markdown script use ```

```python

# import pandas

```



## Pad a number with zeros on the left

From [StackOverflow](http://stackoverflow.com/questions/339007/nicest-way-to-pad-zeroes-to-string)

Strings:

```python
>>> n = '4'
>>> print n.zfill(3)
>>> '004'
```

And for numbers:

```python
>>> n = 4
>>> print '%03d' % n
>>> 004
>>> print format(4, '03') # python >= 2.6
>>> 004
>>> print '{0:03d}'.format(4)  # python >= 2.6
>>> 004
>>> print('{0:03d}'.format(4))  # python 3
>>> 004
```


## Turn off warnings

Turn them off for a specific function

```python
import warnings

def fxn():
    warnings.warn("deprecated", DeprecationWarning)

with warnings.catch_warnings():
    warnings.simplefilter("ignore")
    fxn()
   
```

Turn off everything (not condoned):

```python
import warnings
warnings.filterwarnings("ignore")

