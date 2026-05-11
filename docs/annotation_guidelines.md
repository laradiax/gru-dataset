# Annotation Guidelines

This document outlines the protocol used to annotate the **Gru Dataset**. To ensure a high-quality gold standard, the curation process was conducted by three independent experts with experience in large-scale educational assessments in Portuguese.

## 1. Annotation Protocol

Each expert evaluated the candidate texts along two primary dimensions:

1. **Sentence-Level Severity Grading:** Each sentence within the text was evaluated strictly on a four-point violence intensity scale (ranging from 0 to 3).
2. **Pedagogical Adequacy:** Experts provided a qualitative judgment on whether the text as a whole was pedagogically suitable for children and adolescents in high-stakes educational assessments.

## 2. The Consensus Process (Triangulation)

To mitigate individual bias and subjectivity—especially when dealing with implicit violence or figurative language—the following consensus protocol was applied:

* **Independent Review:** The three experts initially scored the sentences independently (`expert1`, `expert2`, `expert3`).
* **Triangulation & Discussion:** In cases of disagreement (e.g., scores of 1, 1, and 2), qualitative discussion rounds were held among the experts.
* **Final Score:** The experts debated the linguistic nuances and the official guidelines until a unanimous consensus (`final`) was reached for every sentence.

## 3. Global Document Level

After annotating all sentences, a `global_level` score was automatically assigned to the source document. This global score corresponds to the maximum violence intensity level found in any of its constituent sentences.

* *Note: In an educational curation pipeline, identifying even a single excerpt containing explicit violence (Levels 2 or 3) is sufficient to exclude the macro-text from use.*

## 4. Normative Basis

The qualitative discussions were grounded in the formal definitions of the **Brazilian Indicative Rating Practical Guide** (Classificação Indicativa), adapting its audiovisual and media descriptors into a computational taxonomy for textual data.
