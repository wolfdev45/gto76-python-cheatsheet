Python and Libraries Cheatsheet
===============================

Main
----
```
if __name__ == '__main__':
    main()
```

Range
-----
```
range(<to exclusive>)
range(<from inclusive>, <to exclusive>)
range(<from inclusive>, <to exclusive>, <step size>)  # Negative step for backward
```

List
----
```
<list>[<inclusive from>:<exclusive to>:<step size>]
<list>.extend(<list>)
<list>.sort()
<list>.reverse()
sum(<list>)
```

Dictionary
----------
<dict>.items()
<dict>.get(<key>, <default>)
<dict>.setdefault(<key>, <default>)
```

Set
---
```
<set> = set()
<set>.add(<el>)
<set>.update(<set>)
<set>.union(<set>)
<set>.intersection(<set>)
<set>.difference(<set>)
```

Enumerate
---------
```
for i, <el> in enumerate(<list>)
```



Type
----
```
type(<el>) is int/str/set/list
```
```
import numbers
isinstance(<el>, numbers.Number)
```



String
------
```
str.replace(<text>, <old>, <new>)
<str>.isnumeric()
```

### Print
```
print(<el1>, <el2>, end='', sep='', file=<file>)
```

### Regex
```
import re
re.sub(<regex>, <new>, <text>)
re.search(<regex>, <text>)
```

### Format
```
'{}'.format(<el>)
```

```
{:<min width>}  -> '<el>    '
{:><min width>} -> '    <el>'
{:^<min width>} -> '  <el>  '
{:_<min width>}  -> '<el>____'
{:.<max width>} -> '<e>'
{:<max widht>.<min width>} -> '    <e>'
{:<max width>.<no of decimals>f} -> '  3.14'
```

### Text Wrap
```
import textwrap
textwrap.wrap(<text>, <width>)
```


Random
------
```
import random
random.random()
random.randint(<from inclusive>, <to inclusive>)
random.shuffle(<list>)
```

Infinity
--------
```
float("inf")
```

Datetime
--------
```
import datetime
now = datetime.datetime.now()
now.strftime('%Y%m%d')
now.strftime('%Y%m%d%H%M%S')
```





Inline
------
### For
```
[i+1 for i in range(10)]
[i+1 for i in range(10) if i > 5]
[i+j for i in range(10) for j in range(10)]
```

### Lambda
```
lambda <arg1>, <arg2>: <return value>
lambda: <return value>
```

Class
-----
### Class
```
class <name>:
    def __init__(self, <arg>):
        self.a = <arg>
    def __repr__(self):
        return str({'a': self.a})
    def __str__(self):
        return str(self.a)
```

### Enum
----
```
import enum
class <name>(enum.Enum):
    <value> = <index>
```

### Copy
```
import copy
copy.copy(<object>)
copy.deepcopy(<object>)
```


System
------

### Arguments
```
import sys
sys.argv
```

### Read File
```
with open(<filename>, encoding='utf-8') as file:
    return file.readlines()
```

### Write to File
```
with open(<filename>, 'w', enconding='utf-8') as file:
    file.write(<text>)
```

### Execute Command
```
import os
os.popen(<command>).read()
```


JSON
----
```
import json
```

### Read File
```
with open(<filename>, encoding='utf-8') as file:
    return json.load(file)
```

### Write to File
```
with open(<filename>, 'w', enconding='utf-8') as file:
    file.write(json.dumps(<object>))
```



SQLite
------
```
import sqlite3
db = sqlite3.connect(<filename>)
```

### Read
```
cursor = db.execute(<query>)
if cursor:
    cursor.<fetchone/fetchall>()
db.close()
```

### Write
```
db.execute(<query>)
db.commit()
```


Threading
---------
```
import threading
```

### Thread
```
thread = threading.Thread(target=<function>, args=(<first arg>, ))
thread.start()
thread.join()
```

### Lock
```
lock = threading.Rlock()
lock.acquire()
lock.release()
```





























