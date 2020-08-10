
# code for multi-granularity reader

- Step 0, mkdir

```
mkdir model_out
mkdir model_save
```


- Step 1, generate seq_tag pairs,

```
python gen_seq_tag_pairs.py --div <div>
```

- Step 2, training and decoding,

```
python main.py --config config/example.config
```

- Step 3, change predicted seq_tag pairs to eval format, generate ```pred.json```.

```
python seq_to_extracts.py --seqfile model_out/multi_bert.out
```


our implementation is built upon [ncrf++](https://arxiv.org/abs/1806.05626)


