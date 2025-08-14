# Employee-Review-Sentiment-Analyzer
1)	Employee review sentiment analysis 
 Problem Statement – 
• "In today’s data-driven work environments, employee feedback is a goldmine of insights, especially in large companies where thousands of reviews are submitted each year on platforms like Glassdoor or Indeed. 
• However, the problem is that these reviews are unstructured, written in free-flowing natural language, and are often ignored or underutilized by organizations because: • They’re difficult to analyse at scale 
• They contain inconsistent grammar, slang, and spelling. 
• Sentiments are often subtle, implicit, or mixed (e.g., “great learning but no work-life balance”) 
• Traditional HR reporting tools aren’t built to quantify qualitative data 
• As a result, decision-makers lack real-time visibility into how employees are feeling and why they’re satisfied or dissatisfied. This disconnects leads to: 
• Ineffective HR policies
• Delayed responses to cultural or management issues 
• Missed opportunities for employee retention and brand improvement" 
2)Objective- 
"The goal of this project was to convert thousands of unstructured employee reviews into structured, analysable insights. Using NLP, I automatically classified sentiments, extracted key themes from pros and cons, and visualized trends over time. This helped HR teams understand what employees value, identify recurring concerns, and make data-driven decisions for improving culture, policies, and retention.
" Data Preprocessing & Cleaning:
 "Each review had ‘Pros’ and ‘Cons’ written in free text. I cleaned the data by lowercasing, removing special characters using regex, and eliminating stopwords with NLTK. Then, I applied lemmatization (reduce word to base form) and used TF-IDF vectorization to convert the text into numerical features, helping identify key terms in each review.
3)Feature Extraction & Visualization -
After cleaning the text and extracting features, I used multiple visualizations to derive insights: 
• Boxen Plots showed the distribution of sentiment scores, helping identify companies with polarized reviews or high variability over time.
 • Time-Series Charts tracked sentiment trends year-wise, revealing patterns linked to internal changes like leadership or policy shifts. 
• WordClouds (generated using TF-IDF) highlighted top themes in Pros and Cons—e.g., ‘flexible’, ‘culture’ in Pros and ‘pressure’, ‘management’ in Cons—summarizing what employees value or criticize most."
4) Sentiment Analysis 
using VADER “For sentiment scoring, I used the VADER (Valence Aware Dictionary for Sentiment Reasoning) tool from NLTK, which is highly effective for social text like reviews. 
• I passed both Pros and Cons through VADER’s sentiment analyser. 
• It returns 4 scores: positive, negative, neutral, and a compound score (-1 to +1). • I used the compound score to assign a sentiment label (positive/neutral/negative) to each review.
 • VADER worked very well in this domain, and I achieved over 95% sentiment coverage, meaning the vast majority of reviews were accurately scored without needing manual labelling.” 
5) Keyword Extraction and Dataset Enrichment 
“I extracted the top 100 keywords from the ‘Pros’ section using TF-IDF scores. These keywords were then integrated back into the dataset to enrich it with feature-level insights: 
• For example, if ‘mentorship’ or ‘flexibility’ appeared frequently in a company’s reviews, it helped HR understand what cultural or operational aspects were strong. This transformed the dataset from just raw reviews to quantified employee sentiment intelligence.” 
6) Business Impact & Learnings “This project wasn't just about modelling — it had strong business implications: • HR teams could use it to track employee satisfaction trends 
• Management could identify recurring pain points in employee experiences 
• Decision-makers could get company-specific, year-wise dashboards to make informed policy changes Personally, I learned: 
• How to process and clean unstructured text data • How to apply TF-IDF and sentiment analysis tools in practice • How to visualize NLP results in a business-consumable format 
• And most importantly, how to convert subjective opinions into data-backed, actionable insights”
