# **Lesson Plan: Data Wrangling & Exploratory Analysis**

## **Overview**

* **Total Duration:** 3 hours  
* **Target Audience:** Adults with basic Python knowledge, moving into Data Science.  
* **Goal:** Transform raw, messy data into a clean, analyzed dataset ready for reporting.

## **Top 3 Critical Topics**

1. **Data Ingestion (I/O):** Reading non-standard CSVs and SQL databases. *Justification: Real data rarely comes in a perfectly formatted clean.csv.*  
2. **Data Cleaning:** Handling Missing Data and String Manipulation. *Justification: The provided HDB dataset requires parsing "60 years 4 months" into numbers to be useful.*  
3. **Descriptive Stats & Aggregation:** GroupBy and Summary Stats. *Justification: This is the primary method for answering business questions.*

## **Section Breakdown**

### **🕒 Section 1: The Data Pipeline (Ingestion) (60 min)**

**Objective:** Learners will be able to read data from CSVs with comments, no headers, and from SQL databases.

* **0-10 min:** Introduction & "Why data is messy."  
* **10-25 min (Demo):** pd.read\_csv parameters (header, names, skiprows). Using ex1.csv vs ex4.csv.  
* **25-50 min (Activity):** "The Data Ingestion Gauntlet". Learners must load 3 different files (CSV, Text, SQL) into DataFrames.  
* **50-60 min:** Debrief. Discussion on file paths and encoding.

### **🕒 Section 2: Digital Janitor (Cleaning) (60 min)**

**Objective:** Learners will be able to identify missing values and perform string transformations to fix column types.

* **0-10 min:** Concept: The 3 types of Missing Data (MCAR, MAR, MNAR) \- keep it high level.  
* **10-25 min (Demo):** isnull(), dropna(), fillna(). String methods .str.replace(), .str.split().  
* **25-50 min (Activity):** "Fixing the HDB Dataset".  
  * Task 1: Identify missing values (if any).  
  * Task 2: **The Challenge:** Convert remaining\_lease (e.g., "61 years 04 months") into a numeric remaining\_years column.  
* **50-60 min:** Debrief. Show different regex/slicing approaches.

### **🕒 Section 3: Data Storytelling (Analysis) (60 min)**

**Objective:** Learners will be able to use describe() and groupby() to extract insights.

* **0-10 min:** Concept: Central Tendency vs. Spread.  
* **10-25 min (Demo):** describe(), corr(), and the power of groupby().  
* **25-50 min (Activity):** "Market Analysis".  
  * Find the most expensive Town.  
  * Compare 3-Room vs 4-Room prices.  
  * Identify outliers in Price per Sqm.  
* **50-60 min:** Final Q\&A and wrap up.


---
# Lesson

## Brief

### Preparation

Ensure you have a basic understanding of statistics and regex as listed in [studies](./studies.md).

We will be using the `pds` environment for this lesson.

### Lesson Overview

This lesson covers the basics of Exploratory Data Analysis (EDA) and how to use Pandas to perform data cleaning and transformation.

You will learn how to summarize data using descriptive statistics, handle missing data, duplicates and outliers, perform data cleaning and transformation, manipulate strings and categorical data, and read (write) data from (to) files and databases.

---

## Part 1 - Exploratory Data Analysis (EDA) Basic

We will be using the `notebooks/eda_basic_lesson.ipynb` notebook throughout this lesson.

> Open the notebook in VSCode by double clicking on the file. Then select `pds` conda environment for the kernel.
>
> Follow on with the lesson in the notebook.
