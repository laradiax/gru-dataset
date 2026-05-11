# Gru Dataset: Violence Classification in Educational Texts

Welcome to the repository for the **Gru Dataset**, a gold-standard Portuguese corpus tailored for detecting and grading violence in long-form educational texts and children's literature.

This dataset is maintained by the **omitted**.

## 📌 Overview

Unlike traditional social media toxicity datasets, the *Gru* dataset focuses on the narrative complexity and figurative language found in educational assessment materials. It was meticulously annotated by three educational assessment experts based on the Brazilian Indicative Rating System guidelines.

* **Language:** Portuguese (PT-BR) with English translations for sentences.
* **Size:** 300 macro-texts segmented into 8,607 sentences.
* **Task:** Binary violence detection and Multiclass severity grading (Scale 0-3).
* **Domain:** Educational materials, news articles, short stories, and fables.

## 🗂️ Dataset Structure

The dataset is provided in CSV format and contains both granular (sentence-level) evaluations and global document metadata.

*(Note: In the public release, the `sentence_pt` and `sentence_en` column may be redacted to comply with copyright restrictions and double-blind review policies).*

The `data/gru_dataset.csv` file contains the following columns:

* `id`: Unique identifier for the instance.
* `links_news`: URL of the original source text.
* `expert1`, `expert2`, `expert3`: Individual binary or severity evaluations provided by the three assessment experts.
* `final`: The consensus evaluation reached by the experts.
* `global_level`: The maximum violence severity score assigned to the overall source document (Scale 0-3).
* `level_`: The specific severity score for the sentence (Scale 0-3).
* `sentence_pt`: The extracted text fragment/sentence in Portuguese.
* `sentence_en`: The English translation of the text fragment.
* `comment`: Qualitative remarks and justifications from the experts regarding the text's pedagogical suitability.
* `adequacy`: A flag indicating if the text is suitable for Large-Scale Educational Assessments (e.g., `yes`, `no`, `partially`).


## 📊 Violence Intensity Scale (Taxonomy)

The consensus score (`level`) is based on a formal 4-point scale:

* **0 (None):** Text without mention of violent acts, threats, or offensive language.
* **1 (Mild):** Hostile language, mild insults, aggressive irony, or implicit tension without physical contact.
* **2 (Moderate):** Description of physical altercations (e.g., punches, pushing) without graphic details or lethal threats.
* **3 (Extreme):** Graphic descriptions of severe injury, torture, explicit homicide, or intense psychological abuse.

## 🚀 Usage

You can easily load the dataset using Pandas in Python:

```python
import pandas as pd

# Load the dataset
df = pd.read_csv("data/gru_dataset.csv")

# Filter only violent sentences (Levels 2 and 3)
violent_sentences = df[df['nivel'] >= 2]
print(violent_sentences[['text', 'nivel']])

# Group by document to see global metrics
document_stats = df.groupby('news_id')['nivel_global'].first()
print(document_stats.value_counts())
```

## 📜 License & Copyright Disclaimer

The expert annotations, metadata, and structuring of the *Gru* dataset are released under the **Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International (CC BY-NC-SA 4.0)** license. It is intended strictly for academic and non-commercial research purposes.

**Copyright Disclaimer & Authorizations:**
Regarding the textual content, the distribution of sentence-level fragments complies with the **Brazilian Copyright Law (Lei 9.610/98, Art. 46, III)**, which permits the citation of brief excerpts for study and research purposes. Furthermore, **express authorization was obtained from specific rights holders** for the evaluation and inclusion of certain materials within this corpus.

To strictly adhere to intellectual property regulations, **full proprietary macro-texts are withheld from this public repository**. Only the necessary brief excerpts (sentences) evaluated in the study are provided, ensuring the protection of the original works while supporting scientific reproducibility.
