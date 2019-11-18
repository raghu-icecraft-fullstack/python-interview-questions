
```python
class A():
    pass
    
aa = A()  # an object of class A is created

# for both below snytax error, cant assign like this 
aa = [:5]
aa = (:5) 

aa = A()
aa(:5)  # passing slice of 1 to 5 numbers, results in syntax error
aa[:5]  # no function is there to handle slice, hence results in 'A' object is not subscriptable
```

```python
# In another declaration
class C():  # by default parent class is Object
    def __getitem__(self, val):
        print val

cc = C()
cc[3]  # displays 3

cc[:5] # slice(None, 5, None), a slice object  is created
cc[3:5] # slice(3, 5, None), a slice object to class instances from 3 to 5
```

In summary, __getitem__ is helpful in managing slice based input
Reference: https://stackoverflow.com/questions/2936863/python-implementing-slicing-in-getitem
