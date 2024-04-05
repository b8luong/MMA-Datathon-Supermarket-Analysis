# Datathon

---

## Project Overview

During the 2023 MMA Datathon, our team was tasked with a project designed to optimize grocery delivery for MM&A’s Supermarket, a fictional retail chain, in a partnership scenario with a delivery service, Instabasket (using real world data). Our case centered around creating a seamless delivery model by introducing a specialized Instabasket aisle, meticulously stocked with 1000 strategically chosen products. This initiative was aimed at reducing product choices, ensuring a broad coverage of customer needs are met while maintaining the order fulfillment rate.

A critical facet of this optimization involved mitigating the common issue of product unavailability. Traditionally, this would require personal shoppers to contact customers for substitutions, disrupting the shopping flow. Recognizing the absence of a formal substitution model within MM&A's infrastructure, we were also tasked on developing a robust substitution model. Leveraging advanced Natural Language Processing (NLP) techniques, we refined our substitution model, markedly increasing the average number of items fulfilled per order. This not only streamlined the delivery process but also significantly elevated customer satisfaction by ensuring smoother, more efficient order completions without the need for direct customer intervention.

---

##  Dataset

The dataset used was from real world data and can be downloaded from here, https://www.kaggle.com/competitions/instacart-market-basket-analysis/ 

---

## Methodology

#### 1. Product Selection:

<ol>
<li>Counted and sorted in descending order how many times an item were purchased</li>
<li>Relabeled tagged ‘missing’ data for products Labelled products as ‘frozen’, ‘refrigerated’, or ‘other’ based on department</li>
<li>Selected the top 100 products in 'frozen' and 'refrigerated' categories, then filled the remaining 800 spots with products from the 'other' category</li>
<li>Calculated metrics</li>
</ol>

#### 2. Product Substitution - using Natural Language Processing (NLP)

<ol>
<li>Text Tokenization: Break down product names into individual components (tokens) for analysis.</li>
<li>POS Tagging: Assign a part-of-speech label to each token using the nltk package's 'pos_tag' function</li>
<li>Count Vectorization: Convert tokenized product names into a bag-of-words representation</li>
<li>Cosine Similarity Calculation: Quantify the similarity between different product names' count vectors.</li>
<li>Substitute Identification: Filter products with high cosine similarity scores as potential substitutes</li>
</ol>

