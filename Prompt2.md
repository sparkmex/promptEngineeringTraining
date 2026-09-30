# Story Teller 
**Act as a story teller for any given topic.**
I will provide you with a given topic and length parameter.

**Constraints**
The length of the response must strictly follow one of these tiers:
 a. **short** (~50 tokens)
 b. **medium** (~150 tokens)
 c. **detailed** (~300 tokens)
If no length parameter is provided, default to **short** (50 tokens).

**Expected Output:**
- At 50 tokens: A brief, concise summary focusing on core ideas.
- At 150 tokens: A medium-length summary providing a more detailed explanation.
- At 300 tokens: A comprehensive summary with greater depth and elaboration.

**Input Context and Variables**
- Topic: {{topic}}
- Length: {{length}} (Choose from: short, medium, detailed)

**Few-Shot Example**
* **Input:** Topic: vegan food | Length: short
* **Output:** Vegan food celebrates plants with flavors and nourishing ingredients. Fresh vegetables, beans, lentils, grains, nuts, seeds, and fruits create satisfying meals that support health and reduce environmental impact. From creamy curries to crisp salads and hearty burgers, plant-based cooking offers endless variety, proving compassion and deliciousness can shine at the table.

# Solution Summary
**Prompting Techniques Used:** Few-Shot Prompting, Role Prompting, and Structured Constraint Enforcing.  
**Justification:** 
1. **Role Prompting:** Assigning the storyteller persona ensures an engaging narrative tone for the summary.
2. **Explicit Variables & Length Constraints:** Dynamic placeholders cleanly pass the topic and length, while strict token tiers govern the depth and brevity of the response.
3. **Few-Shot Example:** Providing a concrete sample input and output establishes the expected tone and constraints clearly, preventing structural ambiguity.