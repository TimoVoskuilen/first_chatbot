# First chatbot
This project is a small experimental chatbot built to understand how chatbots and language models work under the hood. The goal is not to build a production-ready system, but to learn how text is tokenized, represented as numbers, and processed step by step in code. Everything is kept as simple and explicit as possible so each part of the system can be understood, modified, and extended. (p.s. It might include a lot of comments, as they are my mental notes. :P)

## Tokenizer
In this project I used a character-level tokenizer. <br>
It converts text into integer tokens and back again using two lookup tables <br>

The tokenizer works by:
1. Assiging a unique integer ID to each character in the dataset used for training the model
2. Encode strings into lists of integers
3. decoding lists of integers back in to string
```python3,
encode = lambda s: [stoi[c] for c in s]
decode = lambda l: ''.join([itos[i] for i in l])
```

