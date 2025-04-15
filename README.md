# 📊 What and Where Are the World's Oldest Businesses?

This project explores data from [BusinessFinancing.co.uk](https://www.businessfinancing.co.uk/) to analyze the world's oldest continuously operating businesses. Using SQL, we uncover fascinating insights into companies that have survived hundreds (even over a thousand!) years through changing market conditions, innovations, and historical events.

---

## 🧠 Project Goals

In this intermediate SQL project, we aim to answer the following questions:

1. 🕰️ What is the **range of founding years** for the world’s oldest companies?
2. 🏆 What is the **oldest company in the world**, and what **industry** is it in?
3. 🏛️ How many companies were **founded before 1000 AD**, and which ones are they?
4. 🏭 What are the **most common industries** among the world’s oldest companies?
5. 🌍 What are the **oldest companies by continent**?
6. 🌐 What are the **most common industries** for the oldest companies on each continent?

---

## 🗃️ Data Structure

The dataset is organized into the following relational tables:

### `companies`
| Column        | Description                          |
|---------------|--------------------------------------|
| `company_id`  | Unique identifier for the company    |
| `name`        | Company name                         |
| `year_founded`| Year the company was established     |
| `country`     | Country the company is based in      |
| `industry_id` | Foreign key referencing `industries` |

### `industries`
| Column         | Description                          |
|----------------|--------------------------------------|
| `industry_id`  | Unique identifier for the industry   |
| `industry_name`| Name of the industry                 |

### `countries`
| Column   | Description         |
|----------|---------------------|
| `country`| Country name        |
| `continent`| Continent name   |

---

## 🧾 SQL Highlights

Below are some key SQL queries used in this project:

### 1. Range of Founding Years

```sql
SELECT MIN(year_founded) AS oldest_year,
       MAX(year_founded) AS newest_year
FROM companies;
🛠 Tools Used
SQL (PostgreSQL/MySQL)

Relational database concepts

JOINs and subqueries

Aggregation and filtering

📚 References
Dataset sourced from BusinessFinancing.co.uk

SQL techniques inspired by DataCamp's Joining Data with SQL course

💡 Future Enhancements
Add visualizations using Python or Tableau

Perform time series analysis of company survivability

Create a dashboard summarizing key insights

