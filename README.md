<p align="center">
  <img src="https://img.shields.io/badge/Language-Java-007396" alt="Java">
  <img src="https://img.shields.io/badge/Type-Data%20Structures-blue" alt="Type">
  <img src="https://img.shields.io/badge/Project-Weather%20Storage-orange" alt="Project">
</p>

# <span style="color:#0b6efd;">Weather Data Storage System</span>

## 📌 Project Description
<p style="color:#444;">
The <strong style="color:#0b6efd;">Weather Data Storage System</strong> is a Java project to store, retrieve and manage temperature records across multiple cities and years. It demonstrates ADT design, dense 2D array storage, sparse storage (HashMap), row-major vs column-major traversal, and runtime & memory complexity analysis.
</p>

---

## 🎯 Features
- **WeatherRecord ADT**: `LocalDate date`, `String city`, `double temperature`  
- **Dense 2D Array Storage**: `double[][]` with sentinel `Double.NaN` for missing data  
- **Sparse Storage**: `HashMap<String, Double>` keyed by `year-city` (stores only existing records)  
- **Operations**:
  - Insert a record
  - Delete a record
  - Retrieve data for a city & year
- **Traversals**:
  - Row-major traversal (year by year)
  - Column-major traversal (city by city)
- **Complexity analysis** printed at program exit  
- **Interactive menu** for user input

---

## 🏗 System Design (Overview)
- **ADT**: `WeatherRecord` (or use plain types with a key format)
  - Attributes: `LocalDate date`, `String city`, `double temperature`
- **Dense Storage**
  - `double[][] dense` where rows = years, cols = cities
  - Missing values = `Double.NaN`
  - Insert/Delete/Retrieve: **O(1)** (indexing)
- **Sparse Storage**
  - `HashMap<String, Double> sparse` with key `"year-city"`
  - Insert/Delete/Retrieve: **O(1)** average
- **Traversal**
  - Row-major: iterate years outer, cities inner
  - Column-major: iterate cities outer, years inner

---

## ⚡ Complexity Analysis
- **Insert**: O(1)  
- **Delete**: O(1)  
- **Retrieve**: O(1)  
- **Row/Column Traversal**: O(R × C)  
- **Space (Dense)**: O(R × C)  
- **Space (Sparse)**: O(K) where K = number of stored records

---

## ▶️ How to Run
1. Save the file as `WeatherAssignment.java`  
2. Compile:
   ```bash
   javac WeatherAssignment.java
