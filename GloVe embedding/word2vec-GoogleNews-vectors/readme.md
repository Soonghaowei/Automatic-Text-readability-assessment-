follow the below steps:
from gensim.models import KeyedVectors
cn_model = KeyedVectors.load_word2vec_format('GoogleNews-vectors-negative300.bin', binary=True)


eg:
cn_model['beautiful']
