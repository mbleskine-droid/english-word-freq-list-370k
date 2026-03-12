### `README.md`

# Scored English Words (370k+)

A comprehensive, exhaustive list of over 370,000 English words paired with their frequency/scores. 

This repository provides a valuable dataset for developers, researchers, or NLP enthusiasts building search engines, auto-completion tools, word games, or language models.

## 📦 Data Format

The dataset is provided in a simple, easy-to-parse text file: `scored_words.txt`. 
Each line contains a word and its corresponding score, separated by a space (or tab).

**Example:**
```text
a 9982106.974746
aa 363947.066228
aaa 40560.142508
...
aardvark 5184.658714

```

## 🚀 Usage

You can easily load this data into your favorite programming language. Here is a quick example in **Python**:

```python
word_scores = {}
with open('scored_words.txt', 'r', encoding='utf-8') as file:
    for line in file:
        parts = line.strip().split()
        if len(parts) == 2:
            word, score = parts[0], float(parts[1])
            word_scores[word] = score

print(f"Loaded {len(word_scores)} words.")
print(f"Score for 'aardvark': {word_scores.get('aardvark')}")

```

## 🙌 Credits & Acknowledgements

The base list of English words used in this repository originates from the fantastic [dwyl/english-words](https://github.com/dwyl/english-words) repository.

Specifically, the words are based on their [`words_alpha.txt`](https://raw.githubusercontent.com/dwyl/english-words/refs/heads/master/words_alpha.txt) file.
A huge thank you to the contributors of that project for maintaining such a clean and exhaustive list.

*If you only need the raw English words without scores, please check out their repository!*

## 📄 License

The original word list provided by `dwyl/english-words` is released under the **Unlicense** (Public Domain).

In the same spirit, the dataset and code in this repository are provided "as is", and you are free to use, modify, and distribute them in your own projects. (If you wish, you can consider this repo under the MIT License or Unlicense).
