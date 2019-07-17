**follow the below steps:**

**1.download the file and unZip: **

[GoogleNews-vectors-negative300.bin.gz](https://drive.google.com/file/d/0B7XkCwpI5KDYNlNUTTlSS21pQmM/edit)

```
import numpy as np

import re
 
from gensim.models import KeyedVectors
import warnings
with open("GoogleNews-vectors-negative300.bin", 'wb') as new_file, open("GoogleNews-vectors-negative300.bin.gz", 'rb') as file:
    decompressor = bz2.BZ2Decompressor()
    for data in iter(lambda : file.read(100 * 1024), b''):
        new_file.write(decompressor.decompress(data))
  ```      
**2.after unZip the file :**
```
from gensim.models import KeyedVectors
cn_model = KeyedVectors.load_word2vec_format('GoogleNews-vectors-negative300.bin', binary=True)

eg:
cn_model['beautiful']
```
