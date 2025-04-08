# 最省名称的进位制系统（用于0–1000的整数表示）

# The Base System That Requires the Fewest Naming Symbols (0–1000Integers)

This problem originates from the end of Chapter 1 of the book "What is Mathematics?" by Richard Courant and Herbert Robbins.

> **How many different number words are needed to name all integers from 0 to 1000 in various bases (from base 2 to 15)?**  
> 
> In a base-*a* positional system, we need unique words for:
> - Each digit: 0 to *a* − 1  
> - Each power of *a* used in the representation of numbers up to 1000: *a*, *a²*, *a³*, ...

The objective is to determine which base requires the fewest number of unique "number words."

---

## 📌 Examples

- For **base 10**:
  - Digit names: 0–9 → 10 words
  - Powers needed: 10, 100, 1000 → 3 words
  - **Total: 13** words

- For **base 4**:
  - Digit names: 0–3 → 4 words
  - Powers needed: 4, 16, 64, 256 → 4 words
  - **Total: 8** words (the minimum among base 2–15)

---

## 📊 Result Summary

After evaluating all bases from 2 to 15, we find that:

- ✅ **Base 4 requires the fewest total words: 8**
- The number of words increases again for bases larger than 5 due to the growing number of digit names required.

---

## 🧠 How It Works

The Python script calculates the number of distinct words needed for each base from 2 to 15. For each base `a`, the total number of words is computed as:

```
number_of_words = number_of_digits + number_of_power_names
```

Where:
- `number_of_digits = a`
- `number_of_power_names = floor(log_a(1000)) + 1`

---

## 🧪 Run the Code

1. Clone this repo
2. Run the script in your Python environment (Python 3.x)

```bash
python minimal_base_name.py
```

You’ll see the word count per base and the one that minimizes the total.

---

## 📁 Files

- `minimal_base_name.py` — core logic for evaluating number word counts
- `README.md` — this file

---

## 🏷️ Project Name

**English**: _The Base System That Requires the Fewest Naming Symbols (0–1000Integers)_  
**中文**：_最省名称的进位制系统（用于0–1000的整数表示）_

---

## 📚 Source

This project is based on an exercise from the classic mathematics book:

> Courant, R., & Robbins, H. _What is Mathematics?_ (Oxford University Press)

---

## ✨ License

MIT License

---

## 🙌 Author

Created by Benjamin (with help from Lucy ✨)

---

Feel free to ⭐ star or fork this repo if you found it helpful!
