First clone repo

Then cd into repo folder


Install 
```bash
~/word2vec$ gcc non_negative_word2vec.c -o nn_word2vec -lm -pthread -O3 -march=native -funroll-loops
```

Test
```bash
~/word2vec$ ./nn_word2vec -train ../OIWE/alldata-id.txt -output vectors.txt -cbow 0 -size 100 -window 3 -negative 2 -hs 0 -sample 1e-3 -threads 2 -binary 0 -iter 5 -min-count 1 -sentence-vectors 1
Starting training using file ../OIWE/alldata-id.txt
Vocab size: 356395
Words in train file: 26499251
spinkney@CSVASPINKNEY02:~/word2vec$ grep '_\*' vectors.txt > sentence_vectors.txt
```
