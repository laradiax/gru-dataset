# Violence Intensity Scale (Taxonomy)

The **Gru Dataset** utilizes a 4-point severity scale to classify violence. This taxonomy was derived from the official descriptors of the **Brazilian Indicative Rating System** (Sistema de Classificação Indicativa) and adapted for the textual domain. 

Violence is defined formally as the intentional use of force or power resulting in injury, psychological harm, or deprivation.

## Severity Levels

### Level 0: None (Safe)

* **Description:** Text without any mention of violent acts, threats, or offensive language. 
* **Context:** Completely safe for educational environments. Neutral, informative, or positive narratives.

### Level 1: Mild (Verbal / Implicit)

* **Description:** Hostile language, mild insults, aggressive irony, or descriptions of tension without physical contact.
* **Context:** Encompasses mild narrative tension and implicit conflict (e.g., the presence of an antagonist in a classic fable or a non-physical argument). This level is often considered an essential literary element for cognitive development and reading comprehension.

### Level 2: Moderate (Described Physical Action or Clear Threat)

* **Description:** Description of physical altercations (e.g., punches, pushing, hitting) without graphic details, or explicit threats of physical harm.
* **Context:** Actions that depict physical aggression or bullying but lack explicit visceral details. In educational settings, texts reaching this level are typically flagged for exclusion.

### Level 3: Extreme (Explicit Death, Torture, or Severe Harm)

* **Description:** Graphic descriptions of severe injury, torture, explicit homicide, intense psychological abuse (e.g., severe gaslighting resulting in trauma), or lethal violence.
* **Context:** Completely prohibited in educational assessments. Often found in journalistic coverage of crimes, explicit historical accounts, or mature literature.

---
*For practical binary classification tasks (e.g., content filtering pipelines), it is recommended to group **Levels 0 and 1 as "Safe"**, and **Levels 2 and 3 as "Violent"**, balancing student safety with the preservation of rich literary materials.*
