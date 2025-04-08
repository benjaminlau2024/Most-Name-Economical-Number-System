# 最省名称的进位制系统（用于0–1000的整数表示）

The Base System That Requires the Fewest Naming Symbols (0–1000Integers)
> **How many different number words are needed to name all integers from 0 to 1000 in various bases (from base 2 to 15)?**
>
>This problem originates from the end of Chapter 1 of the book "What is Mathematics?" by Richard Courant and Herbert Robbins.
>Consider the representation of integers in a positional numeral system with base a. In order to name the numbers in this system, we need distinct words for the digits 0, 1, ..., a − 1, as well as for the powers of a: a, a², a³, and so on.
>How many different number words are needed to name all integers from 0 to 1000, for a = 2, 3, 4, ..., 15?
>Which base requires the fewest total number words?
> 
>**Examples:**
> 
>If a = 10, we need 10 words for the digits (0–9), plus words for 10, 100, and 1000, totaling 13.
>If a = 20, we need 20 digit names (0–19), plus names for 20 and 400, totaling 22.
>If a = 100, we need 100 digit names and one unit (100), totaling 101.

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
