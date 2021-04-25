> 匿名函数

```python
lambda i : i + 1
# i形参
# i+1 返回值

```

> 闭包

概念：在一个内部函数中，对外部作用域的变量进行引用，并且一般外部函数的返回值为内部函数， 那么内部函数就被认为是闭包

```python

def makefunc():
    list = []
    def func(num):
        list.append(num)
    return func

a = makefunc()
print(a(1))
```

> 装饰器

闭包的一种

```python
import functools

def logs(func):
    @functools.wraps(func)
    def wrapper(*args, **kwargs):
        print('call %s():' % func.__name__)
        func(*args, **kwargs)
        print('args = {}'.format(*args))
        return 
    return wrapper

@logs
def test(p):
    print(test.__name__ + " param: " + p)

test("I am a param")
# 输出
call test():
test param: I am a param
args = I am a param


import functools

def logs(func):
    # @functools.wraps(func)
    def wrapper(*args, **kwargs):
        print('call %s():' % func.__name__)
        func(*args, **kwargs)
        print('args = {}'.format(*args))
        return 
    return wrapper

@logs
def test(p):
    print(test.__name__ + " param: " + p)

test("I am a param")
# 输出
call test():
wrapper param: I am a param
args = I am a param
```



