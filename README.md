# 🤖 Text Generation with Markov Chains

> A Generative AI model built from scratch in Python that learns statistical patterns from text and generates new human-like content — no external ML libraries required.

---

## 📌 About the Project

This project implements a **Markov Chain-based Text Generation model** — a foundational concept in Generative AI and Natural Language Processing (NLP).

A Markov Chain is a statistical model that predicts the **next word or character** based on the previous one(s). By training on any text corpus, the model learns transition probabilities between words/characters and uses them to generate new, coherent text.

This was built as **Task-03** of the Machine Learning Internship at **Prodigy Infotech**.


## ✨ Features

- ✅ **Word-level Markov Chain** — predicts the next word based on previous word(s)
- ✅ **Character-level Markov Chain** — predicts the next character based on previous character(s)
- ✅ **Configurable order (n-gram size)** — control how many previous tokens influence the next
- ✅ **Custom seed support** — steer text generation from a specific starting state
- ✅ **Interactive mode** — train on your own text and generate custom output
- ✅ **Zero external dependencies** — built with Python standard library only


## 🧠 How It Works

```
Training Phase:
("the", "quick") ──► ["brown", "fox", "red"]
("quick", "brown") ──► ["fox", "bear"]

Generation Phase:
Start state ──► randomly pick next word ──► shift state ──► repeat
```

The model builds a **transition table** during training. At generation time, it starts from a state and randomly samples the next token based on learned probabilities — producing new text that mimics the style of the training data.

---

## 📁 Project Structure

```
markov-chain-text-generator/
│
├── markov_chain_text_generator.py   # Main source code
└── README.md                        # Project documentation
```

---

## ▶️ How to Run

### 1. Clone the repository
```bash
git clone https://github.com/your-username/markov-chain-text-generator.git
cd markov-chain-text-generator
```

### 2. Run the script
```bash
python markov_chain_text_generator.py
```

> No pip installs needed — uses only Python built-in modules (`random`, `re`, `collections`).


## 🖥️ Sample Output

```
============================================================
  Task-03: Text Generation with Markov Chains
============================================================

📖 WORD-LEVEL MARKOV CHAIN (order = 1)
----------------------------------------
[Word model] Trained on 89 tokens, 67 unique states.

Generated (50 words):
The forest is full of the season. Brown bears and small.
Over the lazy dog barked loudly at the hills and dogs
often play in the wild are the warm fireplace all day long.

📖 WORD-LEVEL MARKOV CHAIN (order = 2)
----------------------------------------
Generated (50 words):
The river flows quickly through the green forest every day.
Brown bears and quick foxes share the same forest habitat.
Dogs are loyal animals that live with humans for many years.

🔤 CHARACTER-LEVEL MARKOV CHAIN (order = 3)
----------------------------------------
Generated (200 chars):
the quick brown fox jumps over the lazy dog. a fox is a
clever animal that lives in the wild. the dog barked loudly
at the brown fox near the river flows quickly.
```

---

## ⚙️ Configuration

| Parameter | Default | Description |
|-----------|---------|-------------|
| `order` | `2` | Number of previous tokens used to predict the next |
| `num_words` | `50` | Number of words to generate (word model) |
| `num_chars` | `200` | Number of characters to generate (char model) |
| `seed` | `None` | Starting state to guide generation |

---

## 🔬 Concepts Used

| Concept | Description |
|--------|-------------|
| **Markov Chain** | A stochastic model where the next state depends only on the current state |
| **N-gram** | A sequence of N tokens (words or characters) used as the model state |
| **Transition Probability** | The likelihood of moving from one state to another |
| **Generative AI** | AI that creates new content by learning patterns from existing data |

---

## 🚀 Use Cases

- Text autocomplete systems
- Creative writing assistants
- Chatbot prototypes
- Understanding foundations of language models (GPT, etc.)
- NLP learning and experimentation

---

## 🛠️ Built With

- **Python 3.8+**
- `collections.defaultdict` — for building the transition table
- `random` — for probabilistic text sampling
- `re` — for text tokenisation and formatting

---

## 📚 References

- [Markov Chain — Wikipedia](https://en.wikipedia.org/wiki/Markov_chain)
- [N-gram Language Models](https://en.wikipedia.org/wiki/N-gram)

---

## 👩‍💻 Author

**Vabhravi Pandey**  
Generative AI Intern — Prodigy Infotech  


---

## 📄 License

This project is licensed under the MIT License — feel free to use, modify, and distribute.

---

⭐ **If you found this project helpful, please give it a star!**
