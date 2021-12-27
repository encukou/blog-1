# LookupError

`LookupError` is a base class for `IndexError` and `KeyError`:

```python
KeyError.mro()
# [KeyError, LookupError, Exception, BaseException, object]
IndexError.mro()
# [IndexError, LookupError, Exception, BaseException, object]
```

The main purpose of this intermediate exception is to simplify a bit lookup for deeply nested structures when any of these two exceptions may occur:

```python
try:
    username = resp['posts'][-1]['authors'][0]['name']
except LookupError:
    username = None
```
