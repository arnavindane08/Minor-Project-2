# GroupDNA — Your WhatsApp Group Chat, Decoded

> **"Spotify Wrapped, but for your friend group."**  
> Industry-Graded Minor Project — **IBM × Unlox Academy**

GroupDNA is a behavioural chat analytics and personality profiling tool that parses raw WhatsApp `.txt` exports from scratch and generates a structured, terminal-style analytics report using **only Python fundamentals and NumPy**.

---

## 📸 Sample Output

> *(Replace the image link below with a screenshot of your printed report from Google Colab or Jupyter Notebook)*

![GroupDNA Final Report](assets/groupdna_output.png)

---

## ✨ Key Features

1. **Edge-Case Resilient Chat Parser:** Parses raw WhatsApp Android exports line-by-line without regular expressions, cleanly handling system notifications, `<Media omitted>` stubs, deleted messages, multi-line messages, and blank lines.
2. **Group Overview & Activity Breakdown:** Summarizes chat duration, total active days, participant count, and ranked per-person message volumes and percentages.
3. **Peak Activity Detection:** Identifies the single busiest calendar date and highest-traffic hour of the day across the entire chat history.
4. **NumPy 6×24 Activity Heatmap:** Constructs a 2D NumPy matrix (`participants × 24 hours`) and renders a four-level shaded terminal heatmap (`·`, `░`, `▒`, `█`) normalized per user.
5. **Vocabulary & Top Words Analysis:** Tokenizes messages, strips punctuation, filters stop words, and plots proportional horizontal block bars for the group's most-used slang and keywords.
6. **Response Speed & Silent Streaks:** Uses `datetime` deltas to calculate average reply times per participant and tracks each member's longest streak of consecutive silent days.
7. **Personality Archetype Engine:** Scores every participant across 8 quantitative behavioural archetypes (*The Spammer*, *The Group Mom*, *The Night Owl*, *The Storyteller*, *The Drama Queen*, *The Ghost*, *The Comedian*, *The Question Master*) plus a custom 9th archetype (*[Your Custom Archetype Name]*), enforcing exclusive assignment.
8. **Formatted Terminal Report:** Outputs a clean, aligned, box-drawn report designed for readability.

---

## 🛡️ Engineering Constraints (Built From Scratch)

To demonstrate mastery of core data structures and algorithmic thinking without high-level abstractions, this project strictly adheres to the following constraint rules:

| Allowed Tools & Concepts | Forbidden Libraries & Shortcuts |
| :--- | :--- |
| Core Python (`str`, `list`, `dict`, `set`, `tuple`, loops, comprehensions, `sorted()`) | `pandas` (no DataFrames or `read_csv`) |
| File I/O (`open()`, `.read()`, `.readlines()`) | `re` (no regular expressions; all parsing uses string methods) |
| `NumPy` (`np.zeros`, indexing, slicing, aggregations) | `collections.Counter` & `collections.defaultdict` |
| `datetime` (`datetime.strptime` & `timedelta` only) | `matplotlib`, `seaborn`, `plotly` (text-based rendering only) |
| Custom `dict`-based counters & string manipulation | Pre-built WhatsApp parsers, `nltk`, or `scikit-learn` |

---

## 📂 Repository Structure

```text
├── GroupDNA_[YourFirstName]_[RollNumber].ipynb   # Main Jupyter / Google Colab notebook
├── hostel_bois.txt                               # Synthetic 60-day benchmark dataset (3,174 messages)
└── README.md                                     # Project documentation
