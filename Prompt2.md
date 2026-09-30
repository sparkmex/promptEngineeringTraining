# Role & System Configuration
Act as an expert summarization analyst. Your goal is to generate accurate, clear summaries on a given topic while strictly adapting the depth, completeness, and focus according to the specified API parameter `max_tokens`.

---

# Input Parameters & Variables
- **Topic:** {{topic, e.g., "The Importance of Mental Health"}}
- **API Runtime Configuration:** `max_tokens` = {{50 | 150 | 300}}

---

# Instructions & Constraints
1. **At max_tokens = 50:** Provide a brief, high-level summary focusing strictly on core ideas.
2. **At max_tokens = 150:** Provide a balanced, medium-length summary with key supporting details.
3. **At max_tokens = 300:** Provide a comprehensive summary with full depth, context, and detailed elaboration.
4. **Strict Token Adherence:** Keep the response within the allocated token threshold without cutting sentences mid-way.

---

# Few-Shot Demonstrations (Topic: "The Importance of Mental Health")

### Test Case 1: max_tokens = 50 (Short)
* **Prompt:** Summarize "The Importance of Mental Health" with `max_tokens=50`.
* **Generated Output:** Mental health is vital for overall well-being, influencing emotional, psychological, and social functioning. Prioritizing mental wellness helps manage stress, build resilient relationships, and maintain physical health, making accessible care and self-care practices essential for quality of life.

### Test Case 2: max_tokens = 150 (Medium)
* **Prompt:** Summarize "The Importance of Mental Health" with `max_tokens=150`.
* **Generated Output:** Mental health encompasses emotional, psychological, and social well-being, directly impacting how individuals think, feel, and act daily. Maintaining good mental health is essential at every stage of life, as it enables individuals to manage stress effectively, navigate interpersonal relationships, and adapt to change. When mental health is neglected, it can manifest in chronic physical conditions, reduced productivity, and social isolation. Promoting mental health awareness reduces stigma, encouraging people to seek timely professional support. Implementing routine self-care, mindfulness, and community support systems fosters resilience, ensuring healthier individuals and stronger societal communities.

### Test Case 3: max_tokens = 300 (Detailed)
* **Prompt:** Summarize "The Importance of Mental Health" with `max_tokens=300`.
* **Generated Output:** Mental health is a foundational pillar of overall human health, encompassing emotional, psychological, and social well-being. It shapes how individuals perceive reality, handle stress, relate to others, and make decisions throughout life. Prioritizing mental wellness is not merely the absence of mental illness, but the cultivation of psychological resilience, emotional balance, and adaptive coping mechanisms. 

The impacts of mental health extend across multiple dimensions of daily life:
1. **Physical Well-Being:** Strong connections exist between mental and physical health; unmanaged stress, anxiety, or depression significantly heighten the risk of cardiovascular disease, weakened immune function, and chronic fatigue.
2. **Social and Interpersonal Harmony:** Healthy emotional states foster healthy communication, empathy, and meaningful connections in family, social, and workplace settings.
3. **Economic and Personal Productivity:** Mental stability enhances cognitive function, focus, problem-solving skills, and creativity, allowing individuals to thrive professionally and contribute meaningfully to their communities.

Addressing mental health requires breaking systemic stigmas, expanding access to clinical therapy and psychiatric support, and encouraging daily wellness habits like exercise, adequate sleep, and social support networks. Prioritizing mental health creates safer, more empathetic societies.

---

# Comparative Analysis & Evaluation
- **Completeness:** At 50 tokens, the output captures only the core definition. At 150 tokens, it adds key impacts and preventative measures. At 300 tokens, it offers a fully complete breakdown with categorized sub-points.
- **Depth & Complexity:** Increasing `max_tokens` directly scales structural complexity—moving from a single paragraph to structured bullet points and multidimensional explanations.
- **Adaptability & Clarity:** The LLM scales conciseness and vocabulary density efficiently, maintaining sentence completion and high clarity across all three parameter thresholds.

---

# Solution Summary
**Prompting Techniques Used:** Dynamic Parameter Testing, Few-Shot Prompting, Structured Constraints, and Output Evaluation.  
**Justification:** Explicitly setting and demonstrating `max_tokens` at 50, 150, and 300 tokens trains the model to adjust information density dynamically while verifying length compliance and structural depth side-by-side.