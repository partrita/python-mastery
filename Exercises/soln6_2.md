# Exercise 6.2 - Solution

```python
# structure.py

import sys

class Structure:
    _fields = ()

    @staticmethod
    def _init():
        locs = sys._getframe(1).f_locals
        self = locs['self']
        for name, val in locs.items():
            if name == 'self': continue
            setattr(self, name, val)

    def __setattr__(self, name, value):
        if name.startswith('_') or name in self._fields:
            super().__setattr__(name, value)
        else:
            raise AttributeError('No attribute %s' % name)

    def __repr__(self):
        return '%s(%s)' % (type(self).__name__,
                           ', '.join(repr(getattr(self, name)) for name in self._fields))
```




[Back](ex6_2.md)
