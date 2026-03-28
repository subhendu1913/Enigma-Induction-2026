# AI AND ML

**OBJECTIVE: TEXT SUMMARIZER USING HUGGING FACE**

Build a **Text Summarization program** using a pre-trained model from Hugging Face. The program should take a **long paragraph as input** and generate a **short summary**.

---

**TOOLS REQUIRED:**

● Python  
● Hugging Face Transformers  
● Google Colab / Jupyter Notebook  

---

**TASK:**

1. Install the required libraries.  
2. Use the Hugging Face summarization pipeline.  
3. Input a long paragraph or article.  
4. Generate and display the summary.  

---

**BASIC IMPLEMENTATION:**

● `pip install transformers torch`  

● `from transformers import pipeline`  

● `summarizer = pipeline("summarization")`  

● `text = """
Artificial Intelligence is transforming many industries by allowing
machines to perform tasks that normally require human intelligence. It is
widely used in healthcare, finance, robotics, and automation.
"""`

● `summary = summarizer(text, max_length=50, min_length=20, do_sample=False)`  

● `print(summary[0]['summary_text'])`

---

**EXPECTED OUTPUT:**

The program should produce a **short and meaningful summary** of the given text.

---

**SUBMISSION:**

● Source code or notebook.  
● One example input and output summary.
