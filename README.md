# Nepalese Names Dataset

A minimal, cleaned dataset of common Nepalese **first names** and **surnames** in CSV format. This repository is intended for development, testing, and research use cases where realistic Nepali name data is useful.

---

## Contents

- `unique_first_names.csv`  
  A deduplicated list of first names.

- `unique_surnames.csv`  
  A deduplicated list of surnames.


---

## Data Format

Each CSV is simple and consistent.

### unique_first_names.csv
```
First Name
AASHISH
AADESH
...
```

### unique_surnames.csv
```
Surname
KHANAL
KHATRI
DAHAL
...
```

---

## Data Cleaning Rules

The dataset is normalized from raw sources using the following rules:

- Converted to uppercase for consistency
- Removed honorifics and titles such as:
  - DR, MR, MRS, MS, KU, etc.
- Trimmed whitespace and punctuation
- Extracted:
  - **First Name** → first token
  - **Surname** → last token
- Removed duplicates using set-based deduplication
---

## Use Cases

- Form validation and testing
- Mock data generation
- NLP / name parsing experiments
- UI prototyping with realistic data
---

## How to Use

1. Clone the repository:

```bash
git clone https://github.com/dhirajraut1/nepalese-names-surnames.git

cd nepalese-names-surnames
```


Load in Python:

```python
import pandas as pd

first_names = pd.read_csv("unique_first_names.csv")
surnames = pd.read_csv("unique_surnames.csv")

print(first_names.head())
print(surnames.head())
```

---

## Contributing

Contributions are welcome. You can:

* Add more names/surnames
* Improve cleaning logic
* Fix inconsistencies
* Add regional variations

Please ensure:

* No duplicates
* No titles/honorifics
* Proper formatting

---

## Disclaimer

> This dataset is a simplified representation of Nepalese names and may not cover all ethnic, linguistic, or regional variations. It is not intended for official or identity-related use.

---

## License

MIT License

---

## Future Improvements

* Frequency/popularity ranking
* Region/ethnicity tagging
* API access for names generation
