# Semantic Search Engine (BERT, PyTorch)

This project implements a semantic search engine using PyTorch.
It focuses purely on **retrieval** (no generation, no RAG), with a clean separation
between offline indexing and online search.

The system uses a **frozen BERT encoder** to embed documents and queries, and ranks
results using **cosine similarity** over mean-pooled embeddings.

---

##  Features

- Frozen `bert-base-uncased` sentence encoder
- Mean pooling with attention mask
- Cosine similarity–based ranking
- Offline indexing, online search separation
- Paragraph-level Wikipedia corpus
- Topic-focused corpus generation (e.g. programming)
- Clean, modular Python project (no notebooks)
- No HuggingFace Trainer

---

## Instructions to run
[Run everything from root folder]

1] Build the corpus
command: python scripts/build_wiki_corpus.py --max-paragraphs 2000
result: This should create a file named corpus.txt in data folder
2]Build the embedding index
command: python indexing/build_index.py
result: this will create 3 file in index folder: docs.txt (has all paras after preprocessing), raw_docs.txt (has original paras), embeddings.pt (contains embeddings of all paras)
3] Run searcher
command: python search/searcher.py

**Edit config.py to control configurations(MODEL_NAME, BATCH_SIZE, MAX_LENGTH, TOP_K)

Author
Srujith Diddi

