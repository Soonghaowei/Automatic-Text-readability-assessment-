**follow the below steps:**
```
with open("GoogleNews-vectors-negative300.bin", 'wb') as new_file, open("GoogleNews-vectors-negative300.rar", 'rb') as file:
    decompressor = bz2.BZ2Decompressor()
    for data in iter(lambda : file.read(100 * 1024), b''):
        new_file.write(decompressor.decompress(data))

from gensim.models import KeyedVectors
cn_model = KeyedVectors.load_word2vec_format('GoogleNews-vectors-negative300.bin', binary=True)

eg:
cn_model['beautiful']
```
