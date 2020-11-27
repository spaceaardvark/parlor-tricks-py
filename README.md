# parlor-tricks-py
A list or random Python parlor tricks. See also [parlor-tricks-js](https://github.com/spaceaardvark/parlor-tricks-js/).

### Regex: tokenize repeating characters in a string

```python
import re

test = "1101000000101"
regex = r"(\w)\1*"

tokens = [x[0] for x in re.finditer(regex, test)]

print(tokens)
# => ['11', '0', '1', '000000', '1', '0', '1']
```

Tags: regex, string, sequence, repeating, characters, binary gap, run-length encoding

### Binary: *n* bits will all *1*s

16 bits = `pow(2, 17) - 1`  
n bits = `pow(2, n + 1) - 1`

This is a shortcut derived from the [sum of the first n terms of a geometric series](https://en.wikipedia.org/wiki/Geometric_series#Formula).

Tags: binary, shift, bits, geometric series
