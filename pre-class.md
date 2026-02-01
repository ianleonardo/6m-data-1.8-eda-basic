# **Pre-Class Study Guide: Fundamentals of Exploratory Data Analysis (EDA)**

⏱️ Estimated Time: 35 Minutes

🎯 Goal: Understand the core concepts of investigating and cleaning data before we dive into the code during class.

🎬 Watch this video: [[EDA with Pandas]](https://youtu.be/4-VoOWSFwOQ)

## **1\. What is EDA? (5 Minutes)**

**Exploratory Data Analysis (EDA)** is the first step in any data science project. Think of it as "interviewing" your data. Before you can build models or create charts, you must understand what you are working with.

**Why do we do it?**

* **To check assumptions:** Is the data what you think it is?  
* **To spot anomalies:** Are there errors, missing values, or weird outliers?  
* **To find patterns:** What are the basic trends?

**Analogy:** EDA is like a doctor's check-up. You check the vitals (heart rate, blood pressure) before diagnosing any specific illness.

## **2\. The "Health Check": Inspection & Summary (10 Minutes)**

When you first load a file (like a CSV or Excel sheet), you need to answer basic questions:

### **A. How big is it?**

We look at the **Dimensions** (Rows x Columns).

* *Pandas Tool:* .shape

### **B. What type of data is it?**

* **Numerical:** Integers (1, 2, 100\) or Floats (1.5, 3.14).  
* **Categorical/String:** Text data (e.g., "Red", "Blue", "New York").  
* *Pandas Tool:* .info() shows data types and non-null counts.

### **C. What does the distribution look like?**

We use **Summary Statistics** to get a snapshot without looking at every row.

* **Mean:** The average value.  
* **Median:** The middle value.  
* **Min/Max:** The range of the data.  
* *Pandas Tool:* .describe() automatically calculates these for all numeric columns.

## **3\. The "Cleanup": Handling Dirty Data (10 Minutes)**

Real-world data is rarely clean. It often contains errors that will break your analysis if ignored.

### **A. Missing Data (NaN)**

Sometimes data wasn't collected, or a system error occurred. Pandas represents this as NaN (Not a Number).

* **Option 1: Drop.** If a row has too many missing values, we might just throw it away (dropna).  
  * *Risk:* You lose data.  
* **Option 2: Impute (Fill).** We fill the empty spot with a reasonable guess, like the average (mean) or the previous value (fillna).  
  * *Risk:* You might introduce bias.

### **B. Duplicates**

Sometimes the same record appears twice (e.g., a customer clicked "submit" twice).

* **Why fix it?** It inflates your numbers (e.g., double-counting sales).  
* **Solution:** Identify unique row combinations and remove the extras (drop\_duplicates).

### **C. Outliers**

An outlier is a data point that differs significantly from other observations (e.g., a person aged 200).

* **Is it an error?** (e.g., typo). If so, fix or remove it.  
* **Is it real?** (e.g., a billionaire in an income dataset). If so, keep it, but analyze carefully.

## **4\. Refinement: Pattern Matching with Regex (5 Minutes)**

Sometimes clean-up isn't just about missing values. Sometimes the data itself is "messy" text (e.g., "Price: $500", "500 USD", or emails mixed with names).

* **Regular Expressions (Regex):** A special sequence of characters that acts as a search pattern. It helps you find, extract, or replace complex patterns in text strings.  
* **Common Use Cases:**  
  * **Validation:** Checking if an input looks like an email address (e.g., text@text.com).  
  * **Extraction:** Pulling out just the digits from a messy string (e.g., turning "$500.00" into 500.00).  
  * **Cleaning:** Removing special characters or unwanted whitespace.

**Analogy:** Regex is like a "Find" command on steroids. Instead of searching for the exact word "cat", you can search for "any 3-letter word starting with 'c' and ending with 't'".

## **5\. Preparation Checklist (5 Minutes)**

Before class, please ensure you have the following ready:

1. **Environment:** We will use the `pds` environment.  
2. **Libraries:** Ensure pandas and numpy are installed (pip install pandas numpy).  
3. **Mindset:** Be ready to look at "ugly" data and make decisions on how to fix it\!

## **🧠 Quick Self-Check Quiz**

Try to answer these without looking back at the text\!

1. **Scenario:** You have a dataset of 1,000 students. The "Age" column has 50 missing values. Would you drop those 50 rows or fill them with the average age? Why?  
2. **True or False:** The .describe() function gives you the same output for a column of text names as it does for a column of prices.  
3. **Definition:** What is the difference between an integer and a float?  
4. **Regex:** If you wanted to extract prices from text, what kind of pattern might you look for? (e.g., specific symbols or character types).




## **Reference**

- [Beginner's Guide to Statistics](https://www.analyticsvidhya.com/blog/2021/08/a-beginners-guide-to-statistics-for-machine-learning/)
- [Introduction to Regular Expressions in Python](https://developers.google.com/edu/python/regular-expressions)
