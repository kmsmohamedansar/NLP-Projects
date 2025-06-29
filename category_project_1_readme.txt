About this project

Smart Product Categorization with NLP and Zero-Shot Learning
Project Description
In the world of e-commerce, organizing products into the correct categories is essential for a great shopping experience. With thousands (or millions) of products, manual categorization is slow, expensive, and prone to error. In this project, I demonstrate how Natural Language Processing (NLP) and zero-shot learning can automatically match product names to their most relevant categories, dramatically improving efficiency and accuracy for online retailers.

Background
Imagine searching for “Eye Shadow Stick” on an online store, but the product is hidden under the wrong category. This is a common issue in large product catalogs, where products are constantly being added and updated. Traditional keyword matching can help, but it often misses context or synonyms. Modern AI models, however, can understand language more like a human and make smarter decisions about where a product belongs.

Objective
Goal:
Automatically evaluate whether each product in a large catalog is correctly categorized, using both simple text matching and advanced AI models.

Methodology
1. Data Preparation
Loaded a Walmart product dataset containing product names and category paths.

Converted the category strings into Python lists for easier handling.

Extracted the most specific (last) category for each product.

2. Simple Keyword Matching
Checked if the last category name appears in the product name (case-insensitive, spaces removed).

Flagged products where there was no clear keyword match.

3. Zero-Shot Classification with NLP
Used Hugging Face’s transformers library and the facebook/bart-large-mnli model.

For each product, asked the model: “Does this product name fit this category?”

The model returned a confidence score (0 to 1) for the match, even if the words weren’t identical.

4. Results Analysis
Compared the AI’s confidence scores to the simple keyword matches.

Identified products with low match scores for further review or correction.

Demonstrated that AI can catch subtle misclassifications that simple rules miss.

Key Results
High accuracy for clear matches: Products like “Blackout Curtains” scored near 1.0 for their correct category.

Low scores for mismatches: Products with unclear or unrelated names to their categories were flagged for review.

Scalable and efficient: The approach can be applied to thousands of products, saving countless hours of manual labor.

Why This Matters
Better Shopping Experience: Customers find what they want faster.

Reduced Errors: Fewer products are misplaced or mislabeled.

Scalable Solution: AI can handle massive catalogs that would overwhelm human teams.

Skills Demonstrated
Natural Language Processing (NLP)

Zero-Shot Learning

Data Cleaning & Preprocessing

Python (pandas, ast)

Hugging Face Transformers

Google Colab

E-commerce Data Modeling

Tools & Libraries
Python

pandas

ast (Abstract Syntax Trees)

Hugging Face Transformers

facebook/bart-large-mnli model

Google Colab

Sample Output
Product Name	Last Category	Match Score
Laura Mercier Caviar Stick Eye Color Sugar Frost ...	Eye Shadow Stick	0.23
Exultantex Grey Blackout Curtains for Living Room...	Blackout Curtains	0.99
Jessica London Women's Plus Size Stretch Knit Top...	Plus Size Tops	0.00
100% Cotton King Percale Duvet Set (3 Piece) Bed ...	King Duvet Covers	0.98
Disney Boys Graphic Tee Donald Duck Short Sleeve ...	Boys Outfit Sets	0.97
 
How It Works (Layman’s Terms)
Think of this project as building a super-smart librarian for an online store. Instead of reading every product and guessing where it should go, the AI “reads” the product name and its suggested category, then gives a score for how well they fit together. If the score is low, it’s a sign that the product might be in the wrong place and needs a second look.

Additional Links
Medium Article: How AI Organizes Online Stores (example)

Hugging Face Zero-Shot Classification Docs

Project Notebook on Google Colab (example)

Preview Image
Suggested preview image:
A flowchart showing “Product Name” and “Category” as inputs, an “AI Model” box in the middle, and “Match Score” as the output.
Alternatively, use a screenshot of your Colab output table or a royalty-free illustration of AI sorting products.

Conclusion
This project showcases the power of combining simple rules with advanced AI to solve real-world problems in e-commerce. By automating product categorization, we can make online shopping smoother for everyone and free up humans for more creative work.

Feel free to copy, edit, or expand this write-up for your portfolio or Medium post! If you want a shorter summary, more technical details, or a custom image suggestion, just ask.
