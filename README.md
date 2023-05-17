# EagerLinq

EagerLinq is a fall-in-place replacement for `System.Linq.Enumerable` class to debug lazy evaluation issues. Instead of adding multiple .ToList() calls to force eager evaluation, you can replace the namespace reference to `System.Linq` with `EagerLinq` and find out if the issue is regarding lazy evaluation or not. 

EagerLinq is obviously not meant for production, since it's significantly slower than using Linq directly.

In order to use it, add EagerLinq as a dependency, remove the reference to 

```
using System.Linq;
```

and add a reference to:

```
using EagerLinq;
```

Because the `EagerLinq.Enumerable` class mimics the methods of `System.Linq.Enumerable` class, no modifications to existing code needed.

Contributions are welcome.
